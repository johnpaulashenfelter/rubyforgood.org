# Ruby for Good New Website

## Welcome Contributors!

We love open source contributors! Feel free to take on open issues that are
marked `help wanted` or open new issues. Please comment on the issue to be
assigned to work on it as well as if you need more clarification. You can also
reach out to @meg-gutshall via the
[Ruby for Good Slack](https://join.slack.com/t/rubyforgood/shared_invite/zt-1kfeimohe-KL~~~6Lkof7G94_7Ojd_Hw).

When submitting your pull request, please submit to the `dev` branch as this is
our working branch.

## Getting Started

Fork this repository and clone it down to your computer. Create a new branch
that describes what you're working on. Then, run `bundle install` and
`npm install` to make sure you have all the gems and packages you need.

We built this site using Jekyll and it's hosted via GitHub pages. We used Ruby
with Bundler on the initial build and have since added NodeJS. We've included
dot files that support both rbenv (.ruby-version) and asdf (.tool-versions) ruby
managers for your convenience.

### Tool Versioning

- Ruby 2.7.1
- Bundler 2.1.4
- NodeJS 16.1.0
- NPM 7.22.0

### Problems with OpenSSL
If you get
```
linking shared-object rubyeventmachine.bundle
Undefined symbols for architecture arm64:
  "_SSL_get1_peer_certificate", referenced from:
      SslBox_t::GetPeerCert() in ssl.o
ld: symbol(s) not found for architecture arm64
clang: error: linker command failed with exit code 1 (use -v to see invocation)
make: *** [rubyeventmachine.bundle] Error 1

make failed, exit code 2
```
you might try
```
bundle config build.eventmachine --with-ssl-dir=/opt/homebrew/opt/openssl@3
```

## Useful Commands

To run the website locally, type `npm run test` in your terminal and navigate to
[http://127.0.0.1:4000/](http://127.0.0.1:4000/) to see the site in your
browser. A reload will be triggered every time you change the code in you
editor.

We have also implemented some tools that check the files for syntax issues and
autocorrect them whenever possible. These are called linters and they will
automatically check any files you have staged for a commit.

If you'd like to lint your code before you stage it, you can do so with the
following commands:

```bash
npm run lint        // Lints all files (i.e. corrects them syntactically for this codebase)
npm run lint:js     // Applies to JS files only
npm run lint:style  // Applies to CSS and SCSS files only
npm run lint:text   // Applies to Markdown files only
npm run prettier    // Formats and styles all files
```

You will not be able to successfully commit your work until all errors are
cleared.

## Going Deeper

Please see our newly created
[Ruby for Good Website Wiki](https://github.com/rubyforgood/rubyforgood.org/wiki)
to learn more about the project! Content will be continually added there. Also
keep an eye out for project boards in the future!
