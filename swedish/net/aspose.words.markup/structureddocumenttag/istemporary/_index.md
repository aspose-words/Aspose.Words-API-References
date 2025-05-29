---
title: StructuredDocumentTag.IsTemporary
linktitle: IsTemporary
articleTitle: IsTemporary
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen StructuredDocumentTag IsTemporary avgör om din SDT tas bort från WordProcessingML vid innehållsändringar. Optimera dina dokument idag!
type: docs
weight: 160
url: /sv/net/aspose.words.markup/structureddocumenttag/istemporary/
---
## StructuredDocumentTag.IsTemporary property

Anger om detta**SDT** ska tas bort från WordProcessingML-dokumentet när dess innehåll ändras.

```csharp
public bool IsTemporary { get; set; }
```

## Exempel

Visar hur man skapar engångskontroller.

```csharp
Document doc = new Document();

// Infoga en tagg för ett strukturerat dokument i oformaterad text,
// som fungerar som ett vanligt textformulär som användaren kan skriva in text i.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Sätt egenskapen "IsTemporary" till "true" för att få taggen för strukturerat dokument att försvinna och
// integrera dess innehåll i dokumentet efter att användaren har redigerat det en gång i Microsoft Word.
// Sätt egenskapen "IsTemporary" till "false" för att tillåta användaren att redigera innehållet
// av den strukturerade dokumenttaggen valfritt antal gånger.
tag.IsTemporary = isTemporary;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Please enter text: ");
builder.InsertNode(tag);

// Infoga ytterligare en strukturerad dokumenttagg i form av en kryssruta och sätt dess standardläge till "markerad".
tag = new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline);
tag.Checked = true;

// Sätt egenskapen "IsTemporary" till "true" för att göra kryssrutan till en symbol
// när användaren klickar på den i Microsoft Word.
// Sätt egenskapen "IsTemporary" till "false" för att tillåta användaren att klicka på kryssrutan valfritt antal gånger.
tag.IsTemporary = isTemporary;

builder.Write("\nPlease click the check box: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IsTemporary.docx");
```

### Se även

* class [StructuredDocumentTag](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
