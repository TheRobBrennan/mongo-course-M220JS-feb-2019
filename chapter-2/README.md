# Welcome
Chapter 2 of this course is focused on the user-facing backend. Specifically with a focus on basic aggregation, updates, deletes, and joins.

## Ticket: Paging
Modify `getMovies` in `mflix-js/src/dao/moviesDAO.js` so that `mflix-js/test/paging.test.js` passes. Verify by running:
```
$ npm test -t paging
```

## Ticket: Faceted Search
What is [faceted search](https://en.wikipedia.org/wiki/Faceted_search)?

By default, faceted searches are not enabled. To enable faceted search in the UI, open the `mflix-js/build/index.html` file and set `useFacets: true` in the mflix object.

Modify `facetedSearch` in `mflix-js/src/dao/moviesDAO.js` so that `mflix-js/test/facets.test.js` passes. Verify by running:
```
$ npm test -t facets
```

## Ticket: User Management
Modify `getUser`, `addUser`, `loginUser`, `logoutUser`, and `getUserSession` in `mflix-js/src/dao/usersDAO.js` so that `mflix-js/test/user-management.test.js` passes. Verify by running:
```
$ npm test -t user-management
```

## Ticket: Durable Writes
Modify `addUser` in `mflix-js/src/dao/usersDAO.js` to have durable writes - there are no tests for this ticket.

## Ticket: User Preferences
Modify `updatePreferences` in `mflix-js/src/dao/usersDAO.js` so that `mflix-js/test/user-preferences.test.js` passes. Verify by running:
```
$ npm test -t user-preferences
```

## Ticket: Get Comments
Modify `getMovieByID` in `mflix-js/src/dao/moviesDAO.js` so that `mflix-js/test/get-comments.test.js` passes. Verify by running:
```
$ npm test -t get-comments
```

## Ticket: Create/Update Comments
Modify `addComment` and `updateComment` in `mflix-js/src/dao/commentsDAO.js` so that `mflix-js/test/create-update-comments.test.js` passes. Verify by running:
```
$ npm test -t create-update-comments
```
