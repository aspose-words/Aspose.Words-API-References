---
title: FieldFileName.IncludeFullPath
linktitle: IncludeFullPath
articleTitle: IncludeFullPath
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldFileName IncludeFullPath, легко управляйте путями к файлам с помощью настраиваемых параметров для улучшенной обработки и организации файлов.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldfilename/includefullpath/
---
## FieldFileName.IncludeFullPath property

Возвращает или задает, следует ли включать полное имя пути к файлу.

```csharp
public bool IncludeFullPath { get; set; }
```

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

* class [FieldFileName](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
