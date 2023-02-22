---
title: FieldFileSize.IsInKilobytes
second_title: Справочник по API Aspose.Words для .NET
description: FieldFileSize свойство. Получает или задает отображать ли размер файла в килобайтах.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldfilesize/isinkilobytes/
---
## FieldFileSize.IsInKilobytes property

Получает или задает, отображать ли размер файла в килобайтах.

```csharp
public bool IsInKilobytes { get; set; }
```

### Примеры

Показывает, как отобразить размер файла документа с полем FILESIZE.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(18105, doc.BuiltInDocumentProperties.Bytes);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertParagraph();

// Ниже представлены три разные единицы измерения
// с помощью которых поля FILESIZE могут отображать размер файла документа.
// 1 - Байты:
FieldFileSize field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.Update();

Assert.AreEqual(" FILESIZE ", field.GetFieldCode());
Assert.AreEqual("18105", field.Result);

// 2 - Килобайт:
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
* пространство имен [Aspose.Words.Fields](../../fieldfilesize/)
* сборка [Aspose.Words](../../../)


