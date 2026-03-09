# Report for SEBSCHELLI of SciTweets-Classifier

## Report generated at 2026-03-09 14:22:02

## Checking for required files

Found required file: license <br>Missing required file: postbuild <br>Missing required file: citation <br>No duplicate files found.

Found required file: scitweets_test.tsv in  <br>Found required file: scitweets_classifier.py in  <br>Found required file: README.md in  <br>Found required file: scitweets_test_out.tsv in  <br>Found required file: requirements.txt in  <br>Found required file: LICENSE in  <br>Found required file: .github in  <br>Found required file: .git in  <br>All Binder Files found <br>No duplicate files found.

## Checking License: 

Found MIT License, License accepted 

## Checking Readme: 

Found one title: Accepted<br>Found subtitle: Contents of the Repository<br>Found subtitle: Usage<br>Found subtitle: Data<br>Found subtitle: Publication:<br>Found subtitle: Licensing<br>Found subtitle: Contact<br>Found subtitle: Acknowledgment<br>Missing subtitle: Contact Details<br>Missing subtitle: Description<br>Missing subtitle: Environment Setup<br>Missing subtitle: Hardware Requirements<br>Missing subtitle: How to Use<br>Missing subtitle: Input Data<br>Missing subtitle: Output Data<br>Missing subtitle: Technical Details<br>Missing subtitle: Use Cases<br>

## Testing repository with repo2docker

