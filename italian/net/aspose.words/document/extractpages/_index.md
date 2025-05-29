---
title: Document.ExtractPages
linktitle: ExtractPages
articleTitle: ExtractPages
second_title: Aspose.Words per .NET
description: Scopri il metodo Document ExtractPages per recuperare senza sforzo intervalli di pagine specifici, migliorando l'efficienza e la gestione dei tuoi documenti.
type: docs
weight: 640
url: /it/net/aspose.words/document/extractpages/
---
## Document.ExtractPages method

Restituisce il[`Document`](../) oggetto che rappresenta un intervallo specificato di pagine.

```csharp
public Document ExtractPages(int index, int count)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | Int32 | Indice a partire da zero della prima pagina da estrarre. |
| count | Int32 | Numero di pagine da estrarre. |

## Osservazioni

Il documento risultante dovrebbe apparire come quello in MS Word, come se avessimo eseguito 'Stampa pagine specifiche': la numerazione, le intestazioni/piè di pagina e il layout delle tabelle incrociate verranno conservati. Tuttavia, a causa del gran numero di sfumature, che compaiono riducendo il numero di pagine, la corrispondenza completa del layout è un compito piuttosto complicato che richiede molto impegno. A seconda della complessità del documento, potrebbero esserci lievi differenze nel layout del contenuto del documento risultante rispetto al documento di origine. Ogni feedback sarà molto apprezzato.

## Esempi

Mostra come ottenere un intervallo specificato di pagine dal documento.

```csharp
Document doc = new Document(MyDir + "Layout entities.docx");

doc = doc.ExtractPages(0, 2);

doc.Save(ArtifactsDir + "Document.ExtractPages.docx");
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
