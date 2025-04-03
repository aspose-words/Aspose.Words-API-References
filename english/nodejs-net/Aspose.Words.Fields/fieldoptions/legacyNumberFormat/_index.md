---
title: FieldOptions.legacyNumberFormat property
linktitle: legacyNumberFormat property
articleTitle: legacyNumberFormat property
second_title: Aspose.Words for NodeJs
description: "FieldOptions.legacyNumberFormat property. Gets or sets the value indicating whether legacy (early than AW 13.10) number format for fields is enabled or not."
type: docs
weight: 150
url: /nodejs-net/Aspose.Words.Fields/fieldoptions/legacyNumberFormat/
---

## FieldOptions.legacyNumberFormat property

Gets or sets the value indicating whether legacy (early than AW 13.10) number format for fields is enabled or not.


```js
get legacyNumberFormat(): boolean
```

### Remarks

When this property is set to ``true``, template symbol "#" worked as in .net:
Replaces the pound sign with the corresponding digit if one is present; otherwise, no symbols appears in the result string.

When this property is set to ``false``, template symbol "#" works as MS Word:
This format item specifies the requisite numeric places to display in the result.
If the result does not include a digit in that place, MS Word displays a space. For example, { = 9 + 6 \\# $### } displays $ 15.

The default value is ``false``.




### Examples

Shows how enable legacy number formatting for fields.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let field = builder.insertField("= 2 + 3 \\# $##");

expect(field.result).toEqual("$ 5");

doc.fieldOptions.legacyNumberFormat = true;
field.update();

expect(field.result).toEqual("$5");
```

### See Also

* module [Aspose.Words.Fields](../../)
* class [FieldOptions](../)

