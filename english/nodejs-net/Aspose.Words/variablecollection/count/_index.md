---
title: VariableCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Node.js
description: "VariableCollection.count property. Gets the number of elements contained in the collection."
type: docs
weight: 10
url: /nodejs-net/aspose.words/variablecollection/count/
---

## VariableCollection.count property

Gets the number of elements contained in the collection.


```js
get count(): number
```

### Examples

Shows how to work with a document's variable collection.

```js
let doc = new aw.Document();
let variables = doc.variables;

// Every document has a collection of key/value pair variables, which we can add items to.
variables.add("Home address", "123 Main St.");
variables.add("City", "London");
variables.add("Bedrooms", "3");

expect(variables.count).toEqual(3);

// We can display the values of variables in the document body using DOCVARIABLE fields.
let builder = new aw.DocumentBuilder(doc);
let field = builder.insertField(aw.Fields.FieldType.FieldDocVariable, true).asFieldDocVariable();
field.variableName = "Home address";
field.update();

expect(field.result).toEqual("123 Main St.");

// Assigning values to existing keys will update them.
variables.add("Home address", "456 Queen St.");

// We will then have to update DOCVARIABLE fields to ensure they display an up-to-date value.
expect(field.result).toEqual("123 Main St.");

field.update();

expect(field.result).toEqual("456 Queen St.");

// Verify that the document variables with a certain name or value exist.
expect(variables.contains("City")).toEqual(true);

// The collection of variables automatically sorts variables alphabetically by name.
expect(variables.indexOfKey("Bedrooms")).toEqual(0);
expect(variables.indexOfKey("City")).toEqual(1);
expect(variables.indexOfKey("Home address")).toEqual(2);

expect(variables.at(0)).toEqual("3");
expect(variables.at("City")).toEqual("London");

// Enumerate over the collection of variables.
for (var i = 0; i < variables.count; i++) {
  console.log(`Index: ${i}, Value: ${variables.at(i)}`);
}

// Below are three ways of removing document variables from a collection.
// 1 -  By name:
variables.remove("City");

expect(variables.contains("City")).toEqual(false);

// 2 -  By index:
variables.removeAt(1);

expect(variables.contains("Home address")).toEqual(false);

// 3 -  Clear the whole collection at once:
variables.clear();

expect(variables.count).toEqual(0);
```

### See Also

* module [Aspose.Words](../../)
* class [VariableCollection](../)

