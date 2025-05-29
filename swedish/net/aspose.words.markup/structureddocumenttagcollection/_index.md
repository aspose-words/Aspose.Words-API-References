---
title: StructuredDocumentTagCollection Class
linktitle: StructuredDocumentTagCollection
articleTitle: StructuredDocumentTagCollection
second_title: Aspose.Words för .NET
description: Utforska klassen Aspose.Words.Markup.StructuredDocumentTagCollection för effektiv hantering av strukturerade dokumenttaggar och förbättra dina dokumentbehandlingsmöjligheter.
type: docs
weight: 4760
url: /sv/net/aspose.words.markup/structureddocumenttagcollection/
---
## StructuredDocumentTagCollection class

En samling av[`IStructuredDocumentTag`](../istructureddocumenttag/) instanser som representerar de strukturerade dokumenttaggarna i det angivna intervallet.

För att lära dig mer, besök[Strukturerade dokumenttaggar eller innehållskontroll](https://docs.aspose.com/words/net/working-with-content-control-sdt/) dokumentationsartikel.

```csharp
public class StructuredDocumentTagCollection : IEnumerable<IStructuredDocumentTag>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.markup/structureddocumenttagcollection/count/) { get; } | Returnerar antalet strukturerade dokumenttaggar i samlingen. |
| [Item](../../aspose.words.markup/structureddocumenttagcollection/item/) { get; } | Returnerar den strukturerade dokumenttaggen vid det angivna indexet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetById](../../aspose.words.markup/structureddocumenttagcollection/getbyid/)(*int*) | Returnerar den strukturerade dokumenttaggen efter identifierare. |
| [GetByTag](../../aspose.words.markup/structureddocumenttagcollection/getbytag/)(*string*) | Returnerar den första taggen för strukturerat dokument som påträffas i samlingen med den angivna taggen. |
| [GetByTitle](../../aspose.words.markup/structureddocumenttagcollection/getbytitle/)(*string*) | Returnerar den första strukturerade dokumenttaggen som påträffas i samlingen med den angivna titeln. |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagcollection/getenumerator/)() | Returnerar ett uppräknarobjekt. |
| [Remove](../../aspose.words.markup/structureddocumenttagcollection/remove/)(*int*) | Tar bort den strukturerade dokumenttaggen med den angivna identifieraren. |
| [RemoveAt](../../aspose.words.markup/structureddocumenttagcollection/removeat/)(*int*) | Tar bort en strukturerad dokumenttagg vid det angivna indexet. |

## Exempel

Visar hur man får taggar för strukturerade dokument.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// Hämta den strukturerade dokumenttaggen efter Id.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsMultiSection);
Console.WriteLine(sdt.Title);

// Hämta den strukturerade dokumenttaggen eller intervalltaggen efter titel.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### Se även

* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* namnutrymme [Aspose.Words.Markup](../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../)
