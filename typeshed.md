# Modules used by cwltool and schema-salad

|Module|2and3|3      |
|-------|------|-------|
|1. avro|  |     |
|2. cachecontrol|||
|3. pkg_resources||X|
|4. rdflib||       |
|5. requests| X |    |
|6. ruamel||       |
|7. argparse|X|    |
|8. mistune||      |
|9. pathlib||X     |
|10. pprint|X|     |
|11. re||X         |
|12. urlparse||    |
|13. logging|X|    |
|14. shellescape||(shlex is used instead?) |
|15. yaml|X|       |
|16. StringIO||(not used for python3?)    |
|17. io||X         |
|18. subprocess||X |
|19. typing||X     |
|20. urllib||X     |
|21. builtins||X   |
|22. six|| X       |


## Mypy installation

Clone mypy repo

Install virtualenv when there's some problems with ubuntu:
```
python3.6 -m venv /path/to/virt/env --without-pip
cd /path/to/virt/env
source /path/to/virt/env/bin/activate
wget https://bootstrap.pypa.io/get-pip.py
python get-pip.py
```

Install requirements:
```
pip install -r test-requirements.txt
```

## Mypy usage

Copy typeshed files into `mypy/typeshed` directory and run:
```
PYTHONPATH=.. python3 tests/mypy_test.py
```
