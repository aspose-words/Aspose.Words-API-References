---
title: StructuredDocumentTag.LockContents
linktitle: LockContents
articleTitle: LockContents
second_title: Aspose.Words för .NET
description: Upptäck egenskapen StructuredDocumentTag LockContents, inställd på true, den förhindrar användare från att redigera SDT-innehåll, vilket säkerställer dokumentets integritet och säkerhet.
type: docs
weight: 200
url: /sv/net/aspose.words.markup/structureddocumenttag/lockcontents/
---
## StructuredDocumentTag.LockContents property

När den är inställd på`sann` , kommer den här egenskapen att förhindra att en användare redigerar innehållet i detta**SDT** .

```csharp
public bool LockContents { get; set; }
```

## Exempel

Visar hur man tillämpar redigeringsbegränsningar på strukturerade dokumenttaggar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en tagg för ett strukturerat dokument i vanlig text, som fungerar som en textruta som uppmanar användaren att fylla i den.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Sätt egenskapen "LockContents" till "true" för att förhindra att användaren redigerar innehållet i den här textrutan.
tag.LockContents = true;
builder.Write("The contents of this structured document tag cannot be edited: ");
builder.InsertNode(tag);

tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Sätt egenskapen "LockContentControl" till "true" för att förhindra att användaren
// tar bort den här taggen för strukturerat dokument manuellt i Microsoft Word.
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
