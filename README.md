# Intelligence per Watt research website

Static website for the Intelligence per Watt research program, including
OpenJarvis, the Intelligence Control Plane, and Joules-to-GDP.

## Preview locally

Open `index.html` directly in a browser. The site has no package installation,
build step, remote JavaScript dependencies, or server requirement.

For an HTTP preview, run this from the repository directory in a terminal that
permits local servers, then visit <http://localhost:8000>:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Stop the server with Ctrl-C. Opening the page or running this command does not
publish anything.

## Source layout

- `index.html`: page content, inline CSS, and hash-based section navigation.
- `img/people/`: contributor portraits; people without verified images
  use initials in the HTML. See [portrait sources](img/people/SOURCES.md).
- `img/sponsors/`: sponsor assets.
- `CNAME`: the existing public domain configuration.

The panels are Vision, Agenda, Papers + Code, Talks & Media, Blog, Related,
People, and Sponsors. Project anchors are `#intelligence-per-watt`,
`#openjarvis`, `#icp`, and `#joules-to-gdp`; related papers also have
`#minions`, `#archon`, and `#weaver`. Keep these stable when editing.
Navigation supports direct links, reload, and Back/Forward. With JavaScript
disabled, all content remains readable in document order.

## Maintaining content

Edit `index.html` directly; there is no content generation or build pipeline.
For a paper, update its card, full ordered author list, verified contribution
marks, description, publication status, and resource links together. Show
“Preprint” or the accepted conference and year, such as “NeurIPS 2026”.
Keep project cards in
Papers + Code; preserve the original Vision page without a project overview.
Only add code/data/reproduction links once they work publicly.
The ICP PDF and its link are omitted pending paper publication; retain the project
card. Its code release and the Joules-to-GDP code/data buttons are deferred.

For a person, check the existing roster first. Use verified affiliations and
homepages, or plain text and initials when those resources are unavailable.
Do not infer current job titles from a paper affiliation.
Group students by degree level. Keep cards consistent: photo, name/profile
link, and a simple role such as Undergraduate or PhD Student. Do not display
university names or project tags on People cards.

For talks/media, use the host or publisher as the primary source where possible.
Keep entries in reverse chronological order. Preserve month-only dates when
no exact day is known, and add recordings/slides only when a real link exists.
Distinguish event dates from recording publication dates. Separate interviews
and direct coverage from broader industry perspectives; the latter do not
imply an author appearance or endorsement of the research.

When reviewing changes, check desktop and mobile layouts, keyboard focus,
200% zoom, project hashes, Back/Forward, the blog open/back flow, and no-JavaScript
reading. Verify local assets and external destinations.
Check the document title, social descriptions, and displayed update date.

## Publication

GitHub Pages publishes the root of `main` to the existing domain. Review
changes in a pull request before merging. Preserve `CNAME`; no new hosting
service is required. The ICP PDF is intentionally absent from both this
change and its public commit history.
