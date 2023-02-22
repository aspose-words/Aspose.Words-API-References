---
title: FootnoteOptions.Columns
second_title: Aspose.Words för .NET API Referens
description: FootnoteOptions fast egendom. Anger antalet kolumner som fotnotsområdet är formaterat med.
type: docs
weight: 10
url: /sv/net/aspose.words.notes/footnoteoptions/columns/
---
## FootnoteOptions.Columns property

Anger antalet kolumner som fotnotsområdet är formaterat med.

```csharp
public int Columns { get; set; }
```

### Anmärkningar

Om den här egenskapen har värdet 0, formateras fotnotsområdet med ett antal kolumner baserat på antalet kolumner på den visade sidan. Standardvärdet är 0.

### Exempel

Visar hur man delar upp fotnotsavsnittet i ett givet antal kolumner.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");
doc.FootnoteOptions.Columns = 2;
doc.Save(ArtifactsDir + "Document.FootnoteColumns.docx");
```

### Se även

* class [FootnoteOptions](../)
* namnutrymme [Aspose.Words.Notes](../../footnoteoptions/)
* hopsättning [Aspose.Words](../../../)


