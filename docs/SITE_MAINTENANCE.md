# Maintaining Ruijie Xu's academic website

The site's research focus is **data generation for embodied AI**, spanning controllable 3D scenes, simulation-based multimodal data, and safety-oriented benchmarks.

## Publications

Edit `_bibliography/papers.bib` for both the publications page and homepage selections.

- `note` is a short, always-visible overview. Keep it to one or two sentences; the complete abstract belongs in `abstract`.
- `additional_info` holds acceptance status, CCF classification, or equal-contribution information. Start with `&nbsp;· ` so Markdown rendering preserves the space separating it from the venue.
- `selected = {true}` includes a paper on the homepage.
- `code` links to an associated public repository. Describe any pending implementation release in the summary and on the Open Source page.
- Presentation-only `note` content is excluded from the downloadable/displayed BibTeX through `filtered_bibtex_keywords` in `_config.yml`.

Only label a paper with a venue after acceptance is confirmed. Preprints keep the arXiv label. CCF classifications apply to venues, not to preprints or research topics.

Sources checked on October 30, 2026:

- [Exemplar2VQA arXiv record](https://arxiv.org/abs/2609.37655): accepted to NeurIPS 2026; complete author order and code link.
- [CCF artificial intelligence directory](https://www.ccf.org.cn/Academic_Evaluation/AI/): NeurIPS is category A.
- [CCF computer graphics and multimedia directory](https://www.ccf.org.cn/Academic_Evaluation/CGAndMT/): The Visual Computer is category C.

Update `_data/cv.yml`, the alternate JSON Resume at `assets/json/resume.json`, and announcements under `_news/` when a publication's status changes. The date on an announcement is its posting date; it need not be the acceptance date.

## Projects and repositories

Research overviews live in `_projects/`. Use explicit `/projects/<slug>/` permalinks for links shared elsewhere on the site.

Maintain repository order in `_data/repositories.yml` under `github_repos`, with matching metadata in `repository_details`. Each entry should explain its purpose, relationship to the site owner, and current release status. The Open Source page renders text and links without depending on third-party image services. Optional statistics can be enabled with `show_stats`.

The JointEdit3D [public README](https://github.com/xinnan-zhu/JointEdit3D) currently announces SceneEdit3D-15K and schedules implementation release for paper acceptance. Do not describe inference or training code as released until this changes.

Keep repository links in project page bodies. The current theme's project card already wraps the card in a link; adding a `github` frontmatter link produces nested anchors in that theme version.

## Images and template resources

`assets/img/publication_preview/exemplar2vqa.png` is the QA-generation pipeline figure from the [Exemplar2VQA repository](https://github.com/yingjiayu12/Exemplar2VQA/blob/main/docs/assets/pipeline_track2.png), by Jiayu Ying and collaborators, reused under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Attribution also appears on the project's page.

The homepage biography and CV use the existing avatar. The Open Graph preview uses the existing MUSE figure. Other upstream example assets are retained for documentation and test references; they are not personal research outputs.

Agent instructions, test sources, dependency requirements, and the upstream Einstein CV PDF are excluded from the published site through `_config.yml`.

## Verification

Run formatting and starter contract checks, then build with Jekyll. Check the homepage, publications, projects, Open Source, and CV on desktop and mobile. In particular, verify publication summaries, author expansion, abstract toggles, internal links, and long repository names.

The upstream visual suite includes demo blog and teaching pages that this personal site does not contain. Select relevant page checks or use site-specific smoke checks rather than assuming every template fixture exists.

Runtime layouts remain owned by the theme gems. These content changes require no local template overrides.
