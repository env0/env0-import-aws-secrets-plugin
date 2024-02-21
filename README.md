# Jenv0 Import AWS Secrets Plugin
This plugin will fetch output values from AWS Secrets Manager and insert them as terraform and/or environment variables.

# Example Usage

```
version: 2

deploy:
  steps:
    setupVariables:
      after:
        - name: Kosta Plugin
          use: https://github.com/Constantine19/env0-json-plugin
          inputs:
            secret_prefix: kosta_ssm
            secret_aws_region: us-east-1
        - name: Debug
          run: export
```