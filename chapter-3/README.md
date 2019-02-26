# Welcome
Chapter 3 of this course is focused on the admin backend. Specifically on read concerns and bulk operations.

## Ticket: User Report
Modify `mostActiveCommenters` in `mflix-js/src/dao/commentsDAO.js` so that `mflix-js/test/user-report.test.js` passes. Verify by running:
```
$ npm test -t user-report
```

## Ticket: Migration
Modify `mflix-js/src/migrations/movie-last-updated-migration.js` so that `mflix-js/test/migration.test.js` passes. 

Run the migration from the `mflix-js` directory:
```
$ node src/migrations/movie-last-updated-migration.js
```

Verify by running:
```
$ npm test -t migration
```