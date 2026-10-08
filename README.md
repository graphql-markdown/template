> [!WARNING]
> **This template is deprecated and the repository is archived.** It is no longer updated and pins `@graphql-markdown/docusaurus` 1.34.0.
>
> To start a new GraphQL-Markdown site with Docusaurus, use the scaffolder instead:
>
> ```shell
> npm create graphql-markdown-docs@latest -- --framework docusaurus
> ```
>
> The scaffolder creates the same Docusaurus site, kept in sync with every GraphQL-Markdown release and tested in CI. It uses a bundled example schema by default. To use your own schema, pass `--schema <path-or-url>` and the scaffolder adds the matching loader. To reproduce this template's setup, use `--schema https://countries.trevorblades.com/graphql`.
>
> **Already created a site from this template?** You don't need to migrate. Update `@graphql-markdown/docusaurus` to the latest version to get new features and fixes.
>
> More: [Get started](https://graphql-markdown.dev/docs/get-started) · [create-graphql-markdown-docs](https://github.com/graphql-markdown/graphql-markdown/tree/main/packages/create-graphql-markdown-docs)


# GraphQL-Markdown template

Docusaurus template for [GraphQL-Markdown](https://graphql-markdown.dev).

## Quick start

### 1. Install

```shell
npm init docusaurus my-website https://github.com/graphql-markdown/template.git
```

### 2. Configure

Update settings in `.graphqlrc` (see [documentation](https://graphql-markdown.dev/docs/configuration#graphql-config)).

```yaml
schema: 'https://countries.trevorblades.com/graphql'
extensions:
  graphql-markdown:
    baseURL: '.'
    homepage: 'static/index.md'
    loaders:
      UrlLoader: 
        module: '@graphql-tools/url-loader'
        options:
          method: 'POST'
    docOptions:
      frontMatter:
        pagination_next: null
        pagination_prev: null
    printTypeOptions:
      deprecated: 'group'
```

### 3. Generate

```shell
npm run doc
```

### 4. Start

```shell
npm start
```
