---
title: FindReplaceOptions.IgnoreStructuredDocumentTags
second_title: Aspose.Words för .NET API Referens
description: FindReplaceOptions fast egendom. Hämtar eller ställer in ett booleskt värde som anger att innehållet ska ignorerasStructuredDocumentTag . Standardvärdet ärfalsk .
type: docs
weight: 120
url: /sv/net/aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/
---
## FindReplaceOptions.IgnoreStructuredDocumentTags property

Hämtar eller ställer in ett booleskt värde som anger att innehållet ska ignoreras[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) . Standardvärdet är`falsk` .

```csharp
public bool IgnoreStructuredDocumentTags { get; set; }
```

### Anmärkningar

När det här alternativet är inställt på`Sann` , innehållet i[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) kommer att behandlas som en enkel text.

Annars,[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) kommer att behandlas som fristående Story och ersättande mönster kommer att sökas separat för varje[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/), så att om mönstret korsar a[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) , då kommer ersättning inte att utföras för ett sådant mönster.

### Exempel

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
* namnutrymme [Aspose.Words.Replacing](../../findreplaceoptions/)
* hopsättning [Aspose.Words](../../../)


