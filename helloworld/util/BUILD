# Copyright 2020 Pants project contributors.
# Licensed under the Apache License, Version 2.0 (see LICENSE).

python_library(
    # `name` defaults to the name of this directory, i.e., `util`.
    # `sources` defaults to ['*.py', '!*_test.py', '!test_*.py', '!conftest.py'].
    dependencies = [
        "//:setuptools",
        "//:translate",
        "helloworld/protos",
    ],
    # See https://pants.readme.io/docs/python-setup-py-goal.
    provides = setup_py(
        name='helloworld.util',
        version='0.0.1',
        description='Greeting library utilities',
    ),
)

python_tests(
    name = 'tests',
    # `sources` defaults to ['*_test.py', 'test_*.py', 'conftest.py'].
    dependencies = [
        ":config_loader_test_data",
        ":util",
    ],
)

resources(
    name = 'config_loader_test_data',
    sources = ['config_loader_test_data.json'],
)
