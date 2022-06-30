# cpan-02packages-writer

Generate CPAN index from your local directory.

# Usage

```console
❯ cat cpanfile
requires 'File::pushd';

❯ cpm install
DONE install File-pushd-1.016
1 distribution installed.

❯ cpan-02packages-writer ./local > index.txt
---> loading ./local/lib/perl5/darwin-2level/.meta/File-pushd-1.016/install.json
```

And later, you will always reproduce your local directory with the `index.txt`:

```console
❯ cpm install --resolver 02packages,index.txt,https://cpan.metacpan.org
DONE install File-pushd-1.016  <-------- SAME VERSION!
1 distribution installed.
```

# Install

```console
❯ cpm install -g https://github.com/skaji/cpan-02packages-writer.git
```

# License

MIT
