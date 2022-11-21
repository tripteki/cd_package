<h1 align="center">Convention</h1>

Trip Teknologi's Continuous Delivery and Continuous Deployment Package Convention.

Getting Started
---

How to use :

- You need to create a workflow in `.github/workflows/`.

    Sample file :

    ```
    name: Continuous Delivery and Continuous Deployment Package

    on: push

    jobs:
        cd:
            runs-on: ubuntu-latest
            steps:
                - name: cd
                  uses: tripteki/cd-package@1.0.0
                  with:
                    token: ${{ secrets.GITHUB_TOKEN }}
                    repotoken: <repository_token>
                    repouser: <repository_user>
                    repository: <repository_url>
                    language: <language_use>
                    artifact: <artifact>.<extension>
    ```

- `language` section value possibilities :<br />`php`, `js`, `py`.
- `repository` section value possibilities :<br />`https://packagist.org`, `https://registry.npmjs.org`, `https://upload.pypi.org/legacy/`, etc.
- `artifact` section value possibilities :<br />`composer.json`, `package.json`, `pyproject.toml`, etc.

Author
---

- Trip Teknologi ([@tripteki](https://linkedin.com/company/tripteki))
- Hasby Maulana ([@hsbmaulana](https://linkedin.com/in/hsbmaulana))
