---
title: FieldToc.CaptionlessTableOfFiguresLabel
linktitle: CaptionlessTableOfFiguresLabel
articleTitle: CaptionlessTableOfFiguresLabel
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldToc CaptionlessTableOfFiguresLabel för att anpassa din figurtabell. Hantera enkelt sekvensidentifierare utan bildtexter!
type: docs
weight: 30
url: /sv/net/aspose.words.fields/fieldtoc/captionlesstableoffigureslabel/
---
## FieldToc.CaptionlessTableOfFiguresLabel property

Hämtar eller anger namnet på sekvensidentifieraren som används vid uppbyggnad av en figurtabell som inte inkluderar bildtextens etikett och nummer.

```csharp
public string CaptionlessTableOfFiguresLabel { get; set; }
```

## Exempel

Visar hur man anger namnet på sekvensidentifieraren.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);
fieldToc.CaptionlessTableOfFiguresLabel = "Test";

Assert.AreEqual(" TOC  \\a Test", fieldToc.GetFieldCode());
```

### Se även

* class [FieldToc](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
