---
title: Document.GrammarChecked
second_title: Aspose.Words för .NET API Referens
description: Document fast egendom. ReturnerarSann om dokumentet har kontrollerats för grammatik.
type: docs
weight: 180
url: /sv/net/aspose.words/document/grammarchecked/
---
## Document.GrammarChecked property

Returnerar`Sann` om dokumentet har kontrollerats för grammatik.

```csharp
public bool GrammarChecked { get; set; }
```

### Anmärkningar

För att kontrollera grammatiken i dokumentet igen, ställ in den här egenskapen till`falsk` .

### Exempel

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
* namnutrymme [Aspose.Words](../../document/)
* hopsättning [Aspose.Words](../../../)


