---
title: StructuredDocumentTagCollection.GetById
linktitle: GetById
articleTitle: GetById
second_title: Aspose.Words för .NET
description: Hämta strukturerade dokumenttaggar utan problem med GetById-metoden. Få snabb åtkomst till dina data och effektivisera dokumenthanteringen.
type: docs
weight: 30
url: /sv/net/aspose.words.markup/structureddocumenttagcollection/getbyid/
---
## StructuredDocumentTagCollection.GetById method

Returnerar den strukturerade dokumenttaggen efter identifierare.

```csharp
public IStructuredDocumentTag GetById(int id)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| id | Int32 | Taggidentifieraren för det strukturerade dokumentet. |

## Anmärkningar

Returnerar null om den strukturerade dokumenttaggen med den angivna identifieraren inte kan hittas.

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
