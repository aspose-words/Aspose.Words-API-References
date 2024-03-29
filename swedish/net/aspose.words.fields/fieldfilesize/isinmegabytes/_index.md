---
title: FieldFileSize.IsInMegabytes
linktitle: IsInMegabytes
articleTitle: IsInMegabytes
second_title: Aspose.Words för .NET
description: FieldFileSize IsInMegabytes fast egendom. Hämtar eller ställer in om filstorleken ska visas i megabyte i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.fields/fieldfilesize/isinmegabytes/
---
## FieldFileSize.IsInMegabytes property

Hämtar eller ställer in om filstorleken ska visas i megabyte.

```csharp
public bool IsInMegabytes { get; set; }
```

## Exempel

Visar hur man visar filstorleken för ett dokument med ett FILESIZE-fält.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(18105, doc.BuiltInDocumentProperties.Bytes);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertParagraph();

// Nedan finns tre olika måttenheter
// med vilka FILESIZE-fält kan visa dokumentets filstorlek.
// 1 - Byte:
FieldFileSize field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.Update();

Assert.AreEqual(" FILESIZE ", field.GetFieldCode());
Assert.AreEqual("18105", field.Result);

// 2 - Kilobyte:
builder.InsertParagraph();
field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.IsInKilobytes = true;
field.Update();

Assert.AreEqual(" FILESIZE  \\k", field.GetFieldCode());
Assert.AreEqual("18", field.Result);

// 3 - Megabyte:
builder.InsertParagraph();
field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.IsInMegabytes = true;
field.Update();

Assert.AreEqual(" FILESIZE  \\m", field.GetFieldCode());
Assert.AreEqual("0", field.Result);

// För att uppdatera värdena för dessa fält medan du redigerar i Microsoft Word,
// vi måste först spara ändringarna och sedan uppdatera dessa fält manuellt.
doc.Save(ArtifactsDir + "Field.FILESIZE.docx");
```

### Se även

* class [FieldFileSize](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
