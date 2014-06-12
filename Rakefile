desc "Generates combined schema for all schemas in ./schemas"
task :combine do
  `bundle exec prmd combine --meta meta.json schemata/ > schema.json`
end

desc "Generates documentation for combined schema"
task :doc do
  `bundle exec prmd doc --prepend overview.md schema.json > ./schema.md`
end

task :default => [:combine, :doc]