# learning_programming

A new Flutter project of beers catalog.

## Getting Started

I this project we going to create a beer catalog app, when we can se list of beers, search and watch detail.

For technical side the project have to use:

* Riverpod
* GetIt
* Dio
* freezed

In that way the organization of folders is tah one:

core
  - api (api abstraction get, post and api implementation)
  - di (GetIt locator module)
features
  - beers
    - di (module of GetIt with repository and datasource definitions)
    - domain
      - entity (models like Beer)
      - use_case (use case focus on beers list)
      - repository (abstract class with beers functions get, insert, etc...)
    - data
      - datasource (remote and local datasources)
      - repository (repository implemetation define in domain)
    - presentation
      - screen (screen widget with components to use)
      - widget (custom widget like button, textfield with custom params)
      - component (component with multiple widgets and provider connection)
      - provider (provider of information to get beers, search, etc...)
- beer
    - di (module of GetIt with repository and datasource definitions)
    - domain
      - entity (empty)
      - use_case (use case focus on beer detail)
      - repository (abstract class with beer detail function)
    - data
      - datasource (remote and local datasources)
      - repository (repository implemetation define in domain)
    - presentation
      - screen (screen widget with components to use)
      - widget (custom widget like button, textfield with custom params)
      - component (component with multiple widgets and provider connection)
      - provider (provider of information to get beer)

## API Definition

- Get beers: https://api.punkapi.com/v2/beers
- Search beer by name: https://api.punkapi.com/v2/beers?beer_name={beer name}
- Get beet: https://api.punkapi.com/v2/beers/{id beer}
