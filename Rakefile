require 'rake'
require 'active_record'
require 'rake/testtask'
require 'dotenv'

# Load environment variables from .env if available
Dotenv.load if File.exist?('.env')

# Load Rails tasks if using Rails
begin
  require File.expand_path('config/application', __dir__)
  require 'rake'
  Rails.application.load_tasks
rescue LoadError
  puts "Rails environment not found. Ensure you're in a Rails project."
end

namespace :db do
  desc "Create database"
  task :create do
    sh "bundle exec rake db:create"
  end

  desc "Load test schema"
  task :test_load do
    sh "bundle exec rake db:test:load"
  end
end

# Define a default task (e.g., run tests)
task default: [:db_create, :db_test_load]
