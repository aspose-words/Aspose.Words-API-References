---
title: FieldOptions.LegacyNumberFormat
linktitle: LegacyNumberFormat
articleTitle: LegacyNumberFormat
second_title: Aspose.Words for .NET
description: Discover the FieldOptions LegacyNumberFormat property to enable or disable legacy number formats for fields, enhancing compatibility and performance.
type: docs
weight: 160
url: /net/aspose.words.fields/fieldoptions/legacynumberformat/
---
## FieldOptions.LegacyNumberFormat property

Gets or sets the value indicating whether legacy (early than AW 13.10) number format for fields is enabled or not.

```csharp
public bool LegacyNumberFormat { get; set; }
```

## Remarks

When this property is set to `true`, template symbol "#" worked as in .net: Replaces the pound sign with the corresponding digit if one is present; otherwise, no symbols appears in the result string.

When this property is set to `false`, template symbol "#" works as MS Word: This format item specifies the requisite numeric places to display in the result. If the result does not include a digit in that place, MS Word displays a space. For example, { = 9 + 6 \# $### } displays $ 15.

The default value is `false`.

## Examples

Shows how enable legacy number formatting for fields.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("= 2 + 3 \\# $##");

Assert.That(field.Result, Is.EqualTo("$ 5"));

doc.FieldOptions.LegacyNumberFormat = true;
field.Update();

Assert.That(field.Result, Is.EqualTo("$5"));
```

### See Also

* class [FieldOptions](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
