---
title: IStructuredDocumentTag.LockContentControl
linktitle: LockContentControl
articleTitle: LockContentControl
second_title: Aspose.Words för .NET
description: Identifiera egenskapen IStructuredDocumentTag LockContentControl. Om den är satt till sant förhindrar den användare från att ta bort SDT, vilket förbättrar dokumentintegriteten och kontrollen.
type: docs
weight: 70
url: /sv/net/aspose.words.markup/istructureddocumenttag/lockcontentcontrol/
---
## IStructuredDocumentTag.LockContentControl property

När den här egenskapen är satt till sant förhindrar den en användare från att ta bort detta**SDT** .

```csharp
public bool LockContentControl { get; set; }
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

* interface [IStructuredDocumentTag](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
