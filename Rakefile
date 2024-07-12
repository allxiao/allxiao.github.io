task :draft, [:title] do |t, args|
  call_jekyll_compose("draft", args.title)
end

task :post, [:title] do |t, args|
  call_jekyll_compose("post", args.title)
end

task :page, [:title] do |t, args|
  call_jekyll_compose("page", args.title)
end

task :publish, [:file] do |t, args|
  file = args.file.downcase.gsub(/\s+/, "-")
  if not file.end_with?(".md")
    file = "#{file}.md"
  end
  draft = File.join("_drafts", file)
  if File.exist?(draft)
    file = draft
  end
  sh "bundle exec jekyll publish \"#{file}\""
end

def call_jekyll_compose(command, title)
  if not title.include?(" ")
    title = title.split(/-+/).map(&:capitalize).join(' ')
  end
  sh "bundle exec jekyll #{command} \"#{title}\""
end
