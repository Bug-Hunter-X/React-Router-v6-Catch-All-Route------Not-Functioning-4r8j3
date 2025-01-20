# React Router v6 Catch-All Route Issue

This repository demonstrates a problem with the catch-all route (`/*`) in React Router v6.  The issue is that the catch-all route does not correctly match any unmatched paths, preventing a 404 or equivalent from being displayed for undefined routes.

## Problem Description

Routes defined before the catch-all route work correctly.  However, if a user navigates to an undefined path, the catch-all route, intended to handle this case, is not triggered.  Instead, nothing is rendered, or some unexpected behavior occurs.

## Solution

The solution involves ensuring the catch-all route is placed correctly within the `Routes` component.  Also, ensuring that no other route can conflict with or take precedence over this route, which is usually the last route declared within the Routes component.