---
title: DocumentProperty.toDateTime method
linktitle: toDateTime method
articleTitle: toDateTime method
second_title: Aspose.Words for Node.js
description: "DocumentProperty.toDateTime method. Returns the property value as DateTime in UTC."
type: docs
weight: 70
url: /nodejs-net/aspose.words.properties/documentproperty/toDateTime/
---

## toDateTime() {#default}

Returns the property value as **DateTime** in UTC.



```js
toDateTime()
```

### Remarks

Throws an exception if the property type is not [PropertyType.DateTime](../../propertytype/#DateTime).

Microsoft Word stores only the date part (no time) for custom date properties.




### Examples

Shows how to create a custom document property which contains a date and time.

```js
let doc = new aw.Document();

let date = new Date(2024, 6, 9);
doc.customDocumentProperties.add("AuthorizationDate", date);

//console.log(`Document authorized on ${doc.customDocumentProperties.at("AuthorizationDate")}`);
```

Shows various type conversion methods of custom document properties.

```js
let doc = new aw.Document();
let properties = doc.customDocumentProperties;

let authDate = new Date(2024, 9, 5);
properties.add("Authorized", true);
properties.add("Authorized By", "John Doe");
properties.add("Authorized Date", authDate);
properties.add("Authorized Revision", doc.builtInDocumentProperties.revisionNumber);
properties.add("Authorized Amount", 123.45);

expect(properties.at("Authorized").toBool()).toEqual(true);
expect(properties.at("Authorized By").toString()).toEqual("John Doe");
expect(properties.at("Authorized Date").toDateTime()).toEqual(authDate);
expect(properties.at("Authorized Revision").toInt()).toEqual(1);
expect(properties.at("Authorized Amount").type).toEqual(aw.Properties.PropertyType.Double);
expect(properties.at("Authorized Amount").toDouble()).toEqual(123.45);
```

### See Also

* module [Aspose.Words.Properties](../../)
* class [DocumentProperty](../)

