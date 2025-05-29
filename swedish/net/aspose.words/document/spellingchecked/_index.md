---
title: Document.SpellingChecked
linktitle: SpellingChecked
articleTitle: SpellingChecked
second_title: Aspose.Words för .NET
description: Se till att ditt dokument är felfritt med egenskapen Stavningskontrollerad. Ta reda på om ditt innehåll har stavningskontrollerats noggrant för att säkerställa professionalism.
type: docs
weight: 430
url: /sv/net/aspose.words/document/spellingchecked/
---
## Document.SpellingChecked property

Returer`sann` om dokumentet har stavningskontrollerats.

```csharp
public bool SpellingChecked { get; set; }
```

## Anmärkningar

För att kontrollera stavningen i dokumentet igen, sätt den här egenskapen till`falsk` .

## Exempel

Visar hur man ställer in stavnings- eller grammatikverifiering.

```csharp
Document doc = new Document();

// Strängen med stavfel.
doc.FirstSection.Body.FirstParagraph.Runs.Add(new Run(doc, "The speeling in this documentz is all broked."));

// Stavnings-/grammatikkontroll startar om vi ställer in egenskaperna på falskt.
// Vi kan se alla fel i Microsoft Word via Granska -> Stavning och grammatik.
// Observera att Microsoft Word inte startar grammatik-/stavningskontroll automatiskt för DOC- och RTF-dokumentformat.
doc.SpellingChecked = checkSpellingGrammar;
doc.GrammarChecked = checkSpellingGrammar;

doc.Save(ArtifactsDir + "Document.SpellingOrGrammar.docx");
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
