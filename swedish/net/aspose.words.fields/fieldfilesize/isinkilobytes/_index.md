---
title: FieldFileSize.IsInKilobytes
linktitle: IsInKilobytes
articleTitle: IsInKilobytes
second_title: Aspose.Words för .NET
description: Kontrollera visningen av filstorleken med FieldFileSize IsInKilobytes. Växla enkelt mellan storleksvisning i kilobyte för förbättrad datahantering.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldfilesize/isinkilobytes/
---
## FieldFileSize.IsInKilobytes property

Hämtar eller anger om filstorleken ska visas i kilobyte.

```csharp
public bool IsInKilobytes { get; set; }
```

## Exempel

Visar hur man visar filstorleken för ett dokument med ett FILESIZE-fält.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(18105, doc.BuiltInDocumentProperties.Bytes);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertParagraph();

// Nedan följer tre olika måttenheter
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

// För att uppdatera värdena i dessa fält vid redigering i Microsoft Word,
// vi måste först spara ändringarna och sedan uppdatera dessa fält manuellt.
doc.Save(ArtifactsDir + "Field.FILESIZE.docx");
```

### Se även

* class [FieldFileSize](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
