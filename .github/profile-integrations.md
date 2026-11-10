# Profile integrations

Reviewed on 2026-11-10 for [samuelpicado](https://github.com/samuelpicado).

The profile presents a third-year Information Systems Engineering student at Universidad Nacional de Costa Rica, Sede Regional Brunca, seeking internships and entry-level roles. Project descriptions retain the distinction between individual contributions and the team's wider technology stack.

## Decisions

| Tool | Status | Use and limits |
| --- | --- | --- |
| [GitHub Readme Streak Stats](https://github.com/DenverCoder1/github-readme-streak-stats) | Enabled | Daily contribution streak inside a disclosure below the projects. Uses the account's real contribution history, with the Costa Rica timezone; no excluded weekdays or altered counts. |
| [GitHub Profile Trophy](https://github.com/ryo-ma/github-profile-trophy) | Deferred | The documented public endpoint returned HTTP 402 with DEPLOYMENT_DISABLED during verification. No broken image was added. Its ranks are generated from GitHub counts, rather than professional certifications. |
| [GitHub Readme Activity Graph](https://github.com/Ashutosh00710/github-readme-activity-graph) | Deferred | The documented Vercel endpoint returned HTTP 402 with DEPLOYMENT_DISABLED. Summary Cards supplies a working contribution visualization. |
| [Metrics](https://github.com/lowlighter/metrics) | Deferred | The shared-instance image did not render in GitHub preview. The more reliable GitHub Action setup requires a personal access token; the built-in repository GITHUB_TOKEN cannot supply all required user data. |
| [WakaTime Readme Stats](https://github.com/athul/waka-readme) | Deferred | No verified WakaTime account, editor tracking, or read token was available for this update. Coding hours cannot be reconstructed from GitHub contributions. |
| [GitHub Profile Summary Cards](https://github.com/vn7n24fzkq/github-profile-summary-cards) | Enabled | One contribution overview with light/dark variants. No language percentages are presented as skill levels. Public statistics can omit private projects and some collaborative work. |
| [Komarev Profile Views Counter](https://github.com/antonkomarev/github-profile-views-counter) | Enabled | A small footer counter with no artificial base value. It counts image requests/page loads, including repeat visits, rather than unique people or recruiters. |
| [Shields.io](https://shields.io/badges/static-badge) | Enabled | Two factual badges: internship availability and web/desktop project focus. No invented seniority, certification, test coverage or proficiency scores. |
| [Skill Icons](https://github.com/tandpfun/skill-icons) | Enabled | Icons for technologies verified in the project review. The existing text table supplies the fuller technology list, including JavaFX, Oracle, SQLAlchemy and Alembic. |

The five enabled services rendered successfully through GitHub's image proxy in README preview. The profile retains its English presentation and project contribution descriptions. The portfolio link was also updated to the current repository name, Portfolio.

## Optional setup later

### Metrics

Follow the [official GitHub Action setup](https://github.com/lowlighter/metrics/blob/master/.github/readme/partials/documentation/setup/action.md).

Store the required personal token as an Actions repository secret, conventionally METRICS_TOKEN; never put a token in Markdown, YAML literals or image URLs. Public-only metrics can use a token with no additional scopes. The built-in GITHUB_TOKEN can be used separately for committing generated files where the selected action configuration supports it. A daily workflow should generate a repository SVG and publish only that file.

Keep private-repository and organization scopes disabled unless there is a specific reason to include that data. Review the generated SVG before embedding it. No Metrics token or inactive workflow was created as part of this update.

### WakaTime

1. Identify the correct WakaTime account and install its official plugin in the editor used for development.
2. Allow real coding activity to accumulate.
3. Use a WakaTime OAuth read token for the README integration. Current [WakaTime API documentation](https://wakatime.com/developers) says editor API keys are write-only.
4. Store that OAuth token in an Actions secret. The athul/waka-readme action retains the input/secret name WAKATIME_API_KEY even when its value is an OAuth token.
5. Configure a weekly activity section and publish only aggregate language/time data, without project names, machine names, locations or a detailed daily schedule.

An alternative public card requires the relevant WakaTime public-statistics settings. Choose what to expose before enabling them. No WakaTime account, secret or telemetry was configured as part of this update.

### Unavailable image services

Recheck the official Trophy and Activity Graph deployment status before embedding them. A personally hosted deployment is another option, but introduces hosting and credential maintenance. Do not substitute an unverified mirror or enter fabricated numbers.

## Maintenance

- Keep selected projects and individual contributions above statistics.
- Add an icon only after using the technology in a real project.
- Treat cached statistics as approximate activity summaries; do not relabel them as hours, unique visitors or professional expertise.
- If an image stops loading, remove it from the public README until a working replacement has been verified.
- Leave repository visibility and private-contribution sharing settings unchanged when refreshing the presentation.
