Ansible Server
==============

This is the ansible server playbok. It is designed to be executed on servers.

More generally, a server is likely to be a stateful node that has some application deployed on it (such as a
kubernetes worker). While as much as possible I tend to build immuatable infrastructure, there are still some
nodes that must be managed on an ongoing basis (such as the HOST nodes for kubelet, docker build nodes etc) 

Customization
-------------

If there are tasks that are specific to this property, create roles for them. If the tasks can be used, create them in
another repository, and add that repository as a submodule to this one

Execution Instruction
---------------------

The following command will execute the playbook:

```
$ ansible-playbook -i inventory server.yaml
```

Authentication is handled out of band; it assumes that the user will have the appropriate `${HOME}/.ssh/config` file
set up. Such a file will look something like the following:

```
Host host01*
    User debian
    IdentityFile path/to/the/private/key.pem
```

Contact: hello@andrewhowden.com
Web:     https://www.andrewhowden.com/
