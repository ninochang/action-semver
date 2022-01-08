# Hello world docker action

This action prints "Hello World" or "Hello" + the name of a person to greet to the log.

## Inputs

## `input`

**Required** The verion. Default `${{ github.ref_name }}`.

## `pattern`

**Required** Semver pattern. Default `^v?(?P<major>[0-9]+)(?:\.(?P<minor>[0-9]+))?(?:\.(?P<patch>[0-9]+))?(?:\-(?P<prerelease>[\w-]+))?(?:\+(?P<build>[\w-]+))?$`.

## Outputs

## `semver`

## Example usage
```yaml
  - name: Setup - Semver
    id: semver
    uses: swaglive/action-semver@v1
    
  - name: Configure
    id: config
    run: |
      echo ${{ steps.semver.outputs.version }}
```
