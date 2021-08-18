This is the website for ShinjiwLab at LTI, CMU. The theme is adapted from al-folio.

This README is written for lab members to update related pages and information. For all the updates, there should be some exisitng examples already. Please follow their style to make our page consistent.

## Local Test
Before the PR, please test the website locally (especially when you have some stylish modifications).

Assuming you have [Ruby](https://www.ruby-lang.org/en/downloads/) and [Bundler](https://bundler.io/) installed on your system (*hint: for ease of managing ruby gems, consider using [rbenv](https://github.com/rbenv/rbenv)*), first [fork](https://guides.github.com/activities/forking/) the theme from `github.com:alshedivat/al-folio` to `github.com:<your-username>/<your-repo-name>` and do the following:

```bash
$ git clone git@github.com:<your-username>/<your-repo-name>.git
$ cd <your-repo-name>
$ bundle install
$ bundle exec jekyll serve
```

Now, feel free to customize the theme however you like (don't forget to change the name!).
After you are done, **commit** your final changes.

## Member and co-author information

- Photo profile: directly upload to `assets/img/photo-{name}.jpg`
- Member entry: add an entry to present your photo, name, homepage (if any) at `pages/members.md`


## Bibliography

Your publications page is generated automatically from your BibTex bibliography.
Edit `_bibliography/papers.bib` would be fine.

Some fields in the BibTeX are reserved for specific representations.
- `abbr`: serves for the topic label. You may choose from `ASR`, `TTS`, `SE`, `ST`, or other abbreviations that stand for the topic of the paper
- `abbr_publisher`: serves for the label of places of publishing. It should be the abbreviation of journal or conference name, like `Interspeech`, `ICASSP`, `NIPS`, `ACL`.
- `html`: serves for the original page of this paper (e.g., ISCA archive, aclweb, or IEEE library)
- `pdf`: serves for the pdf version of this paper. If the pdf is open-available through the official release (e.g., aclweb or isca-archive), it should be directly linked to that. Otherwise, the arxiv link to the pdf would be fine.
- `code`: the link to its open-source code (if available)
- `arxiv`: the arxiv ID (e.g., 1804.00015) of the paper. It should <strong>NOT</strong> be the arxiv link.
- `selected`: default `false`. It would show up on the front page if setting with `true`. A paper that has more than 100 citations would be selected or the other paper that is approved by Shinji before the setting.

<details><summary><strong>Author annotation:</strong></summary>

In publications, the author entry for yourself is identified by string `scholar:last_name` and string array `scholar:first_name` in `_config.yml`:
```
scholar:
  last_name: Einstein
  first_name: [Albert, A.]
```
If the entry matches the last name and one form of the first name, it will be underlined.
Keep meta-information about your co-authors in `_data/coauthors.yml`, and Jekyll will insert links to their webpages automatically.
The co-author data format in `_data/coauthors.yml` is as follows,
```
"Adams":
  - firstname: ["Edwin", "E.", "E. P.", "Edwin Plimpton"]
    url: https://en.wikipedia.org/wiki/Edwin_Plimpton_Adams

"Podolsky":
  - firstname: ["Boris", "B.", "B. Y.", "Boris Yakovlevich"]
    url: https://en.wikipedia.org/wiki/Boris_Podolsky

"Rosen":
  - firstname: ["Nathan", "N."]
    url: https://en.wikipedia.org/wiki/Nathan_Rosen

"Bach":
  - firstname: ["Johann Sebastian", "J. S."]
    url: https://en.wikipedia.org/wiki/Johann_Sebastian_Bach

  - firstname: ["Carl Philipp Emanuel", "C. P. E."]
    url: https://en.wikipedia.org/wiki/Carl_Philipp_Emanuel_Bach
```
If the entry matches one of the combinations of the last names and the first names, it will be highlighted and linked to the url provided.

</details>

## Open-source
Please follow the existing style when updating this part. 

## News
Add news directly to `_news` with a new MD file. We can also have a long-version (please check the al-folio repo for details)
