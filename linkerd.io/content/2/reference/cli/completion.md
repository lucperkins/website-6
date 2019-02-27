+++
date = "2019-02-17T12:00:00-07:00"
title = "completion"
+++

The Linkerd CLI supports shell command
[auto-completion](https://en.wikipedia.org/wiki/Command-line_completion)
for both [Bash](#bash) and [zsh](#zsh) via the `completion` command.

## Bash

### Linux

For Bash versions 4.0 and later:

```bash
source <(linkerd completion bash)
```

For Bash versions 3.2 and earlier:

```bash
source /dev/stdin <<< "$(linkerd completion bash)"
```

### macOS

For Bash versions 4.0 and later:

```bash
brew install bash-completion@2
linkerd completion bash > $(brew --prefix)/etc/bash_completion.d/linkerd
```

For Bash versions 3.2 and earlier:

```bash
brew install bash-completion # ensure you have bash-completion 1.3+
linkerd completion bash > $(brew --prefix)/etc/bash_completion.d/linkerd
```

## zsh

```bash
source <(linkerd completion zsh)
```

### Oh My Zsh

If you're using the [Oh My Zsh](https://ohmyz.sh/) framework for macOS:

```bash
linkerd completion zsh > "${fpath[1]}/_linkerd"
```
