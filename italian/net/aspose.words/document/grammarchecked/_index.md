---
title: Document.GrammarChecked
second_title: Aspose.Words per .NET API Reference
description: Document proprietà. Restituisce VERO se il documento è stato controllato per la grammatica.
type: docs
weight: 180
url: /it/net/aspose.words/document/grammarchecked/
---
## Document.GrammarChecked property

Restituisce **VERO** se il documento è stato controllato per la grammatica.

```csharp
public bool GrammarChecked { get; set; }
```

### Osservazioni

Per ricontrollare la grammatica nel documento, impostare questa proprietà su **falso** .

### Esempi

Mostra come impostare la verifica ortografica o grammaticale.

```csharp
Document doc = new Document();

// La stringa con errori di ortografia.
doc.FirstSection.Body.FirstParagraph.Runs.Add(new Run(doc, "The speeling in this documentz is all broked."));

 // Il controllo ortografico/grammatico inizia se impostiamo le proprietà su false.
// Possiamo vedere tutti gli errori in Microsoft Word tramite Revisione -> Ortografia e amp; Grammatica.
// Nota che Microsoft Word non avvia automaticamente il controllo grammaticale/ortografico per il formato documento DOC e RTF.
doc.SpellingChecked = checkSpellingGrammar;
doc.GrammarChecked = checkSpellingGrammar;

doc.Save(ArtifactsDir + "Document.SpellingOrGrammar.docx");
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)


