require 'rake'


# Attempt to load Rails if available
begin
  require File.expand_path('config/environment', __dir__)
  require 'active_record/railtie'
  Rails.application.load_tasks
rescue LoadError
  puts "⚠️ Warning: Rails environment not found. Ensure this is a Rails project and you're running inside the correct directory."
end

# Define database tasks
namespace :db do
  desc "Create database"
  task :create do
    sh "bundle exec rails db:create"
  end

  desc "Load test schema"
  task :test_load do
    sh "bundle exec rails db:test:prepare"
  end
end

# Default task (optional)
task default: [:db_create, :db_test_load]
