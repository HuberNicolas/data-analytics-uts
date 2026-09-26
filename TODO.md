# TODO

Open tasks before the repository is made public. See also [Known issues](README.md#known-issues). The full original
state is kept in the private repository `data-analytics-uts-archive`.

## 1. Clean-up

- [x] Remove the week 1 and week 2 demo notebooks written by the teaching staff
- [x] Add the AT2 notebook from `python-data-processing-uts` (without the course data)
- [x] Rename the week folders to `week-NN` and fix the data paths in `notebooks/week-03.ipynb`
- [x] Check that `poetry install` works with the original lock file and that the week 3 notebook runs

## 2. Environment

- [ ] Decide whether to add TensorFlow and tqdm for AT2 (Poetry would pull current versions of their dependencies)
- [ ] Remove the unused `lineapy` dependency, or leave it as it was

## 3. Before publishing

- [x] Add the MIT license
- [x] Credit the datasets (UCI, Gaia)
- [x] Rewrite the history: old email addresses to `nicolas.huber.dev@gmail.com`, removed UTS material out of all
      commits
- [ ] Force-push `main`
- [ ] Set the GitHub description and topics
- [ ] Set the repository to public
