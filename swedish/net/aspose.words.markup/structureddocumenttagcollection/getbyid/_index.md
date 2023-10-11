---
title: StructuredDocumentTagCollection.GetById
second_title: Aspose.Words för .NET API Referens
description: StructuredDocumentTagCollection metod. Returnerar den strukturerade dokumenttaggen med identifierare.
type: docs
weight: 30
url: /sv/net/aspose.words.markup/structureddocumenttagcollection/getbyid/
---
## StructuredDocumentTagCollection.GetById method

Returnerar den strukturerade dokumenttaggen med identifierare.

```csharp
public IStructuredDocumentTag GetById(int id)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| id | Int32 | Den strukturerade dokumenttaggens identifierare. |

### Anmärkningar

Returnerar null om den strukturerade dokumenttaggen med den angivna identifieraren inte kan hittas.

### Exempel

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
* namnutrymme [Aspose.Words.Markup](../../structureddocumenttagcollection/)
* hopsättning [Aspose.Words](../../../)


