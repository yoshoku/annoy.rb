require 'bundler/gem_tasks'
require 'rspec/core/rake_task'

RSpec::Core::RakeTask.new(:spec)

require 'rake/extensiontask'

task :build => :compile

Rake::ExtensionTask.new('annoyext') do |ext|
  ext.ext_dir = 'ext/annoy'
  ext.lib_dir = 'lib/annoy'
end

task :default => [:clobber, :compile, :spec]
