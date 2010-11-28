require "rake/testtask"
require "rake/rdoctask"

desc 'Default: run unit tests.'
task :default => :test

desc 'Test the job_boss gem.'
Rake::TestTask.new(:test) do |t|
  t.libs << 'test'
  t.libs << 'test/app_root/app/jobs'

  t.pattern = 'test/**/*_test.rb'
  t.verbose = true
end

desc 'Generate documentation for the job_boss gem.'
Rake::RDocTask.new(:rdoc) do |rdoc|
  rdoc.rdoc_dir = 'rdoc'
  rdoc.title    = 'job_boss'
  rdoc.options << '--line-numbers' << '--inline-source'
  rdoc.rdoc_files.include('README')
  rdoc.rdoc_files.include('lib/**/*.rb')
end

namespace :job_boss do
  task :restart do
  end
end