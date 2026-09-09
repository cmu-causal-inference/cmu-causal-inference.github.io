# CMU Causal Inference Working Group

This repository contains the CMU Causal Inference Working Group website. It is plain HTML and CSS: no installation, build step, or database is required. Open `index.html` in your browser to view it locally.

Repository: [jungholeestat/cmu-causal-working-group](https://github.com/jungholeestat/cmu-causal-working-group).

After the one-time setup below, GitHub Pages will publish this repository at `https://jungholeestat.github.io/cmu-causal-working-group/`. The existing ChatGPT-hosted site is a separate deployment; edits here update GitHub Pages after setup, not the ChatGPT URL.

## Set up GitHub Pages once

1. Open this repository's [Settings → Pages](https://github.com/jungholeestat/cmu-causal-working-group/settings/pages).
2. Under **Build and deployment**, choose **Deploy from a branch** as the source.
3. Choose **main** and **/(root)**, then **Save**.
4. Wait for the initial deployment. GitHub will show the public website URL on that page. Later commits to `main` will publish updates automatically. Deployment progress appears in the repository's [Actions tab](https://github.com/jungholeestat/cmu-causal-working-group/actions).

The required files are already at the repository root. Keep `index.html`, `styles.css`, `favicon.svg`, and `.nojekyll` there. The empty `.nojekyll` file tells GitHub Pages to publish the static files directly. The repository is public and can use GitHub Pages on GitHub Free.

Publishing from a branch is documented in [GitHub Pages publishing settings](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

## Routine updates

Open [the editor for index.html](https://github.com/jungholeestat/cmu-causal-working-group/edit/main/index.html), make your changes, and choose **Commit changes** to save to `main`. Once Pages is enabled, GitHub publishes the updated site automatically. You can also use a local text editor and push your changes. See [GitHub's file editor guide](https://docs.github.com/en/repositories/working-with-files/managing-files/editing-files).

| What you want to change | Where to edit |
| --- | --- |
| Day, time, or room | The paragraph with `class="meeting-logistics"` in `index.html` |
| Discussant, title, or paper link | The appropriate row in the meeting table in `index.html` |
| Organizer names and links | The `organizer-list` in `index.html` |
| People link | The section with `id="people"` in `index.html` |
| Course or seminar links | The section with `id="resources"` in `index.html` |
| Colors, typography, or spacing | `styles.css` |
| Browser tab icon | `favicon.svg` |

Each schedule row contains three cells in this order: date, discussant, paper/topic. For example, this is the current introductory meeting:

```html
<tr>
  <td>09/08</td>
  <td>Patrick Kramer</td>
  <td>Introductory meeting</td>
</tr>
```

To add a meeting, duplicate one row inside `<tbody>`, then edit its three cells. Use an empty `<td></td>` for an unassigned discussant or topic. Keep the existing September-to-December rows unless you intend to revise the schedule.

A paper link goes inside the topic cell, for example:

```html
<td>
  <a href="https://arxiv.org/abs/2606.28200" target="_blank" rel="noopener noreferrer">
    Experimental design when N equals one
    <span class="sr-only"> (opens in a new tab)</span>
  </a>
</td>
```

Use `&amp;` for an ampersand and `&lt;` for a literal less-than sign in HTML text. The resource entries intentionally have no descriptive paragraphs.

## Preview and hand over

After an edit, open `index.html` locally to check the page, including the schedule and links. GitHub's commit history keeps the previous versions if you need to undo a change. When organizers change, give the next maintainer access to the repository and point them to this guide.

The site uses a red, white, and gray theme, a causal diagram, and a responsive layout. Asset paths are relative so it works at either a domain root or a GitHub Pages project URL.
