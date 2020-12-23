# random-pet
Terraform random_pet example

## Pre-requirements
- [git](https://git-scm.com/downloads) need to be installed 
- [terraform](https://www.terraform.io/downloads.html) need to be installed 

## How to consume

```bash
git clone git@github.com:base-line/random-pet.git
cd random-pet
terraform init
terraform apply
```

## As result

use `terraform state list` to check the list of created resources

```bash
random_pet.name
```

as well can run `terraform show`

```bash
# random_pet.name:
resource "random_pet" "name" {
    id        = "pre-repeatedly-solely-smooth-octopus"
    keepers   = {
        "key" = "value"
    }
    length    = 4
    prefix    = "pre"
    separator = "-"
}
```

## Destroy

destroy created infrastructure if need be

```
terraform destroy
```