# The Datapimp Gem

# Taking the HTTP out of Common Rest Patterns 

Current User. Parameters. Resources.

All of the players are aware of the user that is making the query, the
user that is running the command, the user who is viewing a resource

## GET index and show: FilterContext's

- ActiveRecord complex queries
- Query as a specific user: permissions / security / scoping
- Server caching: query cache keys based on the maximum updated_at and count for given params
- HTTP Request Caching: ETags + Last Modified headers
- Metadata for inspection + documentation generation

## PUT / POST / DELETE: ApplicationCommand's

- Mutations Gem.
- Bring some order to activerecord lifecycle callbacks
- Declarative DSL 
- Metadata for inspection + documentation generation

## Views: ApplicationSerializer's

- ActiveModel Serializers
- Documentation DSL
- Metadata for inspection + documentation generation

## API Documentation & Integration Tests

- rspec_api_documentation gem
- plan: take advantage of metadata defined above to auto-generate
  documentation with the ability to pass expectation blocks as pass /
  fail indicators
