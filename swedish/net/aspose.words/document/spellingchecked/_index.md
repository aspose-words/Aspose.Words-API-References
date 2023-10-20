---
title: Document.SpellingChecked
linktitle: SpellingChecked
articleTitle: SpellingChecked
second_title: Aspose.Words för .NET
description: Document SpellingChecked fast egendom. ReturnerarSann om dokumentet har stavningskontrollerats i C#.
type: docs
weight: 410
url: /sv/net/aspose.words/document/spellingchecked/
---
## Document.SpellingChecked property

Returnerar`Sann` om dokumentet har stavningskontrollerats.

```csharp
public bool SpellingChecked { get; set; }
```

## Anmärkningar

För att kontrollera stavningen i dokumentet igen, ställ in den här egenskapen till`falsk` .

## Exempel

Visar hur du ställer in stavning eller grammatikverifiering.

```csharp
Document doc = new Document();

// Strängen med stavfel.
doc.FirstSection.Body.FirstParagraph.Runs.Add(new Run(doc, "The speeling in this documentz is all broked."));

 // Stavnings-/Grammatikkontroll startar om vi ställer in egenskaper på false.
// Vi kan se alla fel i Microsoft Word via Granska -> Stavning & Grammatik.
// Observera att Microsoft Word inte startar grammatik/stavningskontroll automatiskt för DOC- och RTF-dokumentformat.
doc.SpellingChecked = checkSpellingGrammar;
doc.GrammarChecked = checkSpellingGrammar;

doc.Save(ArtifactsDir + "Document.SpellingOrGrammar.docx");
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
