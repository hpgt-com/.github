# .github

Felles filer for repoene i hpgt-com. Retningslinjene står i [hpgt-com/guidelines](https://github.com/hpgt-com/guidelines).

| Hva | Innhold |
|---|---|
| `profile/README.md` | Forsiden til organisasjonen på GitHub |
| `SECURITY.md`, `CONTRIBUTING.md`, `PULL_REQUEST_TEMPLATE.md`, `ISSUE_TEMPLATE/` | Standardfiler for repoer som ikke har sine egne |
| `workflow-templates/` | Arbeidsflytmaler under Actions → New workflow |
| `.github/workflows/` | Sjekkene for dette repoet: `workflow-security`, `dependency-review`, CodeQL, Scorecard og automatisk merge av Dependabot |

Dependabot oppdaterer arbeidsflytene i `.github/workflows/`, men ikke malene i `workflow-templates/`. Når Dependabot
oppdaterer en action her, oppdateres de samme SHA-ene i malene i samme pull request.
