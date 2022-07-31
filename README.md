<p align="center">
  <a href="" rel="noopener">
 <img src="./docs/logo.png" alt="ghcoin logo"></a>
</p>

<h3 align="center">ghcoin-cli</h3>
<h4 align="center">The companion to the totally practical currency ghcoin</h3>

`ghcoin` is the CLI for [ghcoin](https://github.com/plamorg/ghcoin), creating a
more-intuitive, faster interface for performing transactions on the repository.

## Prerequisites

- Python3
- Git
- GitHub CLI Tool
- Curl

## Usage

```
Control your transactions from the command line.

USAGE:
    ghcoin <command> <subcommand>

CORE COMMANDS:
    send <recipient> <amount>  Send the specified recipient the given amount
    balance [user ...]         Retrieve the balance of self or the specified user(s)
    list                       List valid recipients
    register                   Register self onto the ledger
    use-node                   Change the target remote ledger
    help, -h, --help           List this help message
```

Make sure that you are logged in to the GitHub CLI tool. Run `gh auth status` to
confirm. If you are not logged in, run `gh auth login`.

If you are not yet on the ledger, run `ghcoin register`.

Transactions are performed with `ghcoin send <recipient> <amount>`. For example:
`ghcoin send priime0 10`. The recipient must be on the ledger to receive it. The
amount must be a non-negative integer, and must be less than or equal to your
balance.
