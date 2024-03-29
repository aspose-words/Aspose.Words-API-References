---
title: StructuredDocumentTag.IsTemporary
linktitle: IsTemporary
articleTitle: IsTemporary
second_title: Aspose.Words för .NET
description: StructuredDocumentTag IsTemporary fast egendom. Anger om dettaSDT ska tas bort från WordProcessingMLdokumentet när dess contents ändras i C#.
type: docs
weight: 160
url: /sv/net/aspose.words.markup/structureddocumenttag/istemporary/
---
## StructuredDocumentTag.IsTemporary property

Anger om detta**SDT** ska tas bort från WordProcessingML-dokumentet när dess contents ändras.

```csharp
public bool IsTemporary { get; set; }
```

## Exempel

Visar hur man gör engångskontroller.

```csharp
Document doc = new Document();

// Infoga en textstrukturerad dokumenttagg,
// som kommer att fungera som en vanlig textform som användaren kan skriva in text i.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Ställ in egenskapen "IsTemporary" till "true" för att få den strukturerade dokumenttaggen att försvinna och
// assimilera dess innehåll i dokumentet efter att användaren redigerat det en gång i Microsoft Word.
// Ställ in egenskapen "IsTemporary" till "false" för att tillåta användaren att redigera innehållet
// av den strukturerade dokumenttaggen hur många gånger som helst.
tag.IsTemporary = isTemporary;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Please enter text: ");
builder.InsertNode(tag);

// Infoga en annan strukturerad dokumenttagg i form av en kryssruta och ställ in dess standardläge till "markerad".
tag = new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline);
tag.Checked = true;

// Ställ in egenskapen "IsTemporary" till "true" för att få kryssrutan att bli en symbol
// när användaren klickar på den i Microsoft Word.
// Ställ in egenskapen "IsTemporary" till "false" för att tillåta användaren att klicka på kryssrutan hur många gånger som helst.
tag.IsTemporary = isTemporary;

builder.Write("\nPlease click the check box: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IsTemporary.docx");
```

### Se även

* class [StructuredDocumentTag](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
