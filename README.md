# Epic Dependency Planner — policy site

Standalone policy review site for Aer Studios Limited. Contact: devs@aerstudios.co.uk.

The `docs/` directory is a complete, buildless static site. It contains no application code, Jira records, credentials, external assets, scripts, trackers or forms. GitHub Pages itself logs request information under GitHub’s privacy statement.

## Review status

These pages are clearly marked **Review draft — not yet adopted as AER policy**. Publication provides reviewable links; it does not represent company approval or establish legal adequacy. Do not treat the draft URLs as adopted policies for Forge distribution until AER has confirmed the content.

Before adopting the documents, confirm:

- AER’s controller/processor responsibilities and the relationship to staff, contractor and client privacy information.
- The proposed lawful basis and any required legitimate-interests assessment for assignee reporting.
- Retention periods or criteria for source Jira information, exports, support messages and relevant supplier records.
- Supplier processing locations, agreements and any applicable international-transfer safeguards.
- The contact address, internal-use scope and compatibility with existing agreements.

The technical description was checked against the app source on 16 October 2026. It describes client-side analysis, current-assignee attribution, browser-local preferences, optional exports and no separate application data store. It does not claim that Atlassian or GitHub collect no operational data, or that all data remains in the UK/EU.

To adopt approved wording, replace the review blocks and draft status consistently on all three HTML pages, set an actual effective date, and update the description. Keep a record of the approved text and date in version control. The review blocks deliberately contain unresolved points rather than inventing company policies.

## Local preview

From this repository:

```sh
python3 -m http.server 4185 --bind 127.0.0.1 --directory docs
```

Open http://127.0.0.1:4185/. No Node.js packages or build step are needed. The site also works under a GitHub project subpath because its internal links and stylesheet URLs are relative.

## GitHub Pages

In this repository’s **Settings → Pages**, choose **Deploy from a branch**, branch **main**, folder **/docs**, and save. The `.nojekyll` file keeps the HTML and CSS unchanged. No custom Actions workflow or additional credential is needed.

After deployment, the standard URLs are:

- https://aerstudios.github.io/epic-dependency-planner-policies/privacy.html
- https://aerstudios.github.io/epic-dependency-planner-policies/terms.html

Use the URLs reported by GitHub Pages if an organisation-level custom domain changes the address. Verify both pages return HTTP 200 while signed out. After the policies are adopted, use the privacy and terms URLs in the Forge Developer Console’s Distribution settings.

This repository contains policy pages only. Its public accessibility does not change access to the Jira app or Jira tickets.

## References

- [Forge distribution](https://developer.atlassian.com/platform/forge/distribute-your-apps/)
- [GitHub Pages setup](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)
- [GitHub Pages privacy](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages)
- [ICO lawful basis guidance](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/lawful-basis/a-guide-to-lawful-basis/)
