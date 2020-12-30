# Terraform

---

This role installs the Terraform CLI on Windows or Linux servers.

## Requirements

---

There are no external requirements for this role.

## Role Variables

---

There are a few variables that can be set from the playbook if you like and the role makes an assumption in the defaults
section.

### terraform_version

This is the version of terraform that will be installed, the complete list can be found on the [Hashicorp Releases](https://releases.hashicorp.com/terraform/) page. The value should only include everything after 'terraform_' so for the latest version the value would be:

```yaml
  terraform_version: 0.14.3
```

### download_dir

This is the directory where the Terraform installation package will be downloaded to.

#### Windows Default

```yaml
  download_dir: "C:\\Windows\\Temp"
```

#### Linux Default

```yaml
  download_dir: "/tmp"
```

### terraform_dir

This is the directory where Terraform is installed into

#### Windows Default

```yaml
  terraform_dir: "C:\\ProgramData\\Hashicorp\\Terraform"
```

#### Linux Default

```yaml
  terraform_dir: "/opt/terraform"
```

## Dependencies

---

There are no external dependencies for this role.

## Example Playbook

---

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

``` yaml
    - hosts: all
      roles:
         - terraform
      vars:
        terraform_version: 0.14.3
```

## License

---

MIT

## Author Information

---

My name is Jeff Patton, feel free to contact me via [issues](https://github.com/anisble-playbooks/terraform/issues).
