# Unhandled Route in React Router v6
This example demonstrates an uncommon bug in React Router v6 related to missing route handling.  The application lacks a catch-all route (`/*`) to handle paths that don't match any explicitly defined routes.  This can lead to unexpected behavior, particularly when navigating to non-existent paths.

## Bug
The initial `App.js` component uses `react-router-dom` v6 but omits a route to handle any path that doesn't match `/` or `/about`.  If a user navigates to an undefined path, React Router won't render anything. This can lead to blank screens or unexpected behavior.

## Solution
The `AppSolution.js` demonstrates the solution.  By adding a `Route` component with `path="*"`, any path that doesn't match a previous route is handled. This helps to improve user experience by providing a fallback route, or error page. 