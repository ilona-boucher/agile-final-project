[role]  **As a** store administrator
[function] **I need** the ability to create a new product in the catalog
[benefit]  **So that** customers can discover and purchase new items added to the store
   
### Details and Assumptions
* The product catalog is exposed via a back-end API (e.g. POST /products endpoint).
* A product must include at minimum: name, description, price, and SKU (unique identifier).
* Only authenticated users with a "Store Administrator" role can create a product.
* Price must be a positive number; SKU must be unique across the catalog (no duplicates allowed).
* This story only covers creation — advanced field validation (image formats, categories, etc.) is out of scope and may become a separate story if needed.
   
### Acceptance Criteria 
```gherkin
Given I am authenticated as a Store Administrator
When I submit valid product details (name, description, price, SKU)
Then a new product is created in the catalog
And a unique product ID is returned in the response

```
