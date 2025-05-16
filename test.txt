terraform {
  required_version = "~> 1.9"
  required_providers {
    azurerm = {
      source  = "hashicorp/azurerm"
      version = "~> 4.0"
    }
  }
  backend "azurerm" {}
}


provider "azurerm" {
  features {}
}

# add new comment to test CI
resource "azurerm_resource_group" "example" {
  name     = "testbdorg1223"
  location = "Southeast Asia"
}