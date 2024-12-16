---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "sonarqube_portfolio Data Source - terraform-provider-sonarqube"
subcategory: ""
description: |-
  Use this data source to get a Sonarqube portfolio resource
---

# sonarqube_portfolio (Data Source)

Use this data source to get a Sonarqube portfolio resource

## Example Usage

```terraform
data "sonarqube_portfolio" "portfolio" {
  key = "portfolio-key"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `key` (String) The key of the portfolio

### Read-Only

- `branch` (String) Which branch is analyzed
- `description` (String) Description of the portfolio
- `id` (String) The ID of this resource.
- `name` (String) Name of the portfolio
- `qualifier` (String) `VW` (portfolios always have this qualifier)
- `regexp` (String) The regular expression used to populate the portfolio. Only active when `selection_mode` is `REGEXP`
- `selection_mode` (String) How the Portfolio is populated. Possible values are `NONE`, `MANUAL`, `TAGS`, `REGEXP` or `REST`. [See docs](https://docs.sonarqube.org/9.8/project-administration/managing-portfolios/#populating-portfolios) for how Portfolio population works
- `tags` (List of String) The list of tags used to populate the Portfolio. Only active when `selection_mode` is `TAGS`
- `visibility` (String) Portfolio visibility