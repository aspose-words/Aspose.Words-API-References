---
title: Section.ClearContent
second_title: Aspose.Words per .NET API Reference
description: Section metodo. Cancella la sezione.
type: docs
weight: 110
url: /it/net/aspose.words/section/clearcontent/
---
## Section.ClearContent method

Cancella la sezione.

```csharp
public void ClearContent()
```

### Osservazioni

Il testo di[`Body`](../body/) viene cancellato, rimane solo un paragrafo vuoto che rappresenta l'interruzione di sezione.

Il testo di tutte le intestazioni e piè di pagina viene cancellato, ma[`HeaderFooter`](../../headerfooter/) gli oggetti stessi non vengono rimossi.

### Esempi

Mostra come cancellare il contenuto di una sezione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.GetText().Trim());
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// L'esecuzione del metodo "ClearContent" rimuoverà tutto il contenuto della sezione
// ma lascia un paragrafo vuoto per aggiungere nuovamente contenuto.
doc.FirstSection.ClearContent();

Assert.AreEqual(string.Empty, doc.GetText().Trim());
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);
```

### Guarda anche

* class [Section](../)
* spazio dei nomi [Aspose.Words](../../section/)
* assemblea [Aspose.Words](../../../)


