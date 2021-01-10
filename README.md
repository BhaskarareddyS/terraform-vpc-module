
Terraform-vpc-module---

module "vpc" {
  source = "git@github.com:bhargavimandala/terraform-vpc-module.git"
  product = var.product
  environment = var.environment
  vpc_cidr = var.cidr_range
  tenancy = "default"
  public_subnets = var.public_subnet #example--  "10.0.1.0,10.0.2.0"
  private_subnets = var.private_subnet #example -- "10.0.3.0/24,10.0.4.0/24"
  availability_zones = "eu-west-2a,eu-west-2b"

}
