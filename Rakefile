# frozen_string_literal: true

require "bundler/gem_tasks"
require "rake/testtask"

Rake::TestTask.new(:test) do |t|
  t.pattern = "test/**/*_test.rb"
end

require "rubocop/rake_task"

RuboCop::RakeTask.new do |task|
  task.requires << "rubocop-minitest"
end

task default: [:test, *(:rubocop if RUBY_ENGINE == "ruby")]
