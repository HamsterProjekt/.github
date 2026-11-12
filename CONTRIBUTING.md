# Contributing

Thanks for helping to keep Hamster alive. HamsterProjekt is a fork of
[Project Hamster](https://github.com/projecthamster/hamster); see the
[organization page](https://github.com/HamsterProjekt) for why it exists.

## Reporting problems

Open an issue in the repository the problem is in:

- [hamster](https://github.com/HamsterProjekt/hamster/issues): the service, the
  GTK windows, storage (SQLite or Markdown).
- [hamster-kde](https://github.com/HamsterProjekt/hamster-kde/issues): the Plasma
  widget and the Qt windows.

Please say which version or commit you run, your distribution and desktop, and
which storage you use. If the bug also happens with upstream Hamster, mention
that.

## Sending changes

1. Fork the repository and make a branch.
2. Keep the change small and focused. One fix or feature per pull request.
3. Add or update tests where there are tests. For the Markdown backend:
   `python3 -m unittest tests.test_markdown_storage` in the `hamster` repository.
4. Sign off every commit (`git commit -s`); see
   [Developer Certificate of Origin](#developer-certificate-of-origin).
5. Explain in the pull request what changes and why.

Do not break compatibility without a good reason: SQLite stays the default,
and Hamster's data model and D-Bus methods and signals stay as they are.
The D-Bus, settings and application names are HamsterProjekt's own
(`io.github.HamsterProjekt.*`); use those, not upstream's `org.gnome.Hamster`.

## Developer Certificate of Origin

Every commit must be signed off. By signing off you certify the
[Developer Certificate of Origin](https://developercertificate.org/): that you
wrote the change, or otherwise have the right to submit it under the
repository's licence. The sign-off is a line at the end of the commit message,
with your real name and the e-mail of the commit's author:

    Signed-off-by: Your Name <you@example.org>

`git commit -s` (`--signoff`) adds it. The "DCO" check of a pull request fails
if a commit lacks it, and `main` only takes pull requests that pass. To sign
off the commits already on your branch:

```bash
git rebase --signoff main
```

```bash
git push --force-with-lease
```

Commits made in GitHub's web editor are signed off by GitHub.

## Upstream

Where a fix is useful to everyone, keep it separate from fork-specific work so
it can be offered to
[projecthamster/hamster](https://github.com/projecthamster/hamster) too.

## License

Contributions are licensed under the GNU GPL v3, like the rest of the project.
