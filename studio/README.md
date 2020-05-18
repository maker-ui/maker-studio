Key to success:

Studio w/ local data store handles theme object / variants, site options, layouts
-- has rehydrate function to get essential theme / options data from DB at dev command
-- saves all changes asynchronously to DB while saving edits in local state
-- fetches other data from DB and acts as shell
-- visually shows you schema for DB models
-- Lets you add, edit, delete records for models
-- -- Lets you search / query with GUI
-- pings localhost:8000 to rebuild when it detects a relevant change

Plugin is a dev dependency that only runs locally and fetches data from localhost:5000 to let you build
pages visually.
-- opens stream to localhost:5000 for data changes
-- adds builder UI overlay to whole project when in dev mode
-- parses 'visual builder' output into MDX file and saves to disk or sends to 5000 API and forces a redevelop with incremental data
-- implements incremental builds

-- has App analytics dashboards
-- uses i18n

Look into service workers and passing messages through iframes OR use AWS notification api

Need CLI to add configurations / files to your project example:

Common APIs with config packages
maker-ui add config-aws-amplify --auth
maker-ui add config-algolia
maker-ui add config-stripe
maker-ui add config-okta
...etc

2 apps connected to AWS amplify + 1 gatsby plugin that adds site functionality during development
Instead of iframe, maker ui builds clone of it in real time. Like sanity preview but way better
They both use same theme variants in shared directory ?
