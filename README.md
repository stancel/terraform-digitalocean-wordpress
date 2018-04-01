# terraform-wordpress-digitalocean

A Terraform module for creating a fully functional WordPress Droplet.

# Module Input Variables

Defaults:

* `image` - The Droplet image ID or slug, defaults to `wordpress-16-04`
* `name` - The name of the Droplet, defaults to `wordpress`
* `region` - The region of the Droplet, defaults to `nyc1`
* `size` - The instance size, defaults to `1gb`
* `backups` - Boolean controlling if backups are made, defaults to `false`
* `monitoring` - Boolean controlling whether monitoring agent is installed, defaults to `false`
* `ipv6` - Boolean controlling if IPv6 is enabled, defaults to `false`
* `private_networking` - Boolean controlling if private networks are enabled, defaults to `false`
* `resize_disk` - Boolean controlling whether to increase the disk size when resizing a Droplet, defaults to `true`

# Module Outputs

* `ip` - The public ipv4 address for the Droplet

# Usage

## Generate a Personal Access Token

https://www.digitalocean.com/community/tutorials/how-to-use-the-digitalocean-api-v2#how-to-generate-a-personal-access-token

## Example

Take a look at [example.tf](./example/example.tf) for a working example.

## Applying the changes

Review your changes:

```
terraform plan
```

Apply your changes:

```
terraform apply -auto-approve
```

After about a minute, Terraform will output the IP address of the Droplet.

## Enabling WordPress

In order to start the wordpress installation, you will need to ssh into the instance. The credentials will be provided via e-mail.

# Contributing

When contributing to this repository, please first discuss the change you wish to make via a Github issue.
