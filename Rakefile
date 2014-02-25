require 'puppetlabs_spec_helper/rake_tasks'
require 'puppet-lint/tasks/puppet-lint'

PuppetLint.configuration.fail_on_warnings = true
PuppetLint.configuration.send('disable_80chars')
# Ignore all upstream modules
PuppetLint.configuration.ignore_paths = ['spec/fixtures/modules/**/*.pp']

task(:default).clear
task :default => [:spec_prep, :spec_standalone, :lint]
