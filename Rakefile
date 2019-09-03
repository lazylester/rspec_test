# Add your own tasks in files placed in lib/tasks ending in .rake,
# for example lib/tasks/capistrano.rake, and they will automatically be available to Rake.

require "rspec/core/rake_task"
require_relative 'config/application'

Rails.application.load_tasks


RSpec::Core::RakeTask.new(:spec)

desc "run the entire test suite except request specs"
task :default => :spec
RSpec::Core::RakeTask.module_eval do
  def pattern
    "spec/models/**/*_spec.rb"
  end
end


