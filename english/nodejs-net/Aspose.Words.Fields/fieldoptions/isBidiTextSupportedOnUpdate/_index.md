---
title: FieldOptions.isBidiTextSupportedOnUpdate property
linktitle: isBidiTextSupportedOnUpdate property
articleTitle: isBidiTextSupportedOnUpdate property
second_title: Aspose.Words for Node.js
description: "FieldOptions.isBidiTextSupportedOnUpdate property. Gets or sets the value indicating whether bidirectional text is fully supported during field update or not."
type: docs
weight: 140
url: /nodejs-net/aspose.words.fields/fieldoptions/isBidiTextSupportedOnUpdate/
---

## FieldOptions.isBidiTextSupportedOnUpdate property

Gets or sets the value indicating whether bidirectional text is fully supported during field update or not.


```js
get isBidiTextSupportedOnUpdate(): boolean
```

### Remarks

When this property is set to ``true``, additional steps are performed to produce Right-To-Left language
(i.e. Arabic or Hebrew) compatible field result during its update.

When this property is set to ``false`` and Right-To-Left language is used, correctness of field result
after its update is not guaranteed.

The default value is ``false``.




### Examples

Shows how to use FieldOptions to ensure that field updating fully supports bi-directional text.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Ensure that any field operation involving right-to-left text is performs as expected.
doc.fieldOptions.isBidiTextSupportedOnUpdate = true;

// Use a document builder to insert a field that contains the right-to-left text.
let comboBox = builder.insertComboBox("MyComboBox", ["עֶשְׂרִים", "שְׁלוֹשִׁים", "אַרְבָּעִים", "חֲמִשִּׁים", "שִׁשִּׁים"], 0);
comboBox.calculateOnExit = true;

doc.updateFields();
doc.save(base.artifactsDir + "FieldOptions.bidi.docx");
```

### See Also

* module [Aspose.Words.Fields](../../)
* class [FieldOptions](../)

