- [btp_subaccount_service_plan (Data Source)](https://registry.terraform.io/providers/SAP/btp/latest/docs/data-sources/subaccount_service_plan)

```terraform
data "btp_subaccount_service_plan" "auditlog_default" {
  subaccount_id = btp_subaccount.self.id
  name          = "default"
  offering_name = "auditlog-management"

  depends_on = [btp_subaccount_entitlement.auditlog_management_default]
}
```