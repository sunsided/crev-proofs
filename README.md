# crev-proofs

This is a [proof repository] for [crev]. See the [Getting Started] document for information about how to use [cargo-crev].

## Using proof repositories

Use `cargo crev fetch all` to periodically update all downloaded Proof Repositories.

To register my reviews, use

```bash
cargo crev repo fetch url https://github.com/sunsided/crev-proofs
```

To optionally _trust_ my reviews, use

```bash
cargo crev trust https://github.com/sunsided/crev-proofs
```


## TL;DR on `cargo crev` usage

```bash
# setup
cargo install cargo-crev
cargo crev trust --level high https://github.com/dpc/crev-proofs
cargo crev repo fetch all

# verify
cargo crev verify --show-all

# review
cargo crev open $crate_name
cargo crev review $crate_name

# share reviews
# Fork this: https://github.com/crev-dev/crev-proofs/fork
cargo crev id set-url https://github.com/$your_github_username/crev-proofs
cargo crev publish

# get more reviews
cargo crev id query all
cargo crev trust # insert other people's URLs or Ids here

# review just the parts that changed since
cargo crev crate diff $crate_name | less
cargo crev review --diff $previous_version -- $crate_name
```

[Getting Started]: https://github.com/crev-dev/cargo-crev/blob/main/cargo-crev/src/doc/getting_started.md
[cargo-crev]: https://github.com/crev-dev/cargo-crev
[crev]: https://github.com/crev-dev/crev/
[proof repository]: https://github.com/crev-dev/crev/wiki/Proof-Repository
