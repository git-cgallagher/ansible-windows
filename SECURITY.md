# Security policy

## Reporting a vulnerability

Please report security issues **privately** through GitHub:
[Report a vulnerability](https://github.com/git-cgallagher/ansible-windows/security/advisories/new)
(the **Security** tab, then **Report a vulnerability**). Don't open a public issue for a security problem.

You can expect an acknowledgement within a week. This is a one-person project that isn't actively
developed, so fixes are best effort.

## Supported versions

Only the latest version on `main` gets fixes.

## Scope

Three Ansible modules for Windows hosts. Each one is written in PowerShell, with a Python file that
holds its documentation:

- `win_domain_site` creates, renames or removes Active Directory sites. Removing a site also removes
  the site links that include it, and it refuses while domain controllers are still in the site.
- `win_iis_mimetype` adds, changes or removes IIS MIME type mappings.
- `win_iis_mimetype_info` looks up IIS MIME type mappings and changes nothing.

The modules run on the managed Windows host with the privileges of Ansible's connection user. They
take no credentials of their own and open no network listeners.
