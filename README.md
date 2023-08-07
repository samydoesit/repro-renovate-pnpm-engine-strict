# Repro Renovate PNPM Engine Strict

I recently noted that Renovatebot switched to using pnpm as its package manager. However, when running the config-validator of Renovatebot with our local package.json's engines constraint for pnpm, the validation fails.

## Steps to reproduce
Install: `pnpm install`
Run validateRenovate: `pnpm run validateRenovate`

Output:
```bash
 ERR_PNPM_UNSUPPORTED_ENGINE  Unsupported environment (bad pnpm and/or Node.js version)

This error happened while installing a direct dependency of /tmp/pnpm/store/v3/tmp/dlx-7145

Your pnpm version is incompatible with "registry.npmjs.org/renovate/36.34.0".

Expected version: ^8.6.11
Got: 8.6.5
```
