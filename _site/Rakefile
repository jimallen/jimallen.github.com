require 'rubygems'
require 'rake'
require 'fileutils'
require "date"

desc "Draft a new post"
task :new do
  puts "What should we call this post for now?"
  name = STDIN.gets.chomp
  puts "What Category?"
  category = STDIN.gets.chomp
  filename = "#{DateTime.now.year}-#{DateTime.now.month}-#{DateTime.now.day}-#{name}"
  FileUtils.touch("_posts/#{filename}.markdown")

  open("_posts/#{filename}.markdown", 'a') do |f|
    f.puts "---"
    f.puts "layout: post2"
    f.puts "title: \"#{name}\""
    f.puts "Category: \"#{category}\""
    f.puts "year: #{DateTime.now.year}"
    f.puts "month: #{DateTime.now.month}"
    f.puts "day: #{DateTime.now.day}"
    f.puts "published: false"
    f.puts "tags: blog_post"
    f.puts "---"
  end
end


desc "Startup Jekyll"
task :start do
  sh "jekyll --server"
end

task :default => :start

