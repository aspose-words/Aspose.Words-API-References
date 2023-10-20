---
title: Document.ShadeFormData
linktitle: ShadeFormData
articleTitle: ShadeFormData
second_title: Aspose.Words för .NET
description: Document ShadeFormData fast egendom. Anger om den grå skuggningen ska aktiveras i formulärfält i C#.
type: docs
weight: 380
url: /sv/net/aspose.words/document/shadeformdata/
---
## Document.ShadeFormData property

Anger om den grå skuggningen ska aktiveras i formulärfält.

```csharp
public bool ShadeFormData { get; set; }
```

## Exempel

Visar hur man tillämpar grå skuggning på formulärfält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world! ");
builder.InsertTextInput("My form field", TextFormFieldType.Regular, "",
    "Text contents of form field, which are shaded in grey by default.", 0);

// Vi kan stänga av den grå skuggningen så att den bokmärkta texten smälter in med den andra texten.
doc.ShadeFormData = useGreyShading;
doc.Save(ArtifactsDir + "Document.ShadeFormData.docx");
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
