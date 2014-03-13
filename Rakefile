desc "Generates combined schema for all schemas in ./schemas"
task :combine do
  `prmd combine ./schemas > ./1x-api-schema.json`
end

desc "Generates documentation for combined schema"
task :doc do
  `prmd doc ./1x-api-schema.json > ./docs/1x-api.md`
end
