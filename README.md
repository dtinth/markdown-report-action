# markdown-report-action
Attachs some Markdown report to the GitHub Actions build.

## Usage

```yaml
# First, create a Markdown file containing the report.
- run: echo 'Content here. You *can* use Markdown.' | tee /tmp/report.md

# Then use this action to generate the report.
- uses: dtinth/markdown-report-action@v1
  with:
    name: Report name
    title: Report title
    body-file: /tmp/report.md
```
