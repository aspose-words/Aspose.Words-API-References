---
title: FieldOptions.IsBidiTextSupportedOnUpdate
linktitle: IsBidiTextSupportedOnUpdate
articleTitle: IsBidiTextSupportedOnUpdate
second_title: Aspose.Words for .NET
description: Discover if bidirectional text support is enabled in FieldOptions. Easily manage text updates for enhanced multilingual functionality.
type: docs
weight: 150
url: /net/aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/
---
## FieldOptions.IsBidiTextSupportedOnUpdate property

Gets or sets the value indicating whether bidirectional text is fully supported during field update or not.

```csharp
public bool IsBidiTextSupportedOnUpdate { get; set; }
```

## Remarks

When this property is set to `true`, additional steps are performed to produce Right-To-Left language (i.e. Arabic or Hebrew) compatible field result during its update.

When this property is set to `false` and Right-To-Left language is used, correctness of field result after its update is not guaranteed.

The default value is `false`.

## Examples

Shows how to use FieldOptions to ensure that field updating fully supports bi-directional text.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ensure that any field operation involving right-to-left text is performs as expected. 
doc.FieldOptions.IsBidiTextSupportedOnUpdate = true;

// Use a document builder to insert a field that contains the right-to-left text.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "עֶשְׂרִים", "שְׁלוֹשִׁים", "אַרְבָּעִים", "חֲמִשִּׁים", "שִׁשִּׁים" }, 0);
comboBox.CalculateOnExit = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.Bidi.docx");
```

### See Also

* class [FieldOptions](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
