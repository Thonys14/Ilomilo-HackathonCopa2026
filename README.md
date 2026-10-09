# Ilomilo-HackathonCopa2026
Repository created for the Hackathon-Cup2026 event

## instrucciones de paso 1 Iac 1201

Solicitando una instancia de Cloud Shell.Succeeded. 
Connecting terminal...

Welcome to Azure Cloud Shell

Type "az" to use Azure CLI
Type "help" to learn about Cloud Shell

Your Cloud Shell session will be ephemeral so no files or system changes will persist beyond your current session.
missel [ ~ ]$ git clone https://github.com/HackathonLabsNetworks/2026-Veraguas-Microsoft-IaC.git
Cloning into '2026-Veraguas-Microsoft-IaC'...
remote: Enumerating objects: 8, done.
remote: Counting objects: 100% (8/8), done.
remote: Compressing objects: 100% (6/6), done.
remote: Total 8 (delta 0), reused 8 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (8/8), done.
missel [ ~ ]$ cd develop-veraguas-iac/hackathon-team/
bash: cd: develop-veraguas-iac/hackathon-team/: No such file or directory
missel [ ~ ]$ cd develop-veraguas-iac/hackathon-team/
bash: cd: develop-veraguas-iac/hackathon-team/: No such file or directory
missel [ ~ ]$ cd 2026-Veraguas-Microsoft-IaC
missel [ ~/2026-Veraguas-Microsoft-IaC ]$ ./deploy.ps1 -TeamId 25
bash: ./deploy.ps1: Permission denied
missel [ ~/2026-Veraguas-Microsoft-IaC ]$ chmod u+x deploy.ps1
missel [ ~/2026-Veraguas-Microsoft-IaC ]$ ./deploy.ps1 -TeamId 25

MOTD: Share your feedback and help us improve Cloud Shell: https://aka.ms/cloudshell/feedback

VERBOSE: Authenticating to Azure ...
WARNING: You're using Az version 16.3.0. The latest version of Az is 16.4.0. Upgrade your Az modules using the following commands:
  Update-PSResource Az -WhatIf    -- Simulate updating your Az modules.
  Update-PSResource Az            -- Update your Az modules.
Validando el grupo del usuario autenticado...
Membresia validada: grupo-copa-25.
Inicializando Terraform...
Initializing the backend...

Initializing provider plugins...
- Finding hashicorp/azurerm versions matching "~> 4.0"...
- Installing hashicorp/azurerm v4.81.0...
- Installed hashicorp/azurerm v4.81.0 (signed by HashiCorp)

Terraform has created a lock file .terraform.lock.hcl to record the provider
selections it made above. Include this file in your version control repository
so that Terraform can guarantee to make the same selections by default when
you run "terraform init" in the future.

Terraform has been successfully initialized!

You may now begin working with Terraform. Try running "terraform plan" to see
any changes that are required for your infrastructure. All Terraform commands
should now work.

If you ever set or change modules or backend configuration for Terraform,
rerun this command to reinitialize your working directory. If you forget, other
commands will detect it and remind you to do so if necessary.
Seleccionando el estado del equipo 25...
Created and switched to workspace "team-25"!

You're now on a new, empty workspace. Workspaces isolate their state,
so if you run "terraform plan" Terraform will not see any existing state
for this configuration.
El workspace aun no tiene estado; se comprobaran recursos existentes en Azure.
El recurso hackathon-copa-2026-team-25-law no existe; Terraform lo creara.
El recurso hackathon-copa-2026-team-25-appi no existe; Terraform lo creara.
El recurso hackathon-copa-2026-team-25-frontend no existe; Terraform lo creara.
El recurso hackathon-copa-2026-team-25-api no existe; Terraform lo creara.
Generando el plan de Terraform...
data.azurerm_resource_group.team: Reading...
data.azurerm_service_plan.plan_backend: Reading...
data.azurerm_service_plan.plan_frontend: Reading...
data.azurerm_resource_group.team: Read complete after 0s [id=/subscriptions/d2dda6e6-81c9-42a9-86c8-55c8e8552a95/resourceGroups/rg-team-25]
data.azurerm_service_plan.plan_backend: Read complete after 0s [id=/subscriptions/d2dda6e6-81c9-42a9-86c8-55c8e8552a95/resourceGroups/rg-hackathon-shared/providers/Microsoft.Web/serverFarms/plan-back-13]
data.azurerm_service_plan.plan_frontend: Read complete after 0s [id=/subscriptions/d2dda6e6-81c9-42a9-86c8-55c8e8552a95/resourceGroups/rg-hackathon-shared/providers/Microsoft.Web/serverFarms/plan-front-13]

Terraform used the selected providers to generate the following execution plan. Resource actions are indicated with the following symbols:
  + create

