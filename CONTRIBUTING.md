# Contribution Guidelines

Thanks for helping keep this list useful. Please read this before opening a pull request.

## What belongs here

An entry should be something a Mastra developer would be glad to find:

- Official documentation, reference pages, and integrations.
- Templates, starters, and example applications that run.
- Open-source projects built on Mastra.
- Courses, workshops, articles, and videos that teach something specific.
- Tools, adapters, and libraries that extend Mastra.

## What does not belong here

- Projects that only mention Mastra in passing.
- Empty repositories, abandoned forks, or unreleased work.
- Paid products with no free tier and no technical detail.
- Self-promotion without substance, or duplicate entries.
- Link shorteners, affiliate links, and tracking parameters.

## Quality bar

Before submitting, check that the project:

- Has a README that explains what it does and how to run it.
- Has seen a commit in the last twelve months, or is clearly complete.
- Works with a currently supported version of Mastra.
- Uses HTTPS links that resolve without a redirect chain.

## Formatting

Every entry follows one format:

```markdown
- [Name](https://example.com) - Short description that ends with a period.
```

Rules the linter enforces:

- One entry per line, in a bulleted list.
- A single space, a hyphen, and a single space between the link and the description.
- Descriptions start with a capital letter and end with a period.
- Keep descriptions to one sentence. Say what the thing does, not why it is great.
- No marketing language, no emoji, no trailing whitespace.
- Do not put backticks or bold text inside the link name.
- Add new entries in a position that keeps the section readable. Sections are roughly grouped by relevance, not alphabetized.

## Adding a section

If your entry does not fit an existing section, add a new one and add a matching line to the Contents list. The Contents list and the section headings must stay in sync or the linter will fail.

## Submitting

1. Fork the repository and create a branch.
2. Make your change in `README.md`.
3. Run `npm install && npm test` to check formatting and links.
4. Open a pull request that explains what you added and why it is useful.

One pull request per addition where practical. It makes review and revert easier.

## Removing an entry

Open an issue or a pull request if a link is dead, a project is archived, or something no longer works with current Mastra. Removals are as welcome as additions.
