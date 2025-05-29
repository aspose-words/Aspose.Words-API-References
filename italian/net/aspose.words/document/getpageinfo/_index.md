---
title: Document.GetPageInfo
linktitle: GetPageInfo
articleTitle: GetPageInfo
second_title: Aspose.Words per .NET
description: Scopri il metodo GetPageInfo per recuperare informazioni essenziali su dimensioni di pagina, orientamento e rendering per una stampa ottimizzata e una gestione avanzata dei documenti.
type: docs
weight: 650
url: /it/net/aspose.words/document/getpageinfo/
---
## Document.GetPageInfo method

Ottiene le dimensioni della pagina, l'orientamento e altre informazioni su una pagina che potrebbero essere utili per la stampa o il rendering.

```csharp
public PageInfo GetPageInfo(int pageIndex)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pageIndex | Int32 | Indice di pagina basato su 0. |

## Esempi

Mostra come verificare se la pagina è a colori oppure no.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Controlla che la prima pagina del documento non sia colorata.
Assert.IsFalse(doc.GetPageInfo(0).Colored);
```

### Guarda anche

* class [PageInfo](../../../aspose.words.rendering/pageinfo/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
