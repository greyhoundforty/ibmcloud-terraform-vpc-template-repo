# Template repo for IBM Cloud Terraform projects

## pre-commit hooks:

 - terraform_fmt: Syntax checking for Terraform
 - detect_secrets: Ensure we don't commit anything sensitive
 - terraform_docs: Generate a INFO.md for the Terraform resources 
 
## detect secrets: 

To add new Secrets to the existing Baseline, run the following command:

```shell
$ detect-secrets scan --baseline .secrets.baseline
```

This will rescan your codebase, and:

- Update/upgrade your baseline to be compatible with the latest version,
- Add any new secrets it finds to your baseline, and remove any secrets no longer in your codebase
- Preserve any labelled secrets you have.
