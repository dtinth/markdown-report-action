# markdown-report-action
Attachs a Markdown report your GitHub Actions build. This action uses the Checks API, which is less noisy and more tidy than using comments.

[This report will appear as another job in GitHub Actions UI:](https://github.com/dtinth/markdown-report-action/runs/4339917802?check_suite_focus=true)

![run](https://user-images.githubusercontent.com/193136/143671955-586c13d6-c505-4b10-aab9-6f9343f02ebe.png)

[In a pull request, the report will appear as neutral status check:](https://github.com/dtinth/markdown-report-action/pull/1/checks?check_run_id=4339917802)

![checks](https://user-images.githubusercontent.com/193136/143671954-776ea75c-f369-4677-9b7e-d5c8918b9b5d.png)

## Usage

```yaml
# First, create a Markdown file containing the report.
- run: echo 'Content here. You *can* use Markdown.' | tee /tmp/report.md

# Then use this action to generate the report.
- uses: dtinth/markdown-report-action@v1
  with:
    name: Report name
    title: Report title here
    body-file: /tmp/report.md
```