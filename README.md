# PyTest

## install pytest
    pip install pytest

### Pytest requires the test function names to start with test

## Run all tests
    pytest Or pytest -v

## To execute the tests from a specific file
    pytest <filename> -v

## To execute the tests containing a string in its name we can use the following syntax −
    pytest -k <substring> -v

## group the tests using markers
    import pytest
    @pytest.mark.<markername>

## Run the tests using markers
    pytest -m <markername> -v

## Fixture the tests
#### Fixtures are used to feed some data to the tests
    import pytest
    @pytest.fixture

## make fixtures accessible across multiple test files
#### create conftest.py file
    import pytest
    @pytest.fixture

## Parameterizing a test 
    import pytest
    @pytest.mark.parametrize

## xfail tests 
    import pytest
    @pytest.mark.xfail

## skip tests
    import pytest
    @pytest.mark.skip

## stop the execution of test suite soon after n number of test fails
    pytest --maxfail = <num>

## Run Tests in Parallel
#### install pytest-xdist
    pip install pytest-xdist
#### run tests parallely
    pytest -n 3

## generate the details of the test execution in an xml file
    pytest <file-name>.py -v --junitxml="result.xml"
