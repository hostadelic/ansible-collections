Hostadelic Ansible collections
==============================

Ansible collections of various uses.

They were proven useful in our internal projects and may be so to some.

# Usage

In your repository add to your `requirements.yaml` the following snippet:

```
collections:
- name: https://github.com/hostadelic/ansible-collections.git#/hostadelic/
  type: git
  version: main
```

This will install all collections under the `hostadelic` umbrella. You can
limit the collections by being more precise in the hash path.

The `main` version is actually a ref name (branch name, tag name, commit
id...). So you can lock the version if need be.

# Releasing (to those in the know)

The private way is to use the bare repository.

When you're satisfied with the version, tag it accordingly and push tag.

# Releasing (to broader audience)

The proper way to release is to use `galaxy.ansible.com`, you should be an
owner of the organization on Github and create an account on the aforementioned
website, or an already accounted for owner should add you.

Then you would get your API key and register it to the `galaxy.yaml` file.

To release a collection, you would enter its directory and build it:

```console
$ cd /dev/ansible-collections/hostadelic/devops
$ ansible-galaxy collection build
Created collection for hostadelic.devops at /dev/ansible-collections/hostadelic/devops/hostadelic-devops-0.0.1.tar.gz
```

And then publish:

```console
$ ansible-galaxy collection publish
```

There's an `--api-key` option in case you didn't find where to put it in the
configuration file (I eye slashed the doc and only saw it mentioned, not
detailed).
