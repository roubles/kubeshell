kubeshell
=========

kubeshell is a command line tool to interactively shell in to (and out
of) kubernetes pods.

::

   ~$ kubeshell
    Pick your pod:
       NAME                                                              READY   STATUS             RESTARTS   AGE

    => some-pod-7f9b5f475wdcmv                                           1/1     Running            0          26h
       some-other-pod-556p4cfw                                           0/1     CrashLoopBackOff   83         7h10m
       yet-another-pod-589cf77568-rjzkv                                  0/1     Running            82         7h4m
       exit

Install
-------

You can install from pypi as follows

::

   $ pip install kubeshell

OR, clone the repo

::

   $ git clone https://github.com/roubles/kubeshell
   $ cd kubeshell
   $ python setup.py install

Usage
-----

::

   usage: kubeshell [-h] [-s SHELL] [-n NAMESPACE] [substring]

   interactively shell into k8s pods

   positional arguments:
     substring             substring to filter pods

   optional arguments:
     -h, --help            show this help message and exit
     -s SHELL, --shell SHELL
                           Which shell to use
     -n NAMESPACE, --namespace NAMESPACE
                           Which namespace to use
