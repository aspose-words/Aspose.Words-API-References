---
title: DocumentProperty.toBool method
linktitle: toBool method
articleTitle: toBool method
second_title: Aspose.Words for Node.js
description: "DocumentProperty.toBool method. Returns the property value as bool."
type: docs
weight: 50
url: /nodejs-net/aspose.words.properties/documentproperty/toBool/
---

## toBool() {#default}

Returns the property value as bool.


```js
toBool()
```

### Remarks

Throws an exception if the property type is not [PropertyType.Boolean](../../propertytype/#Boolean).




### Examples

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

