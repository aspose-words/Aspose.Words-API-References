---
title: FieldFileSize.IsInKilobytes
linktitle: IsInKilobytes
articleTitle: IsInKilobytes
second_title: Aspose.Words для .NET
description: Управляйте отображением размера файла с помощью FieldFileSize IsInKilobytes. Легко переключайте видимость размера в килобайтах для улучшенного управления данными.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldfilesize/isinkilobytes/
---
## FieldFileSize.IsInKilobytes property

Возвращает или задает, отображать ли размер файла в килобайтах.

```csharp
public bool IsInKilobytes { get; set; }
```

## Примеры

Показывает, как отобразить размер файла документа с помощью поля FILESIZE.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(18105, doc.BuiltInDocumentProperties.Bytes);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertParagraph();

// Ниже приведены три различные единицы измерения.
// с помощью которых поля FILESIZE могут отображать размер файла документа.
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

// 3 - Мегабайт:
builder.InsertParagraph();
field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.IsInMegabytes = true;
field.Update();

Assert.AreEqual(" FILESIZE  \\m", field.GetFieldCode());
Assert.AreEqual("0", field.Result);

// Чтобы обновить значения этих полей при редактировании в Microsoft Word,
// сначала необходимо сохранить изменения, а затем вручную обновить эти поля.
doc.Save(ArtifactsDir + "Field.FILESIZE.docx");
```

### Смотрите также

* class [FieldFileSize](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