Repo2Docker build failed.<br> Repo2Docker Output:<br>```text<br> 1.1.2, 1.1.3, 1.1.4, 1.1.5, 1.2.0, 1.2.1, 1.2.2, 1.2.3, 1.2.4, 1.2.5, 1.3.0, 1.3.1, 1.3.2, 1.3.3, 1.3.4, 1.3.5, 1.4.0, 1.4.1, 1.4.2, 1.4.3, 1.4.4, 1.5.0, 1.5.1, 1.5.2, 1.5.3, 2.0.0, 2.0.1, 2.0.2, 2.0.3, 2.1.0, 2.1.1, 2.1.2, 2.1.3, 2.1.4, 2.2.0, 2.2.1, 2.2.2, 2.2.3, 2.3.0, 2.3.1, 2.3.2, 2.3.3)
#20 0.756 ERROR: No matching distribution found for pandas==3.0.1
#20 ERROR: process "/bin/sh -c ${KERNEL_PYTHON_PREFIX}/bin/pip install --no-cache-dir -r \"requirements.txt\"" did not complete successfully: exit code: 1
------
 > [15/18] RUN /srv/conda/envs/notebook/bin/pip install --no-cache-dir -r "requirements.txt":
0.493 Collecting emoji==2.15.0 (from -r requirements.txt (line 1))
0.523   Downloading emoji-2.15.0-py3-none-any.whl.metadata (5.7 kB)
0.540 Collecting nltk==3.9.3 (from -r requirements.txt (line 2))
0.547   Downloading nltk-3.9.3-py3-none-any.whl.metadata (3.2 kB)
0.695 ERROR: Ignored the following versions that require a different python version: 3.0.0 Requires-Python >=3.11; 3.0.0rc0 Requires-Python >=3.11; 3.0.0rc1 Requires-Python >=3.11; 3.0.0rc2 Requires-Python >=3.11; 3.0.1 Requires-Python >=3.11
0.695 ERROR: Could not find a version that satisfies the requirement pandas==3.0.1 (from versions: 0.1, 0.2, 0.3.0, 0.4.0, 0.4.1, 0.4.2, 0.4.3, 0.5.0, 0.6.0, 0.6.1, 0.7.0, 0.7.1, 0.7.2, 0.7.3, 0.8.0, 0.8.1, 0.9.0, 0.9.1, 0.10.0, 0.10.1, 0.11.0, 0.12.0, 0.13.0, 0.13.1, 0.14.0, 0.14.1, 0.15.0, 0.15.1, 0.15.2, 0.16.0, 0.16.1, 0.16.2, 0.17.0, 0.17.1, 0.18.0, 0.18.1, 0.19.0, 0.19.1, 0.19.2, 0.20.0, 0.20.1, 0.20.2, 0.20.3, 0.21.0, 0.21.1, 0.22.0, 0.23.0, 0.23.1, 0.23.2, 0.23.3, 0.23.4, 0.24.0, 0.24.1, 0.24.2, 0.25.0, 0.25.1, 0.25.2, 0.25.3, 1.0.0, 1.0.1, 1.0.2, 1.0.3, 1.0.4, 1.0.5, 1.1.0, 1.1.1, 1.1.2, 1.1.3, 1.1.4, 1.1.5, 1.2.0, 1.2.1, 1.2.2, 1.2.3, 1.2.4, 1.2.5, 1.3.0, 1.3.1, 1.3.2, 1.3.3, 1.3.4, 1.3.5, 1.4.0, 1.4.1, 1.4.2, 1.4.3, 1.4.4, 1.5.0, 1.5.1, 1.5.2, 1.5.3, 2.0.0, 2.0.1, 2.0.2, 2.0.3, 2.1.0, 2.1.1, 2.1.2, 2.1.3, 2.1.4, 2.2.0, 2.2.1, 2.2.2, 2.2.3, 2.3.0, 2.3.1, 2.3.2, 2.3.3)
0.756 ERROR: No matching distribution found for pandas==3.0.1
------
Dockerfile:118
--------------------
 116 |     COPY --chown=1001:1001 src/requirements.txt ${REPO_DIR}/requirements.txt
 117 |     USER ${NB_USER}
 118 | >>> RUN ${KERNEL_PYTHON_PREFIX}/bin/pip install --no-cache-dir -r "requirements.txt"
 119 |     
 120 |     # ensure root user after preassemble scripts
--------------------
ERROR: failed to build: failed to solve: process "/bin/sh -c ${KERNEL_PYTHON_PREFIX}/bin/pip install --no-cache-dir -r \"requirements.txt\"" did not complete successfully: exit code: 1
Traceback (most recent call last):
  File "/opt/hostedtoolcache/Python/3.12.12/x64/bin/repo2docker", line 6, in <module>
    sys.exit(main())
             ^^^^^^
  File "/opt/hostedtoolcache/Python/3.12.12/x64/lib/python3.12/site-packages/repo2docker/__main__.py", line 476, in main
    r2d.start()
  File "/opt/hostedtoolcache/Python/3.12.12/x64/lib/python3.12/site-packages/repo2docker/app.py", line 846, in start
    self.build()
  File "/opt/hostedtoolcache/Python/3.12.12/x64/lib/python3.12/site-packages/repo2docker/app.py", line 809, in build
    for l in picked_buildpack.build(
             ^^^^^^^^^^^^^^^^^^^^^^^
  File "/opt/hostedtoolcache/Python/3.12.12/x64/lib/python3.12/site-packages/repo2docker/buildpacks/base.py", line 672, in build
    yield from client.build(**build_kwargs)
  File "/opt/hostedtoolcache/Python/3.12.12/x64/lib/python3.12/site-packages/repo2docker/docker.py", line 162, in build
    yield from execute_cmd(args, True)
  File "/opt/hostedtoolcache/Python/3.12.12/x64/lib/python3.12/site-packages/repo2docker/utils.py", line 76, in execute_cmd
    raise subprocess.CalledProcessError(ret, cmd)
subprocess.CalledProcessError: Command '['docker', 'buildx', 'build', '--progress', 'plain', '--build-arg', 'NB_USER=runner', '--build-arg', 'NB_UID=1001', '--tag', 'r2dtestee1773066122', '--platform', 'linux/amd64', '/tmp/tmpiqw23fk_']' returned non-zero exit status 1.
<br>```<br>