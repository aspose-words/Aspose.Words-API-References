---
title: CustomDocumentProperties.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Properties.CustomDocumentProperties.add method"
type: docs
weight: 10
url: /nodejs-net/Aspose.Words.Properties/customdocumentproperties/add/
---

## add(name, value) {#string_string}

Creates a new custom document property of the [PropertyType.String](../../propertytype/#String) data type.



```js
add(name: stringvalue: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | string | The name of the property. |
| value | string | The value of the property. |

### Returns

The newly created property object.


## add(name, value) {#string_number}

Creates a new custom document property of the [PropertyType.Number](../../propertytype/#Number) data type.



```js
add(name: stringvalue: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | string | The name of the property. |
| value | number | The value of the property. |

### Returns

The newly created property object.


## add(name, value) {#string_date}

Creates a new custom document property of the [PropertyType.DateTime](../../propertytype/#DateTime) data type.



```js
add(name: stringvalue: Date)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | string | The name of the property. |
| value | Date | The value of the property. |

### Returns

The newly created property object.


## add(name, value) {#string_boolean}

Creates a new custom document property of the [PropertyType.Boolean](../../propertytype/#Boolean) data type.



```js
add(name: stringvalue: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | string | The name of the property. |
| value | boolean | The value of the property. |

### Returns

The newly created property object.


## add(name, value) {#string_number}

Creates a new custom document property of the [PropertyType.Double](../../propertytype/#Double) data type.



```js
add(name: stringvalue: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | string | The name of the property. |
| value | number | The value of the property. |

### Returns

The newly created property object.


## Examples

Shows how to work with a document's custom properties.

```js
let doc = new aw.Document();
let properties = doc.customDocumentProperties;

expect(properties.count).toEqual(0);

// Custom document properties are key-value pairs that we can add to the document.
properties.add("Authorized", true);
properties.add("Authorized By", "John Doe");
properties.add("Authorized Date", Date.now());
properties.add("Authorized Revision", doc.builtInDocumentProperties.revisionNumber);
properties.add("Authorized Amount", 123.45);

// The collection sorts the custom properties in alphabetic order.
expect(properties.indexOf("Authorized Amount")).toEqual(1);
expect(properties.count).toEqual(5);

// Print every custom property in the document.
/*for (let p of properties) {
    console.log(`Name: \"${p.name}\"\n\tType: \"${p.type}\"\n\tValue: \"${p.toString()}\"`);
}*/

// Display the value of a custom property using a DOCPROPERTY field.
let builder = new aw.DocumentBuilder(doc);
let field = builder.insertField(" DOCPROPERTY \"Authorized By\"").asFieldDocProperty();
field.update();

expect(field.result).toEqual("John Doe");

// We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
doc.save(base.artifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Below are three ways or removing custom properties from a document.
// 1 -  Remove by index:
properties.removeAt(1);

expect(properties.contains("Authorized Amount")).toEqual(false);
expect(properties.count).toEqual(4);

// 2 -  Remove by name:
properties.remove("Authorized Revision");

expect(properties.contains("Authorized Revision")).toEqual(false);
expect(properties.count).toEqual(3);

// 3 -  Empty the entire collection at once:
properties.clear();

expect(properties.count).toEqual(0);
```

Shows how to create a custom document property which contains a date and time.

```js
let doc = new aw.Document();

let date = new Date(2024, 6, 9);
doc.customDocumentProperties.add("AuthorizationDate", date);

//console.log(`Document authorized on ${doc.customDocumentProperties.at("AuthorizationDate")}`);
```

## See Also

* module [Aspose.Words.Properties](../../)
* class [CustomDocumentProperties](../)

