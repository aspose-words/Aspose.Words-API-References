---
title: FootnoteOptions.Columns
linktitle: Columns
articleTitle: Columns
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FootnoteOptions Columns för att enkelt formatera dina fotnoter med anpassningsbara kolumnlayouter för förbättrad läsbarhet och presentation.
type: docs
weight: 10
url: /sv/net/aspose.words.notes/footnoteoptions/columns/
---
## FootnoteOptions.Columns property

Anger antalet kolumner som fotnotsområdet formateras med.

```csharp
public int Columns { get; set; }
```

## Anmärkningar

Om den här egenskapen har värdet 0 formateras fotnotsområdet med ett antal kolumner baserat på antalet kolumner på den visade sidan. Standardvärdet är 0.

## Exempel

Visar hur man delar upp fotnotsavsnittet i ett givet antal kolumner.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");
doc.FootnoteOptions.Columns = 2;
doc.Save(ArtifactsDir + "Document.FootnoteColumns.docx");
```

### Se även

* class [FootnoteOptions](../)
* namnutrymme [Aspose.Words.Notes](../../../aspose.words.notes/)
* hopsättning [Aspose.Words](../../../)
