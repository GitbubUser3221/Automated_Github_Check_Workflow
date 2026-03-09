# Report for SEBSCHELLI of SciTweets-Classifier

## Report generated at 2026-03-09 14:13:25

## Checking for required files

Found required file: license <br>Missing required file: postbuild <br>Missing required file: citation <br>No duplicate files found.

Found required file: scitweets_test.tsv in  <br>Found required file: scitweets_classifier.py in  <br>Found required file: README.md in  <br>Found required file: scitweets_test_out.tsv in  <br>Found required file: requirements.txt in  <br>Found required file: LICENSE in  <br>Found required file: .github in  <br>Found required file: .git in  <br>All Binder Files found <br>No duplicate files found.

## Checking License: 

Found MIT License, License accepted 

## Checking Readme: 

Found one title: Accepted<br>Found subtitle: Contents of the Repository<br>Found subtitle: Usage<br>Found subtitle: Data<br>Found subtitle: Publication:<br>Found subtitle: Licensing<br>Found subtitle: Contact<br>Found subtitle: Acknowledgment<br>Missing subtitle: Contact Details<br>Missing subtitle: Description<br>Missing subtitle: Environment Setup<br>Missing subtitle: Hardware Requirements<br>Missing subtitle: How to Use<br>Missing subtitle: Input Data<br>Missing subtitle: Output Data<br>Missing subtitle: Technical Details<br>Missing subtitle: Use Cases<br>

## Testing repository with repo2docker

Repo2Docker build failed.<br> Repo2Docker Output:<br>```text<br>.039           return hook(config_settings)
#20 4.039         File "/tmp/pip-build-env-k1t4ueso/overlay/lib/python3.10/site-packages/setuptools/build_meta.py", line 333, in get_requires_for_build_wheel
#20 4.039           return self._get_build_requires(config_settings, requirements=[])
#20 4.039         File "/tmp/pip-build-env-k1t4ueso/overlay/lib/python3.10/site-packages/setuptools/build_meta.py", line 301, in _get_build_requires
#20 4.039           self.run_setup()
#20 4.039         File "/tmp/pip-build-env-k1t4ueso/overlay/lib/python3.10/site-packages/setuptools/build_meta.py", line 520, in run_setup
#20 4.039           super().run_setup(setup_script=setup_script)
#20 4.039         File "/tmp/pip-build-env-k1t4ueso/overlay/lib/python3.10/site-packages/setuptools/build_meta.py", line 317, in run_setup
#20 4.039           exec(code, locals())
#20 4.039         File "<string>", line 19, in <module>
#20 4.039       ModuleNotFoundError: No module named 'pkg_resources'
#20 4.039       [end of output]
#20 4.039   
#20 4.039   note: This error originates from a subprocess, and is likely not a problem with pip.
#20 4.091 error: subprocess-exited-with-error
#20 4.091 
#20 4.091 × Getting requirements to build wheel did not run successfully.
#20 4.091 │ exit code: 1
#20 4.091 ╰─> See above for output.
#20 4.091 
#20 4.091 note: This error originates from a subprocess, and is likely not a problem with pip.
#20 ERROR: process "/bin/sh -c ${KERNEL_PYTHON_PREFIX}/bin/pip install --no-cache-dir -r \"requirements.txt\"" did not complete successfully: exit code: 1
------
 > [15/18] RUN /srv/conda/envs/notebook/bin/pip install --no-cache-dir -r "requirements.txt":
4.039       [end of output]
4.039   
4.039   note: This error originates from a subprocess, and is likely not a problem with pip.
4.091 error: subprocess-exited-with-error
4.091 
4.091 × Getting requirements to build wheel did not run successfully.
4.091 │ exit code: 1
4.091 ╰─> See above for output.
4.091 
4.091 note: This error originates from a subprocess, and is likely not a problem with pip.
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
subprocess.CalledProcessError: Command '['docker', 'buildx', 'build', '--progress', 'plain', '--build-arg', 'NB_USER=runner', '--build-arg', 'NB_UID=1001', '--tag', 'r2dtestee1773065605', '--platform', 'linux/amd64', '/tmp/tmp808aj7zo']' returned non-zero exit status 1.
<br>```<br>