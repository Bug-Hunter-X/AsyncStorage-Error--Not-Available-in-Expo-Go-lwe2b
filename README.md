# AsyncStorage Error in Expo Go

This repository demonstrates a common issue encountered when using AsyncStorage within Expo Go.  The AsyncStorage API, which is typically used for local data persistence, may not function correctly in the Expo Go environment due to limitations in accessing the device's file system.

## Problem

The main problem is that `AsyncStorage.setItem()` and other AsyncStorage functions throw errors like `AsyncStorage: not available` when run inside an Expo Go instance. This prevents simple data persistence functionality.

## Solution

The solution involves using a different method of data persistence that is compatible with Expo Go.  This example uses MMKV, a high-performance key-value storage library.