---
title: StructuredDocumentTag.LockContents
linktitle: LockContents
articleTitle: LockContents
second_title: Aspose.Words för .NET
description: StructuredDocumentTag LockContents fast egendom. När inställd påSann  kommer den här egenskapen att förbjuda en användare från att redigera innehållet i dennaSDT  i C#.
type: docs
weight: 200
url: /sv/net/aspose.words.markup/structureddocumenttag/lockcontents/
---
## StructuredDocumentTag.LockContents property

När inställd på`Sann` , kommer den här egenskapen att förbjuda en användare från att redigera innehållet i denna**SDT** .

```csharp
public bool LockContents { get; set; }
```

## Exempel

Visar hur du tillämpar redigeringsbegränsningar på strukturerade dokumenttaggar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en textstrukturerad dokumenttagg, som fungerar som en textruta som uppmanar användaren att fylla i den.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Ställ in egenskapen "LockContents" till "true" för att förbjuda användaren att redigera innehållet i denna textruta.
tag.LockContents = true;
builder.Write("The contents of this structured document tag cannot be edited: ");
builder.InsertNode(tag);

tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Ställ in egenskapen "LockContentControl" till "true" för att förbjuda användaren från
// ta bort denna strukturerade dokumenttagg manuellt i Microsoft Word.
tag.LockContentControl = true;

builder.InsertParagraph();
builder.Write("This structured document tag cannot be deleted but its contents can be edited: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Lock.docx");
```

### Se även

* class [StructuredDocumentTag](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
