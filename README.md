# jq-examples

This project contains some JQ queries example.

# Installation 

```ssh
brew install jq
```

# JQ Examples

### Nested Query with multiple fields

```ssh
cat example.json |  jq ".data.collections.edges[].node.products.edges[].node.variants.edges[].node | .product.productType, .quantity"
```

### Exporting data to CSV

```ssh
cat final.json |  jq -r ".[].Awis.Results.Result.Alexa | [.ContentData.DataUrl, .ContentData.SiteData.Title, .ContentData.Speed.MedianLoadTime, .ContentData.Speed.Percentile, .ContentData.AdultContent, .ContentData.Language.Locale,.ContentData.Language.Encoding,.ContentData.LinksInCount, .TrafficData.DataUrl, .TrafficData.Rank] | @csv" >> result.csv
```
