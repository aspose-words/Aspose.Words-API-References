---
title: FieldKeywords.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: FieldKeywords Text property. Gets or sets the text of the keywords in C#.
type: docs
weight: 20
url: /net/aspose.words.fields/fieldkeywords/text/
---
## FieldKeywords.Text property

Gets or sets the text of the keywords.

```csharp
public string Text { get; set; }
```

## Examples

Shows to insert a KEYWORDS field.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Add some keywords, also referred to as "tags" in File Explorer.
doc.BuiltInDocumentProperties.Keywords = "Keyword1, Keyword2";

// The KEYWORDS field displays the value of this property.
FieldKeywords field = (FieldKeywords)builder.InsertField(FieldType.FieldKeyword, true);
field.Update();

Assert.AreEqual(" KEYWORDS ", field.GetFieldCode());
Assert.AreEqual("Keyword1, Keyword2", field.Result);

// Setting a value for the field's Text property,
// and then updating the field will also overwrite the corresponding built-in property with the new value.
field.Text = "OverridingKeyword";
field.Update();

Assert.AreEqual(" KEYWORDS  OverridingKeyword", field.GetFieldCode());
Assert.AreEqual("OverridingKeyword", field.Result);
Assert.AreEqual("OverridingKeyword", doc.BuiltInDocumentProperties.Keywords);

doc.Save(ArtifactsDir + "Field.KEYWORDS.docx");
```

### See Also

* class [FieldKeywords](../)
* namespace [Aspose.Words.Fields](../../fieldkeywords/)
* assembly [Aspose.Words](../../../)
