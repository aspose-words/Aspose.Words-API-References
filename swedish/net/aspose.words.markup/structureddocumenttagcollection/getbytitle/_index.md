---
title: StructuredDocumentTagCollection.GetByTitle
linktitle: GetByTitle
articleTitle: GetByTitle
second_title: Aspose.Words för .NET
description: Upptäck GetByTitle-metoden i StructuredDocumentTagCollection, som effektivt hämtar den första dokumenttaggen efter titel för effektiv datahantering.
type: docs
weight: 50
url: /sv/net/aspose.words.markup/structureddocumenttagcollection/getbytitle/
---
## StructuredDocumentTagCollection.GetByTitle method

Returnerar den första strukturerade dokumenttaggen som påträffas i samlingen med den angivna titeln.

```csharp
public IStructuredDocumentTag GetByTitle(string title)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| title | String | Titeln på taggen för det strukturerade dokumentet. |

## Anmärkningar

Returnerar null om den strukturerade dokumenttaggen med den angivna titeln inte kan hittas.

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

* interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* class [StructuredDocumentTagCollection](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
