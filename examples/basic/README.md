# Basic Example

This example demonstrates basic usage of the ArvanCloud DNS module with common record types.

## What This Example Creates

- A record for root domain (`@`)
- A record for `www` subdomain
- A record for `api` subdomain
- MX record for email
- TXT records for SPF and domain verification

## Usage

1. Set your API key:

```bash
export TF_VAR_arvancloud_api_key="your-api-key"
```

1. Initialize and apply:

```bash
terraform init
terraform plan -var="domain=example.ir"
terraform apply -var="domain=example.ir"
```

## Inputs

| Name               | Description        | Type     | Default        |
| ------------------ | ------------------ | -------- | -------------- |
| arvancloud_api_key | ArvanCloud API key | `string` | n/a            |
| domain             | The domain name    | `string` | `"example.ir"` |

## Outputs

| Name         | Description                       |
| ------------ | --------------------------------- |
| record_ids   | Map of all DNS record IDs by type |
| record_count | Count of DNS records by type      |