Terraform will perform the following actions:

  # azurerm_application_insights.team_app_insights will be created
  + resource "azurerm_application_insights" "team_app_insights" {
      + app_id                                = (known after apply)
      + application_type                      = "web"
      + connection_string                     = (sensitive value)
      + daily_data_cap_in_gb                  = 100
      + daily_data_cap_notifications_disabled = (known after apply)
      + daily_data_cap_notifications_enabled  = (known after apply)
      + disable_ip_masking                    = (known after apply)
      + force_customer_storage_for_profiler   = false
      + id                                    = (known after apply)
      + instrumentation_key                   = (sensitive value)
      + internet_ingestion_enabled            = true
      + internet_query_enabled                = true
      + ip_masking_enabled                    = (known after apply)
      + local_authentication_disabled         = (known after apply)
      + local_authentication_enabled          = (known after apply)
      + location                              = "centralus"
      + name                                  = "hackathon-copa-2026-team-25-appi"
      + resource_group_name                   = "rg-team-25"
      + retention_in_days                     = 90
      + sampling_percentage                   = 100
      + workspace_id                          = (known after apply)
    }

  # azurerm_linux_web_app.backend-app will be created
  + resource "azurerm_linux_web_app" "backend-app" {
      + app_settings                                   = (known after apply)
      + client_affinity_enabled                        = false
      + client_certificate_enabled                     = false
      + client_certificate_mode                        = "Required"
      + custom_domain_verification_id                  = (sensitive value)
      + default_hostname                               = (known after apply)
      + enabled                                        = true
      + ftp_publish_basic_authentication_enabled       = true
      + hosting_environment_id                         = (known after apply)
      + https_only                                     = false
      + id                                             = (known after apply)
      + key_vault_reference_identity_id                = (known after apply)
      + kind                                           = (known after apply)
      + location                                       = "centralus"
      + name                                           = "hackathon-copa-2026-team-25-api"
      + outbound_ip_address_list                       = (known after apply)
      + outbound_ip_addresses                          = (known after apply)
      + possible_outbound_ip_address_list              = (known after apply)
      + possible_outbound_ip_addresses                 = (known after apply)
      + public_network_access_enabled                  = true
      + resource_group_name                            = "rg-team-25"
      + service_plan_id                                = "/subscriptions/d2dda6e6-81c9-42a9-86c8-55c8e8552a95/resourceGroups/rg-hackathon-shared/providers/Microsoft.Web/serverFarms/plan-back-13"
      + site_credential                                = (sensitive value)
      + virtual_network_backup_restore_enabled         = false
      + vnet_image_pull_enabled                        = false
      + webdeploy_publish_basic_authentication_enabled = true
      + zip_deploy_file                                = (known after apply)

      + site_config {
          + always_on                               = true
          + container_registry_use_managed_identity = false
          + default_documents                       = (known after apply)
          + detailed_error_logging_enabled          = (known after apply)
          + ftps_state                              = "Disabled"
          + http2_enabled                           = false
          + ip_restriction_default_action           = "Allow"
          + linux_fx_version                        = (known after apply)
          + load_balancing_mode                     = "LeastRequests"
          + local_mysql_enabled                     = false
          + managed_pipeline_mode                   = "Integrated"
          + minimum_tls_version                     = "1.2"
          + remote_debugging_enabled                = false
          + remote_debugging_version                = (known after apply)
          + scm_ip_restriction_default_action       = "Allow"
          + scm_minimum_tls_version                 = "1.2"
          + scm_type                                = (known after apply)
          + scm_use_main_ip_restriction             = false
          + use_32_bit_worker                       = true
          + vnet_route_all_enabled                  = false
          + websockets_enabled                      = false
          + worker_count                            = (known after apply)

          + application_stack {
              + dotnet_version = "10.0"
            }
        }
    }

  # azurerm_linux_web_app.frontend-app will be created
  + resource "azurerm_linux_web_app" "frontend-app" {
      + app_settings                                   = (known after apply)
      + client_affinity_enabled                        = false
      + client_certificate_enabled                     = false
      + client_certificate_mode                        = "Required"
      + custom_domain_verification_id                  = (sensitive value)
      + default_hostname                               = (known after apply)
      + enabled                                        = true
      + ftp_publish_basic_authentication_enabled       = true
      + hosting_environment_id                         = (known after apply)
      + https_only                                     = false
      + id                                             = (known after apply)
      + key_vault_reference_identity_id                = (known after apply)
      + kind                                           = (known after apply)
      + location                                       = "centralus"
      + name                                           = "hackathon-copa-2026-team-25-frontend"
      + outbound_ip_address_list                       = (known after apply)
      + outbound_ip_addresses                          = (known after apply)
      + possible_outbound_ip_address_list              = (known after apply)
      + possible_outbound_ip_addresses                 = (known after apply)
      + public_network_access_enabled                  = true
      + resource_group_name                            = "rg-team-25"
      + service_plan_id                                = "/subscriptions/d2dda6e6-81c9-42a9-86c8-55c8e8552a95/resourceGroups/rg-hackathon-shared/providers/Microsoft.Web/serverFarms/plan-front-13"
      + site_credential                                = (sensitive value)
      + virtual_network_backup_restore_enabled         = false
      + vnet_image_pull_enabled                        = false
      + webdeploy_publish_basic_authentication_enabled = true
      + zip_deploy_file                                = (known after apply)

      + site_config {
          + always_on                               = true
          + container_registry_use_managed_identity = false
          + default_documents                       = (known after apply)
          + detailed_error_logging_enabled          = (known after apply)
          + ftps_state                              = "Disabled"
          + http2_enabled                           = false
          + ip_restriction_default_action           = "Allow"
          + linux_fx_version                        = (known after apply)
          + load_balancing_mode                     = "LeastRequests"
          + local_mysql_enabled                     = false
          + managed_pipeline_mode                   = "Integrated"
          + minimum_tls_version                     = "1.2"
          + remote_debugging_enabled                = false
          + remote_debugging_version                = (known after apply)
          + scm_ip_restriction_default_action       = "Allow"
          + scm_minimum_tls_version                 = "1.2"
          + scm_type                                = (known after apply)
          + scm_use_main_ip_restriction             = false
          + use_32_bit_worker                       = true
          + vnet_route_all_enabled                  = false
          + websockets_enabled                      = false
          + worker_count                            = (known after apply)

          + application_stack {
              + node_version = "24-lts"
            }
        }
    }

  # azurerm_log_analytics_workspace.team will be created
  + resource "azurerm_log_analytics_workspace" "team" {
      + allow_resource_only_permissions = true
      + daily_quota_gb                  = -1
      + id                              = (known after apply)
      + internet_ingestion_enabled      = true
      + internet_query_enabled          = true
      + local_authentication_disabled   = (known after apply)
      + local_authentication_enabled    = true
      + location                        = "centralus"
      + name                            = "hackathon-copa-2026-team-25-law"
      + primary_shared_key              = (sensitive value)
      + resource_group_name             = "rg-team-25"
      + retention_in_days               = 30
      + secondary_shared_key            = (sensitive value)
      + sku                             = "PerGB2018"
      + workspace_id                    = (known after apply)
    }

