# Note It

Codebase that compiles to the site [Note It][noteit].

## Setup

1. Install all the RubyGems dependencies

   ```console
   $ bundle
   ```

2. Start local development server

   ```console
   $ rake s
   ```

## Compose New Posts

1. Create a draft post

   ```ruby
   rake draft["My New Post Title"]
   ```

   This creates the file `_drafts/my-new-post-title.md`.
2. Write the post content in the newly created file, and update the front matters.
3. Post the draft

   ```ruby
   rake post[my-new-post-title]
   ```

   This will move the post from `_drafts` to `_posts`, rename it with a date prefix, and also update the `date` field
   in the front matters.
4. Commit and push to the upstream.

## License

This work is published under [MIT][mit] License. It is based on [chirpy-starter][chirpy] and the license is included
in the end of the license file.

[noteit]: https://allxiao.github.io
[chirpy]: https://github.com/cotes2020/chirpy-starter
[mit]: LICENSE
