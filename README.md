# get-previous-tag-action

This GitHub action allows you to get the previous tag from Git. In the case you use several different tags in a monorepo, filters can be applied to help you find a tag using a prefix or suffix.

## Inputs

By default, this action will fetch all available tags. You can choose to specify a tag pattern with the help of a prefix or a suffix.

- `prefix` *(optional)* - The prefix of the tag pattern
- `suffix` *(optional)* - The suffix of the tag pattern

## Outputs

- `previous-tag` - The previous tag

## Usage

### Get the previous tag

```yaml
- uses: younited/get-previous-tag-action@v1.0.0
```

### Get the previous tag with a tag pattern

Return a tag such as *RELEASE.2022-01-10.hotfix*:
```yaml
- uses: younited/get-previous-tag-action@v1.0.0
  with:
    prefix: RELEASE
    suffix: hotfix
```
