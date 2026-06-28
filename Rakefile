require 'html-proofer'

# rake test
desc "build and test website"

task :test do
  sh "bundle exec jekyll build"
  abort "AGENTS.md was published to _site/AGENTS.md" if File.exist?("_site/AGENTS.md")
  HTMLProofer.check_directory(
    "_site",
    disable_external: true,
    href_ignore: ['http://localhost:4000'],
    verbose: true
  ).run
end
