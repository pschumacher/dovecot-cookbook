# encoding: UTF-8
# -*- mode: ruby -*-
# vi: set ft=ruby :

source 'https://rubygems.org'

chef_version = ENV.key?('CHEF_VERSION') ? ENV['CHEF_VERSION'] : nil

group :doc do
  gem 'yard', '~> 0.8'
end

group :test do
  gem 'rake'
  gem 'berkshelf', '~> 4.0'
end

group :style do
  gem 'foodcritic', '~> 4.0.0'
  gem 'rubocop', '~> 0.36.0'
end

group :unit do
  gem 'chef', chef_version unless chef_version.nil?
  gem 'simplecov', '~> 0.9'
  gem 'should_not', '~> 1.1'
  gem 'chefspec', '~> 4.1'
end

group :integration do
  gem 'test-kitchen', '~> 1.2'
end

group :integration_docker do
  gem 'kitchen-docker', '~> 2.1'
end

group :integration_vagrant do
  gem 'vagrant-wrapper', '~> 2.0'
  gem 'kitchen-vagrant', '~> 0.10'
end

group :integration_cloud do
  gem 'kitchen-ec2', '~> 0.8'
  gem 'kitchen-digitalocean', '~> 0.9'
end

group :guard do
  gem 'guard', '~> 2.6'
  gem 'guard-foodcritic', '~> 1.0'
  gem 'guard-rubocop', '~> 1.1'
  gem 'guard-rspec', '~> 4.3'
  # Temporary disabled: Error is: cannot load such file -- guard/kitchen
  # gem 'guard-kitchen', '~> 0.0'
end

group :travis do
  gem 'coveralls', '~> 0.7', require: false
end
