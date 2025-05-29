---
title: FindReplaceOptions.IgnoreStructuredDocumentTags
linktitle: IgnoreStructuredDocumentTags
articleTitle: IgnoreStructuredDocumentTags
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FindReplaceOptions IgnoreStructuredDocumentTags. Kontrollera om StructuredDocumentTag-innehåll ignoreras med denna lättanvända booleska inställning.
type: docs
weight: 120
url: /sv/net/aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/
---
## FindReplaceOptions.IgnoreStructuredDocumentTags property

Hämtar eller ställer in ett booleskt värde som anger att innehållet i antingen ska ignoreras[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) . Standardvärdet är`falsk` .

```csharp
public bool IgnoreStructuredDocumentTags { get; set; }
```

## Anmärkningar

När det här alternativet är inställt på`sann` , innehållet i[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) kommer att behandlas som en enkel text.

Annars,[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) kommer att bearbetas som fristående Story och ersättningsmönstret kommer att sökas separat för varje[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) , så att om mönstret korsar ett[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) , då kommer ersättning inte att utföras för ett sådant mönster.

## Exempel

Visar hur man ignorerar innehållet i taggar från ersättning.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

// Detta stycke innehåller SDT.
Paragraph p = (Paragraph)doc.FirstSection.Body.GetChild(NodeType.Paragraph, 2, true);
string textToSearch = p.ToString(SaveFormat.Text).Trim();

FindReplaceOptions options = new FindReplaceOptions() { IgnoreStructuredDocumentTags = true };
doc.Range.Replace(textToSearch, "replacement", options);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IgnoreStructuredDocumentTags.docx");
```

### Se även

* class [FindReplaceOptions](../)
* namnutrymme [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* hopsättning [Aspose.Words](../../../)
