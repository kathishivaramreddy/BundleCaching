# frozen_string_literal: true
source "https://rubygems.org"

gem 'fastlane'

# Since we use other actions from build-tools
# we need its dependencies
gem 'aws-sdk'
plugins_path = File.join(File.dirname(__FILE__), 'fastlane', 'Pluginfile')
eval(File.read(plugins_path), binding) if File.exist?(plugins_path)

gem 'xcode-install'

group :test, optional: true do
  # comments on Pull Request
  gem 'danger'
  gem 'danger-swiftlint', '0.11.1'
  gem 'danger-xcode_summary'
  gem 'danger-junit'
  gem 'xcpretty-json-formatter'
end

# Dependencies of developer.rb
group :development do
  gem 'xcodeproj'
  gem 'inifile'
end
