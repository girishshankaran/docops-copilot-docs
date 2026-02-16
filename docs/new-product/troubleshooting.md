# Troubleshooting

## Overview
Describe the feature, its use case, and its value proposition.

## Configuration & Installation
Document setup, prerequisites, environment variables, and dependencies.

## API Documentation
Document endpoints, request parameters, response schema, and examples.

### Product Status API

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
