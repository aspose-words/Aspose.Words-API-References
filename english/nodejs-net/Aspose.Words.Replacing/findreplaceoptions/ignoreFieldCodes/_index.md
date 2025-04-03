---
title: FindReplaceOptions.ignoreFieldCodes property
linktitle: ignoreFieldCodes property
articleTitle: ignoreFieldCodes property
second_title: Aspose.Words for NodeJs
description: "FindReplaceOptions.ignoreFieldCodes property. Gets or sets a boolean value indicating either to ignore text inside field codes"
type: docs
weight: 70
url: /nodejs-net/Aspose.Words.Replacing/findreplaceoptions/ignoreFieldCodes/
---

## FindReplaceOptions.ignoreFieldCodes property

Gets or sets a boolean value indicating either to ignore text inside field codes.
The default value is ``false``.



```js
get ignoreFieldCodes(): boolean
```

### Remarks

This option affects only field codes (it does not ignore nodes between
[NodeType.FieldSeparator](../../../aspose.words/nodetype/#FieldSeparator) and [NodeType.FieldEnd](../../../aspose.words/nodetype/#FieldEnd)).

To ignore whole field, please use corresponding option [FindReplaceOptions.ignoreFields](../ignoreFields/).




### Examples

Shows how to ignore text inside field codes.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.insertField("INCLUDETEXT", "Test IT!");

let options = new aw.Replacing.FindReplaceOptions();
options.ignoreFieldCodes = ignoreFieldCodes;;

// Replace 'T' in document ignoring text inside field code or not.
doc.range.replace(/*new Regex*/("T"), "*", options);
console.log(doc.getText());

Assert.AreEqual(
  ignoreFieldCodes
    ? "\u0013INCLUDETEXT\u0014*est I*!\u0015"
    : "\u0013INCLUDE*EX*\u0014*est I*!\u0015", doc.getText().trim());
```

### See Also

* module [Aspose.Words.Replacing](../../)
* class [FindReplaceOptions](../)

