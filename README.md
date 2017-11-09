# Hello-word

I am trying to install Opencv 3 on my Rpi 3.

For this, I followed the instructions of A.Rosebrock: Installation Guide: Raspberry Pi 3 + Raspbian Jessie + OpenCV 3

My problem is this:
In step 4 of the guide: after entering the command: $ mkvirtualenv cv -p python2, I get the following error:

OSError: Command /home/pi/.virtualenvs/cv/bin/python2 - setuptools pip wheel failed with error code 2

Thanks you in advance to help me to solve this problem.
Regards

see below my screenshot for details:

pi@raspberrypi:~ $ source ~/.profile
pi@raspberrypi:~ $ mkvirtualenv cv -p python2
Running virtualenv with interpreter /usr/bin/python2
New python executable in /home/pi/.virtualenvs/cv/bin/python2
Also creating executable in /home/pi/.virtualenvs/cv/bin/python
Installing setuptools, pip, wheel...
  Complete output from command /home/pi/.virtualenvs/cv/bin/python2 - setuptools pip wheel:
  The directory '/home/pi/.cache/pip/http' or its parent directory is not owned by the current user and the cache has been disabled. Please check the permissions and owner of that directory. If executing pip with sudo, you may want sudo's -H flag.
The directory '/home/pi/.cache/pip' or its parent directory is not owned by the current user and caching wheels has been disabled. check the permissions and owner of that directory. If executing pip with sudo, you may want sudo's -H flag.
Collecting setuptools
  Downloading setuptools-36.6.0-py2.py3-none-any.whl (481kB)
Exception:
Traceback (most recent call last):
  File "/usr/local/lib/python2.7/dist-packages/virtualenv_support/pip-9.0.1-py2.py3-none-any.whl/pip/basecommand.py", line 215, in main
    status = self.run(options, args)
  File "/usr/local/lib/python2.7/dist-packages/virtualenv_support/pip-9.0.1-py2.py3-none-any.whl/pip/commands/install.py", line 324, in run
    requirement_set.prepare_files(finder)
  File "/usr/local/lib/python2.7/dist-packages/virtualenv_support/pip-9.0.1-py2.py3-none-any.whl/pip/req/req_set.py", line 380, in prepare_files
    ignore_dependencies=self.ignore_dependencies))
  File "/usr/local/lib/python2.7/dist-packages/virtualenv_support/pip-9.0.1-py2.py3-none-any.whl/pip/req/req_set.py", line 664, in _prepare_file
    dist = abstract_dist.dist(finder)
  File "/usr/local/lib/python2.7/dist-packages/virtualenv_support/pip-9.0.1-py2.py3-none-any.whl/pip/req/req_set.py", line 110, in dist
    self.req_to_install.source_dir))[0]
IndexError: list index out of range
----------------------------------------
...Installing setuptools, pip, wheel...done.
Traceback (most recent call last):
  File "/usr/local/lib/python2.7/dist-packages/virtualenv.py", line 2328, in <module>
    main()
  File "/usr/local/lib/python2.7/dist-packages/virtualenv.py", line 713, in main
    symlink=options.symlink)
  File "/usr/local/lib/python2.7/dist-packages/virtualenv.py", line 945, in create_environment
    download=download,
  File "/usr/local/lib/python2.7/dist-packages/virtualenv.py", line 901, in install_wheel
    call_subprocess(cmd, show_stdout=False, extra_env=env, stdin=SCRIPT)
  File "/usr/local/lib/python2.7/dist-packages/virtualenv.py", line 797, in call_subprocess
    % (cmd_desc, proc.returncode))

OSError: Command /home/pi/.virtualenvs/cv/bin/python2 - setuptools pip wheel failed with error code 2
pi@raspberrypi:~ $



