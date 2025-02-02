# React Native useRef Hook Object Update Issue

This repository demonstrates a common, yet subtle, bug in React Native when using the `useRef` hook with objects.  Modifying the object's properties directly does not trigger a re-render, leading to unexpected behavior.

## Bug Description
The `useRef` hook is intended for storing mutable values that don't cause re-renders. However, if you directly modify properties of an object stored in `useRef`, the changes are not reflected in the UI because the reference itself hasn't changed.

## Solution
To solve this, create a new object with the updated values, thereby triggering a re-render due to the change in the reference.