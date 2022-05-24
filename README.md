# Demo with git next tag

> This is a demo repository to guide git users to use a git alias when
> presenting a demo.

## Setup git alias for the demo

```bash
git config --local alias.next '!f() { git checkout --detach $((`git describe --tags` + 1)) 2> /dev/null || echo "git next: the end of the demo"; }; f'
```

## Go to the demo initial tag

```bash
git chechout 0
```

## Navigate through sequential tags

```bash
git next
```
