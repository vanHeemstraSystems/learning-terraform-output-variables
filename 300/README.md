# 300 - Learning Our Subject

Watch me declare an input variable.

```
variable "location" {
  type = string
}
```
variables.tf

Inputs come in three primitive types:

- string, 
- boolean, or 
- number

And two collection types: 

- list, or 
- map

Watch me declare an output variable:

```
output "location" {
  value = var.location
}
```
outputs.tf

```Output``` variables let you expose information generated within terraform and pass it along to the next step in your process.

Watch me run terraform init:

```
$ terraform init
```

Watch me run terraform plan:

```
$ terraform plan
```

If values for input variables are not otherwise specified, terraform will wait for the manual input from the user.

```
$ var.location
  Enter a value: westus
```

Watch me run terraform apply:

```
$ terraform apply
```

The ```apply``` operation has the same behavior.

Watch me run terraform apply again:

```
$ terraform apply
```

Terraform is designed to run over and over again. If there's no change it won't do anything.

Watch me run terraform apply after changing the value from ```West U.S``` to ```East US```:

```
$ var.location
  Enter a value: eastus
```

```
$ terraform apply
```

Terraform will detect changes in your solution and propose tasks of either create, destroy, or inline update.

Notice how it's changing the value from ```West U.S``` to ```East US```.

That's it!
