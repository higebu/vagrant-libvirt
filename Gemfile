source 'https://rubygems.org'

# Specify your gem's dependencies in vagrant-libvirt.gemspec
gemspec

group :development do
  # We depend on Vagrant for development, but we don't add it as a
  # gem dependency because we expect to be installed within the
  # Vagrant environment itself using `vagrant plugin`.
  if ENV['VAGRANT_VERSION']
    gem 'vagrant', :git => 'https://github.com/mitchellh/vagrant.git',
      tag: ENV['VAGRANT_VERSION']
  else
    gem 'vagrant', :git => 'https://github.com/mitchellh/vagrant.git'
  end

  gem 'vagrant-spec', :github => 'mitchellh/vagrant-spec',
    tag: ENV['VAGRANT_SPEC_VERSION'] || "24b7e3c07f3b89dec6c501a6c41c6ae971d593ca"

  gem 'pry'
end

gem 'coveralls', require: false
