[Home](index.md)

# Infinite Loop

This example shows how infinite loop written is processor will stop the execution with exception and you get the error result.

## Collection
*Note*
This ideally can be obtained after workspace activation. I am mentioning it here due to current cooke issue in code.

*Http Header*
collection-key : 

## Processor
```javascript
switch(request.operation ) {
    case "next":
       var n2 = store.n2
       store.n2 = store.n2 + store.n1
       store.n1 = n2
      break;
    case "previous":
       var n1 = store.n1
       store.n1 = store.n2 - store.n1
       store.n2 = n1
      break;
    default:
      // code block
  }
  return store
```

## Data Store

This is initial state of data store.

```javascript
{
  "n1": 1,
  "n2": 1
}
```

# API's

#### 1
---
/hello/world

```javascript
{
  "Message": "India Welcomes you"
}
```
#### 2
---
/fibonacci/{next/previous/current}

```javascript
{
  "n1": 1,
  "n2": 1
}
```

*Note*
> The values of n1 and n2 are supposed to be change based on API call.

---