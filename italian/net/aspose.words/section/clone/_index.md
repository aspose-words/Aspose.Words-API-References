---
title: Section.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words per .NET
description: Duplica le sezioni senza sforzo con il nostro metodo "Section Clone". Semplifica il tuo flusso di lavoro e aumenta la produttività con questo potente strumento!
type: docs
weight: 130
url: /it/net/aspose.words/section/clone/
---
## Section.Clone method

Crea un duplicato di questa sezione.

```csharp
public Section Clone()
```

## Esempi

Mostra come aggiungere e rimuovere sezioni in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

// Elimina la prima sezione dal documento.
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// Aggiungere una copia di quella che ora è la prima sezione alla fine del documento.
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

### Guarda anche

* class [Section](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
