# Expo Camera onBarCodeScanned Inconsistent Behavior

This repository demonstrates a bug related to the Expo `Camera` component's `onBarCodeScanned` prop.  The `onBarCodeScanned` callback function may not consistently fire, or may provide incomplete or incorrect barcode data.  This can lead to unreliable barcode scanning functionality in your application.

## Bug Description

The `onBarCodeScanned` function is intended to provide barcode data when a barcode is scanned. However, this is not functioning consistently.  The function may not be called at all, or it may be called with missing, incorrect, or duplicated data.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install the dependencies.
3. Run `expo start` to start the Expo development server.
4. Test the barcode scanning functionality using various barcodes. Observe that scans may be missed, or the returned data is not always correct.

## Solution

The provided solution attempts to address the inconsistency by adding a debounce mechanism to reduce the number of calls and ensure that only the most recent data is processed.  See `bugSolution.js` for the improved implementation. 
