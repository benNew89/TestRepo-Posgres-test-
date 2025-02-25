source 'https://rubygems.org'

ruby '3.0.5'

gem 'rails', '~> 7.0' # Rails framework
gem 'pg', '~> 1.4' # PostgreSQL adapter
gem 'dotenv', '~> 2.8' # Load environment variables
gem 'rake', '~> 13.0' # Task management
gem 'rspec-rails', '~> 6.0' # Testing framework for Rails
gem 'bundler', '~> 2.3' # Dependency manager

group :development, :test do
  gem 'rubocop', '~> 1.59' # Linter for Ruby
  gem 'factory_bot_rails', '~> 6.2' # Test data setup
end

group :test do
  gem 'database_cleaner-active_record', '~> 2.0' # Clean DB between tests
end
