# templateAIOps

The intent of this repo is to make it easier and faster to set up a github repo in your org for Responsible AI projects.

** NOTE: ** This repo is a work in progress!

 This repo includes:
- consistent repo metrics
    - capturing Github provided metrics
    - aggregate and report
- Build pipelines
    - consistent creation and run

Folders and files:
- AUTHORS - Provides list of maintainers and contributors with info about contributions
- CONTRIBUTING.md - Copied an existing file, can be modified to change approach.
- LICENSE.md - MIT license
- README.md - info for repo. This README.md will document how to personalize the repo.
- SECURITY.md - Microsoft security recommendation

- Test
    - create expected test types and pipeline naming, folder hierarchy and format
- Contrib - MS or not?
- license - MIT + MS?

benchmarks: optional
   - if metrics are calculated on the models in repo, this is a handy place to store
docker: optional
   - Readme explains common docker image creation and use
scripts: recommended
   - Contains scripts for setup, environment.yml, etc
tests: recommended
   - tests/unit, tests/smoke, tests/integration
     These folders store the unit, smoke and integration tests. Each are described in the README.md in tests
   - tests/AIDevOps
     As MLOps tends to refer to pipelines that train and deploy models, a different name was selected.  This folder will contain the DevOps pipeline files to run build and tests in unit/smoke/integration.

tools: suggested
   - this includes files like flake8, pre-commit file, pyproject.toml (set char per line)

tools/repo_metrics : strongly recommended
   - this requires setting up cosmos db to enable capturing and reporting metrics

DevOps pipelines 
- recommend keyvault for secrets/subscription info
- Pep8 - make requirement?

## NOTE When using Conda in your pipeline
This devops bug fix is needed:

- bash: |
    echo "##vso[task.prependpath]/data/anaconda/bin"
  displayName: Add Conda to PATH

Recommend Issue templates:
- Recommend both Bug Report and Feature Request Templates

Suggested content:
```
Bug Report
### Description
<!--- Describe your issue/bug/request in detail -->

### In which platform does it happen?
<!--- Describe the platform where the issue is happening (use a list if needed) -->
<!--- For example: -->
<!--- * Azure Data Science Virtual Machine. -->
<!--- * Azure Databricks.  -->
<!--- * Other platforms.  -->

### How do we replicate the issue?
<!--- Please be specific as possible (use a list if needed). -->
<!--- For example: -->
<!--- * Create a conda environment for pyspark -->
<!--- * Run unit test `test_sar_pyspark.py` with `pytest -m 'spark'` -->
<!--- * ... -->

### Expected behavior (i.e. solution)
<!--- For example:  -->
<!--- * The tests for SAR PySpark should pass successfully. -->

### Other Comments

Suggested Feature Request:
### Description
<!--- Describe your expected feature in detail -->

### Expected behavior with the suggested feature
<!--- For example:  -->
<!--- *Adding algorithm xxx will help people understand more about xxx use case scenarios. -->

### Other Comments
```


Open Questions:
- do we want to force autorun of precommit like pep8
- MANIFEST.in - put in what folder?
- environment.yml - where?
- preferences on location to store pypi files?
