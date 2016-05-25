# hello-world-packer

This is a simple packer template that will build an AMI with the Chef Recipe that I've written.

To run it need to run install all the cookbook dependencies locally by running
```'berks vendor vendor/cookbooks' ```
in the chef recipe directory

After that is done update the cookbook_paths in the template and run packer to build

To build the image run:

```packer build -var 'aws_access_key=YOUR ACCESS KEY' -var 'aws_secret_key=YOUR SECRET KEY' hello_world.json ```

or 

```packer build hello_world.json ```

if your environment variables are set with your AWS keys
