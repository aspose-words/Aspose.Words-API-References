---
title: StructuredDocumentTagCollection.GetByTitle
linktitle: GetByTitle
articleTitle: GetByTitle
second_title: Aspose.Words för .NET
description: StructuredDocumentTagCollection GetByTitle metod. Returnerar den första strukturerade dokumenttaggen som påträffas i samlingen med den angivna titeln i C#.
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
| title | String | Titeln på strukturerad dokumenttagg. |

## Anmärkningar

Returnerar null om den strukturerade dokumenttaggen med den angivna titeln inte kan hittas.

## Exempel

Visar hur man får strukturerad dokumenttagg.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// Hämta den strukturerade dokumenttaggen efter Id.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsRanged());
Console.WriteLine(sdt.Title);

// Hämta den strukturerade dokumenttaggen eller ranged taggen efter titel.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### Se även

* interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* class [StructuredDocumentTagCollection](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
