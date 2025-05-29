---
title: Document.ShowGrammaticalErrors
linktitle: ShowGrammaticalErrors
articleTitle: ShowGrammaticalErrors
second_title: Aspose.Words för .NET
description: Kontrollera synligheten av grammatikfel i ditt dokument med egenskapen ShowGrammaticalErrors. Förbättra skrivandets tydlighet och professionalism utan ansträngning.
type: docs
weight: 410
url: /sv/net/aspose.words/document/showgrammaticalerrors/
---
## Document.ShowGrammaticalErrors property

Anger om grammatikfel ska visas i det här dokumentet.

```csharp
public bool ShowGrammaticalErrors { get; set; }
```

## Exempel

Visar hur man visar/döljer fel i dokumentet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga två meningar med misstag som skulle upptäckas
// av stavnings- och grammatikkontrollen i Microsoft Word.
builder.Writeln("There is a speling error in this sentence.");
builder.Writeln("Their is a grammatical error in this sentence.");

// Om dessa alternativ är aktiverade kommer stavfel att understrykas
// i utdatadokumentet med en taggig röd linje, och en dubbel blå linje markerar grammatiska fel.
doc.ShowGrammaticalErrors = showErrors;
doc.ShowSpellingErrors = showErrors;

doc.Save(ArtifactsDir + "Document.SpellingAndGrammarErrors.docx");
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