Plan: 4 to add, 0 to change, 0 to destroy.

───────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────

Saved the plan to: /home/missel/2026-Veraguas-Microsoft-IaC/.terraform/team-25.tfplan

To perform exactly these actions, run the following command to apply:
    terraform apply "/home/missel/2026-Veraguas-Microsoft-IaC/.terraform/team-25.tfplan"
Aplicando el plan de Terraform...
azurerm_log_analytics_workspace.team: Creating...
azurerm_log_analytics_workspace.team: Still creating... [00m10s elapsed]
azurerm_log_analytics_workspace.team: Still creating... [00m20s elapsed]
azurerm_log_analytics_workspace.team: Still creating... [00m30s elapsed]
azurerm_log_analytics_workspace.team: Still creating... [00m40s elapsed]
azurerm_log_analytics_workspace.team: Creation complete after 43s [id=/subscriptions/d2dda6e6-81c9-42a9-86c8-55c8e8552a95/resourceGroups/rg-team-25/providers/Microsoft.OperationalInsights/workspaces/hackathon-copa-2026-team-25-law]
azurerm_application_insights.team_app_insights: Creating...
azurerm_application_insights.team_app_insights: Creation complete after 3s [id=/subscriptions/d2dda6e6-81c9-42a9-86c8-55c8e8552a95/resourceGroups/rg-team-25/providers/Microsoft.Insights/components/hackathon-copa-2026-team-25-appi]
azurerm_linux_web_app.backend-app: Creating...
azurerm_linux_web_app.frontend-app: Creating...
azurerm_linux_web_app.frontend-app: Still creating... [00m10s elapsed]
azurerm_linux_web_app.backend-app: Still creating... [00m10s elapsed]
azurerm_linux_web_app.frontend-app: Still creating... [00m20s elapsed]
azurerm_linux_web_app.backend-app: Still creating... [00m20s elapsed]
azurerm_linux_web_app.frontend-app: Still creating... [00m30s elapsed]
azurerm_linux_web_app.backend-app: Still creating... [00m30s elapsed]
azurerm_linux_web_app.backend-app: Still creating... [00m40s elapsed]
azurerm_linux_web_app.frontend-app: Still creating... [00m40s elapsed]
azurerm_linux_web_app.frontend-app: Creation complete after 48s [id=/subscriptions/d2dda6e6-81c9-42a9-86c8-55c8e8552a95/resourceGroups/rg-team-25/providers/Microsoft.Web/sites/hackathon-copa-2026-team-25-frontend]
azurerm_linux_web_app.backend-app: Creation complete after 50s [id=/subscriptions/d2dda6e6-81c9-42a9-86c8-55c8e8552a95/resourceGroups/rg-team-25/providers/Microsoft.Web/sites/hackathon-copa-2026-team-25-api]

Apply complete! Resources: 4 added, 0 changed, 0 destroyed.
Infraestructura del equipo 25 desplegada correctamente.
missel [ ~/2026-Veraguas-Microsoft-IaC ]$ 
