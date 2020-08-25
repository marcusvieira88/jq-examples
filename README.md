# jq-examples

This project contains some JQ queries example.

# Installation 

```ssh
brew install jq
```

# Nested Query with multiple fields

```ssh
cat example.json |  jq ".data.collections.edges[].node.products.edges[].node.variants.edges[].node | .product.productType, .quantity"
```
