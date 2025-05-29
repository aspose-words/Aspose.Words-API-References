---
title: IStructuredDocumentTag.LockContents
linktitle: LockContents
articleTitle: LockContents
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen IStructuredDocumentTag LockContents förbättrar dokumentsäkerheten genom att förhindra innehållsredigeringar. Se till att din SDT förblir intakt!
type: docs
weight: 80
url: /sv/net/aspose.words.markup/istructureddocumenttag/lockcontents/
---
## IStructuredDocumentTag.LockContents property

När den här egenskapen är satt till sant förhindrar den en användare att redigera innehållet i detta**SDT** .

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

* interface [IStructuredDocumentTag](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
