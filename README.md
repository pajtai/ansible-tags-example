# ansible tags

The intial `vagrant up` and subsequent `vagrant provision` will run the playbook with the `example-3` tag.
The dependent `example-1` is only run if the `example-2` role is commented out in `ansible/site.yml` making `example-3` the first role. `example-1`
will not run with `site.yml` as is.
