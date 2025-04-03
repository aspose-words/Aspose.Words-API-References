---
title: FieldOptions.useInvariantCultureNumberFormat property
linktitle: useInvariantCultureNumberFormat property
articleTitle: useInvariantCultureNumberFormat property
second_title: Aspose.Words for NodeJs
description: "FieldOptions.useInvariantCultureNumberFormat property. Gets or sets the value indicating that number format is parsed using invariant culture or not"
type: docs
weight: 190
url: /nodejs-net/aspose.words.fields/fieldoptions/useInvariantCultureNumberFormat/
---

## FieldOptions.useInvariantCultureNumberFormat property

Gets or sets the value indicating that number format is parsed using invariant culture or not


```js
get useInvariantCultureNumberFormat(): boolean
```

### Remarks

When this property is set to ``true``, number format is taken from an invariant culture.


When this property is set to ``false``, number format is taken from the current thread's culture.


The default value is ``false``.




### Examples

Shows how to format numbers according to the invariant culture.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

Thread.currentThread.CurrentCulture = new CultureInfo("de-DE");
let field = builder.insertField(" = 1234567,89 \\# $#,###,###.##");
field.update();

// Sometimes, fields may not format their numbers correctly under certain cultures.
expect(doc.fieldOptions.useInvariantCultureNumberFormat).toEqual(false);
expect(field.result).toEqual("$1.234.567,89 ,     ");

// To fix this, we could change the culture for the entire thread.
// Another way to fix this is to set this flag,
// which gets all fields to use the invariant culture when formatting numbers.
// This way allows us to avoid changing the culture for the entire thread.
doc.fieldOptions.useInvariantCultureNumberFormat = true;
field.update();
expect(field.result).toEqual("$1.234.567,89");
```

### See Also

* module [Aspose.Words.Fields](../../)
* class [FieldOptions](../)

