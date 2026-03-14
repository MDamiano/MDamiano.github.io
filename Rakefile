require 'html-proofer'

# rake test
desc "build and test website"

task :test do
  sh "bundle exec jekyll build"
  HTMLProofer.check_directory(
    "_site",
    disable_external: true,
    href_ignore: ['http://localhost:4000'],
    verbose: true
  ).run
end
