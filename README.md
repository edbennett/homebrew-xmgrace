# Minimal Homebrew tap for xmgrace with PDF support

This repository contains the two formulae necessary to let Homebrew install Grace with PDF support.

* The `pdflib-lite` formula was removed from Homebrew for being non-free. The formula is taken directly from [the original version in homebrew-core](https://github.com/fanninpm/homebrew-core/blob/d73f8d6456a5235e8e6198981bbfc22ad341fec2/Formula/pdflib-lite.rb)
* The `grace` formula has been modified to enable the PDF driver to be built. This is based on [the version in homebrew-core as of 2022-07-24](https://github.com/fanninpm/homebrew-core/blob/3758e3fba3b1efb5e61a86ddbfa259a1ef337c94/Formula/grace.rb), with the `configure` arguments changed and the references to bottles removed.

Note that this will not work on an Apple Silicon install of Homebrew. This is because `pdflib-lite` was written pre-Apple Silicon, and makes 
assumptions about architectures supported by macOS. (It does, for example, include PowerPC support!) Fixing that issue is outside the scope 
of this repository, so for now at least you'll need to [install an x86 version of Homebrew](https://medium.com/mkdir-awesome/how-to-install-x86-64-homebrew-packages-on-apple-m1-macbook-54ba295230f).
