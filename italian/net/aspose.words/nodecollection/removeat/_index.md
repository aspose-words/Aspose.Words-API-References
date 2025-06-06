---
title: NodeCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words per .NET
description: Rimuovi facilmente i nodi dalla tua collezione con il metodo RemoveAt di NodeCollection. Semplifica la gestione dei documenti rimuovendo rapidamente nodi specifici.
type: docs
weight: 100
url: /it/net/aspose.words/nodecollection/removeat/
---
## NodeCollection.RemoveAt method

Rimuove il nodo all'indice specificato dalla raccolta e dal documento.

```csharp
public void RemoveAt(int index)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | Int32 | Indice basato su zero del nodo. Gli indici negativi sono consentiti e indicano l'accesso dalla parte posteriore dell'elenco. Ad esempio -1 indica l'ultimo nodo, -2 indica il penultimo e così via. |

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

* class [NodeCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
