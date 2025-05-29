---
title: Document.GrammarChecked
linktitle: GrammarChecked
articleTitle: GrammarChecked
second_title: Aspose.Words för .NET
description: Säkerställ ditt dokuments kvalitet med egenskapen GrammarChecked. Ta reda på om din text är grammatikverifierad för polerade, professionella resultat.
type: docs
weight: 190
url: /sv/net/aspose.words/document/grammarchecked/
---
## Document.GrammarChecked property

Returer`sann` om dokumentet har kontrollerats med avseende på grammatik.

```csharp
public bool GrammarChecked { get; set; }
```

## Anmärkningar

För att kontrollera grammatiken i dokumentet igen, sätt den här egenskapen till`falsk` .

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
