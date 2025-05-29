---
title: FieldOptions.FileName
linktitle: FileName
articleTitle: FileName
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldOptions FileName, которое позволяет легко управлять именем файла документа и настраивать его для лучшей организации и эффективности.
type: docs
weight: 140
url: /ru/net/aspose.words.fields/fieldoptions/filename/
---
## FieldOptions.FileName property

Возвращает или задает имя файла документа.

```csharp
public string FileName { get; set; }
```

## Примечания

Это свойство используется[`FieldFileName`](../../fieldfilename/) поле с более высоким приоритетом, чем[`OriginalFileName`](../../../aspose.words/document/originalfilename/) свойство.

## Примеры

Показывает, как использовать FieldOptions для переопределения значения по умолчанию для поля FILENAME.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
builder.Writeln();

// В этом поле FILENAME будет отображаться имя файла локальной системы загруженного нами документа.
FieldFileName field = (FieldFileName)builder.InsertField(FieldType.FieldFileName, true);
field.Update();

Assert.AreEqual(" FILENAME ", field.GetFieldCode());
Assert.AreEqual("Document.docx", field.Result);

builder.Writeln();

// По умолчанию поле FILENAME показывает имя файла, но не его полный путь в локальной файловой системе.
// Мы можем установить флаг, чтобы отображался полный путь к файлу.
field = (FieldFileName)builder.InsertField(FieldType.FieldFileName, true);
field.IncludeFullPath = true;
field.Update();

Assert.AreEqual(MyDir + "Document.docx", field.Result);

// Мы также можем установить значение для этого свойства
// переопределить значение, отображаемое в поле FILENAME.
doc.FieldOptions.FileName = "FieldOptions.FILENAME.docx";
field.Update();

Assert.AreEqual(" FILENAME  \\p", field.GetFieldCode());
Assert.AreEqual("FieldOptions.FILENAME.docx", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + doc.FieldOptions.FileName);
```

### Смотрите также

* class [FieldOptions](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
