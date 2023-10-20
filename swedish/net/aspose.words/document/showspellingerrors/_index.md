---
title: Document.ShowSpellingErrors
linktitle: ShowSpellingErrors
articleTitle: ShowSpellingErrors
second_title: Aspose.Words för .NET
description: Document ShowSpellingErrors fast egendom. Anger om stavfel ska visas i detta dokument i C#.
type: docs
weight: 400
url: /sv/net/aspose.words/document/showspellingerrors/
---
## Document.ShowSpellingErrors property

Anger om stavfel ska visas i detta dokument.

```csharp
public bool ShowSpellingErrors { get; set; }
```

## Exempel

Visar hur man visar/döljer fel i dokumentet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga två meningar med misstag som skulle plockas upp
// av stavnings- och grammatikkontrollen i Microsoft Word.
builder.Writeln("There is a speling error in this sentence.");
builder.Writeln("Their is a grammatical error in this sentence.");

// Om dessa alternativ är aktiverade kommer stavfel att vara understrukna
// i utdatadokumentet med en taggig röd linje, och en dubbelblå linje kommer att markera grammatiska misstag.
doc.ShowGrammaticalErrors = showErrors;
doc.ShowSpellingErrors = showErrors;

doc.Save(ArtifactsDir + "Document.SpellingAndGrammarErrors.docx");
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
