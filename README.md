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

