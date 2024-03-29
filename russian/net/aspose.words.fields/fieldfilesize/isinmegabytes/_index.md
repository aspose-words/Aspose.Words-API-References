---
title: FieldFileSize.IsInMegabytes
linktitle: IsInMegabytes
articleTitle: IsInMegabytes
second_title: Aspose.Words для .NET
description: FieldFileSize IsInMegabytes свойство. Получает или задает отображать ли размер файла в мегабайтах на С#.
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldfilesize/isinmegabytes/
---
## FieldFileSize.IsInMegabytes property

Получает или задает, отображать ли размер файла в мегабайтах.

```csharp
public bool IsInMegabytes { get; set; }
```

## Примеры

Показывает, как отобразить размер файла документа с помощью поля FILESIZE.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(18105, doc.BuiltInDocumentProperties.Bytes);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertParagraph();

// Ниже приведены три разные единицы измерения
// с помощью которого поля FILESIZE могут отображать размер файла документа.
// 1 - Байты:
FieldFileSize field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.Update();

Assert.AreEqual(" FILESIZE ", field.GetFieldCode());
Assert.AreEqual("18105", field.Result);

// 2 - Килобайты:
builder.InsertParagraph();
field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.IsInKilobytes = true;
field.Update();

Assert.AreEqual(" FILESIZE  \\k", field.GetFieldCode());
Assert.AreEqual("18", field.Result);

// 3 - Мегабайты:
builder.InsertParagraph();
field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.IsInMegabytes = true;
field.Update();

Assert.AreEqual(" FILESIZE  \\m", field.GetFieldCode());
Assert.AreEqual("0", field.Result);

// Чтобы обновить значения этих полей при редактировании в Microsoft Word,
// мы должны сначала сохранить изменения, а затем вручную обновить эти поля.
doc.Save(ArtifactsDir + "Field.FILESIZE.docx");
```

### Смотрите также

* class [FieldFileSize](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
