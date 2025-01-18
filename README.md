# ansible-role-mastodon

Ansible role for setting up Mastodon with Docker Compose, Traefik and PostgreSQL on the host

## Variables

### Docker

- `mastodon_network` [default: `mastodon`]
- `mastodon_files_proxy_traefik_matching_rule` [required]: Example: `"Host(``files.example.com``)"`
- `mastodon_streaming_image` [default: `tootsuite/mastodon-streaming:v4.3.3`]
- `mastodon_web_image` [default: `tootsuite/mastodon:v4.3.3`]

### PostgreSQL

- `mastodon_db_host` [default: `host.docker.internal`]
- `mastodon_db_user` [default: `mastodon`]
- `mastodon_db_name` [default: `mastodon`]
- `mastodon_db_password` [required]
- `mastodon_db_port` [default: `5432`]

### Email

- `mastodon_smtp_server` [default: `host.docker.internal`]
- `mastodon_smtp_auth_method` [default: `none`]
- `mastodon_smtp_openssl_verify_mode` [default: `none`]
- `mastodon_smtp_port` [default: `587`]
- `mastodon_smtp_login` [default: empty]
- `mastodon_smtp_password`[default: empty]
- `mastodon_smtp_from_address` [required]: Example: `"Mastodon <mastodon@example.com>"`

### Object storage

- `mastodon_aws_access_key_id` [required]
- `mastodon_aws_secret_access_key` [required]
- `mastodon_s3_alias_host` [required]
- `mastodon_s3_bucket` [required]
- `mastodon_s3_endpoint` [required]
- `mastodon_s3_hostname` [required]
- `mastodon_s3_region` [required]
- `mastodon_s3_protocol` [required]

### Mastodon

- `mastodon_active_record_encryption_deterministic_key` [required]
- `mastodon_active_record_encryption_key_derivation_salt` [required]
- `mastodon_active_record_encryption_primary_key` [required]
- `mastodon_web_domain` [required]
- `mastodon_local_domain` [required]
- `mastodon_secret_key_base` [required]
- `mastodon_otp_secret` [required]
- `mastodon_vapid_public_key` [required]
- `mastodon_vapid_private_key` [required]
- `mastodon_deepl_api_key` [required]
