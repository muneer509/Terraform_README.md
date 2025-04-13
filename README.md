**tfvars**: A *.tfvars file (or terraform.tfvars) is used to assign values to variables declared in your Terraform configuration.

It separates configuration (variables) from values (inputs), making your code reusable, clean, and easy to manage across dev, staging, or prod environments.

**Variables**: in Terraform allow you to parameterize your infrastructure code, so you can define values once and reuse or override them as needed — for example, across dev, staging, and prod environments.

Instead of hardcoding values (bad practice), you define variables and pass values through .tfvars files, CLI, or environment variables.

**Outputs**: Outputs in Terraform are used to display useful information after a terraform apply or terraform output command.

They are typically used to:

Show the result of a configuration (like instance IPs, resource IDs).

Pass data between modules.

Help with debugging or automation (CI/CD pipelines, scripts, etc.).

**Locals**: A local is like a constant or internal variable. You define it once and reuse it multiple times.
**Why doesn't count work inside locals in Terraform?**
You cannot use count inside locals because locals are evaluated before resources are created, and count is a resource-level meta-argument that depends on runtime values.

**Terraform State**: Terraform state is a file (terraform.tfstate) that maps your configuration (code) to the actual infrastructure deployed.

It's how Terraform keeps track of what resources it created, their current settings, and metadata like IDs, attributes, and dependencies.

What Does the State File Contain?
All deployed resource information (IDs, names, IPs, etc.)

Dependencies between resources

Output values

Module structure

Metadata for performance optimization

**Remot State**:
What Is Remote State in Terraform?
By default, Terraform stores its state locally in a file called terraform.tfstate.

Remote state simply means storing that state file in a remote location, like AWS S3, Terraform Cloud, or Azure Blob Storage.

This enables multiple users and systems to share and access the same Terraform state safely, with features like:
Collaboration (shared state)
State locking
Versioning
Backup

**for_each loop**: In Terraform, a for_each loop is a powerful construct used to create multiple instances of a resource, module, or inline block based on a map or set of strings. It allows you to dynamically create infrastructure components without repeating the same block multiple times.

**Understanding each.key and each.value**

each.key — the key in the map or the item in a set.

each.value — the value associated with the key (in a map), or the item itself (in a set).

**Dynamic blocks** 
In Terraform, a dynamic block is used to dynamically generate nested blocks within a resource, based on a variable or other input data. This is especially helpful when you don’t know how many nested blocks you need ahead of time or want to reduce repetition in your configuration.





