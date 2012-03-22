require 'rubygems'
require 'rake'
require 'fileutils'

desc "Draft a new post"
task :new do
  puts "What should we call this post for now?"
  name = STDIN.gets.chomp
  FileUtils.touch("_posts/#{name}.md")

  open("_posts/#{name}.md", 'a') do |f|
    f.puts "---"
    f.puts "layout: post2"
    f.puts "title: \"#{name}\""
    f.puts "---"
  end
end


desc "Startup Jekyll"
task :start do
  sh "jekyll --server"
end

task :default => :start

