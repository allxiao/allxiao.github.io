%i(draft page post).each do |type|
  desc "Create a new #{type.to_s.capitalize}"
  task type, [:title] do |t, args|
    title = args.title
    if not title.include?(" ")
      title = title.split(/-+/).map(&:capitalize).join(' ')
    end
    sh "bundle exec jekyll #{type} \"#{title}\""
  end
end

desc "Publish a draft"
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

desc "Start the development server"
task :serve do
  sh "bundle exec jekyll serve"
end

task :s => :serve
task :dev => :serve
