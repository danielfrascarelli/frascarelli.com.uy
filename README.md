# frascarelli.com.uy

Static sites, one folder per domain. Hosted on AWS (S3 + CloudFront + Route53).

| Folder | Domain |
|---|---|
| `daniel.frascarelli.com.uy/` | https://daniel.frascarelli.com.uy |

Deploy a site:

```sh
aws s3 sync daniel.frascarelli.com.uy/ s3://<bucket> --delete
aws cloudfront create-invalidation --distribution-id <id> --paths '/*'
```
