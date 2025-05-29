---
title: Document.GrammarChecked
linktitle: GrammarChecked
articleTitle: GrammarChecked
second_title: Aspose.Words per .NET
description: Garantisci la qualità del tuo documento con la proprietà GrammarChecked. Scopri se il tuo testo è grammaticalmente verificato per risultati impeccabili e professionali.
type: docs
weight: 190
url: /it/net/aspose.words/document/grammarchecked/
---
## Document.GrammarChecked property

Restituisce`VERO` se il documento è stato controllato grammaticalmente.

```csharp
public bool GrammarChecked { get; set; }
```

## Osservazioni

Per ricontrollare la grammatica nel documento, imposta questa proprietà su`falso` .

## Esempi

Mostra come impostare la verifica ortografica o grammaticale.

```csharp
Document doc = new Document();

// La stringa con errori di ortografia.
doc.FirstSection.Body.FirstParagraph.Runs.Add(new Run(doc, "The speeling in this documentz is all broked."));

// Il controllo ortografico/grammaticale inizia se impostiamo le proprietà su false.
// Possiamo vedere tutti gli errori in Microsoft Word tramite Revisione -> Ortografia e grammatica.
// Si noti che Microsoft Word non avvia automaticamente il controllo grammaticale/ortografia per i formati di documento DOC e RTF.
doc.SpellingChecked = checkSpellingGrammar;
doc.GrammarChecked = checkSpellingGrammar;

doc.Save(ArtifactsDir + "Document.SpellingOrGrammar.docx");
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
