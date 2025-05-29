---
title: StructuredDocumentTagCollection Class
linktitle: StructuredDocumentTagCollection
articleTitle: StructuredDocumentTagCollection
second_title: Aspose.Words per .NET
description: Esplora la classe Aspose.Words.Markup.StructuredDocumentTagCollection per una gestione efficiente dei tag dei documenti strutturati, migliorando le capacità di elaborazione dei documenti.
type: docs
weight: 4760
url: /it/net/aspose.words.markup/structureddocumenttagcollection/
---
## StructuredDocumentTagCollection class

Una raccolta di[`IStructuredDocumentTag`](../istructureddocumenttag/) istanze che rappresentano i tag del documento strutturato nell'intervallo specificato.

Per saperne di più, visita il[Tag di documenti strutturati o controllo dei contenuti](https://docs.aspose.com/words/net/working-with-content-control-sdt/) articolo di documentazione.

```csharp
public class StructuredDocumentTagCollection : IEnumerable<IStructuredDocumentTag>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.markup/structureddocumenttagcollection/count/) { get; } | Restituisce il numero di tag di documenti strutturati nella raccolta. |
| [Item](../../aspose.words.markup/structureddocumenttagcollection/item/) { get; } | Restituisce il tag del documento strutturato all'indice specificato. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetById](../../aspose.words.markup/structureddocumenttagcollection/getbyid/)(*int*) | Restituisce il tag del documento strutturato in base all'identificatore. |
| [GetByTag](../../aspose.words.markup/structureddocumenttagcollection/getbytag/)(*string*) | Restituisce il primo tag di documento strutturato incontrato nella raccolta con il tag specificato. |
| [GetByTitle](../../aspose.words.markup/structureddocumenttagcollection/getbytitle/)(*string*) | Restituisce il primo tag di documento strutturato riscontrato nella raccolta con il titolo specificato. |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagcollection/getenumerator/)() | Restituisce un oggetto enumeratore. |
| [Remove](../../aspose.words.markup/structureddocumenttagcollection/remove/)(*int*) | Rimuove il tag del documento strutturato con l'identificatore specificato. |
| [RemoveAt](../../aspose.words.markup/structureddocumenttagcollection/removeat/)(*int*) | Rimuove un tag di documento strutturato all'indice specificato. |

## Esempi

Mostra come ottenere il tag del documento strutturato.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// Ottieni il tag del documento strutturato tramite Id.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsMultiSection);
Console.WriteLine(sdt.Title);

// Ottieni il tag del documento strutturato o il tag con intervallo in base al titolo.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### Guarda anche

* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* spazio dei nomi [Aspose.Words.Markup](../../aspose.words.markup/)
* assemblea [Aspose.Words](../../)
