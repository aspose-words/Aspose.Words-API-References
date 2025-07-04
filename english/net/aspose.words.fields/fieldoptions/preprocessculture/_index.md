---
title: FieldOptions.PreProcessCulture
linktitle: PreProcessCulture
articleTitle: PreProcessCulture
second_title: Aspose.Words for .NET
description: Discover how FieldOptions PreProcessCulture enhances your data processing by customizing field value cultures for improved accuracy and efficiency.
type: docs
weight: 170
url: /net/aspose.words.fields/fieldoptions/preprocessculture/
---
## FieldOptions.PreProcessCulture property

Gets or sets the culture to preprocess field values.

```csharp
public CultureInfo PreProcessCulture { get; set; }
```

## Remarks

Currently this property only affects value of the [`FieldDocProperty`](../../fielddocproperty/) field.

The default value is `null`. When this property is set to `null`, the [`FieldDocProperty`](../../fielddocproperty/) field's value is preprocessed with the culture controlled by the [`FieldUpdateCultureSource`](../fieldupdateculturesource/) property.

## Examples

Shows how to set the preprocess culture.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// Set the culture according to which some fields will format their displayed values.
doc.FieldOptions.PreProcessCulture = new CultureInfo("de-DE");

Field field = builder.InsertField(" DOCPROPERTY CreateTime");

// The DOCPROPERTY field will display its result formatted according to the preprocess culture
// we have set to German. The field will display the date/time using the "dd.mm.yyyy hh:mm" format.
Assert.That(Regex.Match(field.Result, @"\d{2}[.]\d{2}[.]\d{4} \d{2}[:]\d{2}").Success, Is.True);

doc.FieldOptions.PreProcessCulture = CultureInfo.InvariantCulture;
field.Update();

// After switching to the invariant culture, the DOCPROPERTY field will use the "mm/dd/yyyy hh:mm" format.
Assert.That(Regex.Match(field.Result, @"\d{2}[/]\d{2}[/]\d{4} \d{2}[:]\d{2}").Success, Is.True);
```

### See Also

* class [FieldOptions](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
