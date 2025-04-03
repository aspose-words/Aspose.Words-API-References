---
title: FindReplaceOptions.ignoreFields property
linktitle: ignoreFields property
articleTitle: ignoreFields property
second_title: Aspose.Words for NodeJs
description: "FindReplaceOptions.ignoreFields property. Gets or sets a boolean value indicating either to ignore text inside fields"
type: docs
weight: 80
url: /nodejs-net/Aspose.Words.Replacing/findreplaceoptions/ignoreFields/
---

## FindReplaceOptions.ignoreFields property

Gets or sets a boolean value indicating either to ignore text inside fields.
The default value is ``False``.



```js
get ignoreFields(): boolean
```

### Remarks

This option affects whole field (all nodes between
[NodeType.FieldStart](../../../aspose.words/nodetype/#FieldStart) and [NodeType.FieldEnd](../../../aspose.words/nodetype/#FieldEnd)).

To ignore only field codes, please use corresponding option [FindReplaceOptions.ignoreFieldCodes](../ignoreFieldCodes/).




### Examples

Shows how to ignore text inside fields.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Hello world!");
builder.insertField("QUOTE", "Hello again!");

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
let options = new aw.Replacing.FindReplaceOptions();

// Set the "IgnoreFields" flag to "true" to get the find-and-replace
// operation to ignore text inside fields.
// Set the "IgnoreFields" flag to "false" to get the find-and-replace
// operation to also search for text inside fields.
options.ignoreFields = ignoreTextInsideFields;

doc.range.replace("Hello", "Greetings", options);

expect(doc.getText().trim()).toEqual(
  ignoreTextInsideFields
    ? "Greetings world!\r\u0013QUOTE\u0014Hello again!\u0015"
    : "Greetings world!\r\u0013QUOTE\u0014Greetings again!\u0015");
```

### See Also

* module [Aspose.Words.Replacing](../../)
* class [FindReplaceOptions](../)

