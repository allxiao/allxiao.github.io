# Note It

Codebase that compiles to the site [Note It][noteit].

## Prepare Environment

Run bundle to install all the required RubyGems dependencies.

## Compose New Posts

1. Create a draft post
   ```ruby
   bundle exec jekyll draft "My New Post Title"
   ```
   This creates the file `_drafts/my-new-post-title.md`.
2. Write the post content in the newly created file, and update the front matters.
3. Post the draft
   ```ruby
   bundle exec jekyll post _drafts/my-new-post-title.md
   ```
   This will move the post from `_drafts` to `_posts`, rename it with a date prefix, and also update the `date` field
   in the front matters.
4. Commit and push to the upstream.

## Acknowledgements

This site is based on the [Chirpy Jekyll Theme][chirpy].

## License

This work is published under [MIT][mit] License.

[noteit]: https://allxiao.github.io
[chirpy]: https://github.com/cotes2020/jekyll-theme-chirpy
[mit]: https://github.com/cotes2020/chirpy-starter/blob/master/LICENSE
