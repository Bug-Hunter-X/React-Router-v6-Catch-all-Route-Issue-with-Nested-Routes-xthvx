# React Router v6 Catch-all Route Issue

This repository demonstrates a problem with the catch-all route (`/*`) in React Router v6 when nested routes are present. The catch-all route unexpectedly intercepts requests, even when a more specific nested route should match.

## Problem

The issue arises when a catch-all route (`/*`) is defined alongside nested routes.  Regardless of the URL, the catch-all route always seems to take precedence. The expected behavior is for the catch-all route to only handle unmatched paths.

## Solution

The solution involves carefully ordering routes.  By ensuring more specific routes are placed *before* the catch-all route, React Router can correctly match the appropriate component.