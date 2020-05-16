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
