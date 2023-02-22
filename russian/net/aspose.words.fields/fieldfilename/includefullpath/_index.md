---
title: FieldFileName.IncludeFullPath
second_title: Справочник по API Aspose.Words для .NET
description: FieldFileName свойство. Получает или задает следует ли включать полный путь к файлу.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldfilename/includefullpath/
---
## FieldFileName.IncludeFullPath property

Получает или задает, следует ли включать полный путь к файлу.

```csharp
public bool IncludeFullPath { get; set; }
```

### Примеры

Показывает, как использовать FieldOptions для переопределения значения по умолчанию для поля FILENAME.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
builder.Writeln();

// В этом поле FILENAME будет отображаться имя локального системного файла документа, который мы загрузили.
FieldFileName field = (FieldFileName)builder.InsertField(FieldType.FieldFileName, true);
field.Update();

Assert.AreEqual(" FILENAME ", field.GetFieldCode());
Assert.AreEqual("Document.docx", field.Result);

builder.Writeln();

// По умолчанию в поле FILENAME отображается имя файла, но не полный путь к нему в локальной файловой системе.
// Мы можем установить флаг, чтобы показать полный путь к файлу.
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

* class [FieldFileName](../)
* пространство имен [Aspose.Words.Fields](../../fieldfilename/)
* сборка [Aspose.Words](../../../)


