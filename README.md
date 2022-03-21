Runs a generic Cloudify CLI command.

# Environment Variables

This Action uses the Cloudify Profile environment variables described in the official
Cloudify documentation (see [More Information](#more-information) below).

# Inputs

| Name | Description
|------|------------
| `command` | The CLI command to run.
| `set-output` | If set to `true`, then a GitHub output called `cli-output` is set with the CLI command's `stdout` contents.

## Notes

The string provided through the `command` input is provided as-is to the Cloudify CLI.

# Example

```yaml
jobs:
  test_job:
    steps:
      - name: Run some command
        uses: cloudify-cosmo/cli-action@v1.2
        with:
          command: "blueprints list"
```

# More Information

Refer to [Cloudify CLI Documentation](https://docs.cloudify.co/latest/cli/) for additional information about `cfy` command line.

Refer to [Cloudify CI/CD Integration](https://docs.cloudify.co/latest/working_with/integration/) for additional information about
Cloudify's integration with CI/CD tools.
