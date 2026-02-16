# Overview

## Overview
Describe the feature, its use case, and its value proposition.

## Configuration & Installation
Document setup, prerequisites, environment variables, and dependencies.

## API Documentation

### Product Status
- `productId`: string - Unique identifier for the product.
- `status`: 'active' | 'paused' - Current status of the product.
- `region`: string - Region where the product is deployed.

#### `getProductStatus`
- Returns a `ProductStatusResponse` object.
- Accepts:
  - `productId`: string - Unique identifier for the product.
- Example output:
  - `productId`: 'prod-001'
  - `status`: 'active'
  - `region`: 'us-east-1'

#### `pauseProduct`
- Returns a `ProductStatusResponse` object.
- Accepts:
  - `productId`: string - Unique identifier for the product.
- Example output:
  - `productId`: 'prod-001'
  - `status`: 'paused'
  - `region`: 'us-east-1'

## Troubleshooting
List common issues, error messages/codes, and resolution steps.