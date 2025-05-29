---
title: FieldTemplate.IncludeFullPath
linktitle: IncludeFullPath
articleTitle: IncludeFullPath
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldTemplate IncludeFullPath, которое позволяет легко управлять включением полного пути к файлу, повышая эффективность и организованность вашего проекта.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldtemplate/includefullpath/
---
## FieldTemplate.IncludeFullPath property

Возвращает или задает, следует ли включать полное имя пути к файлу.

```csharp
public bool IncludeFullPath { get; set; }
```

## Примеры

Показывает, как использовать поле ШАБЛОН для отображения местоположения шаблона документа в локальной файловой системе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Мы можем задать имя шаблона, используя поля. Это свойство используется, когда "doc.AttachedTemplate" пуст.
// Если это свойство пустое, используется имя файла шаблона по умолчанию «Normal.dotm».
doc.FieldOptions.TemplateName = string.Empty;

FieldTemplate field = (FieldTemplate)builder.InsertField(FieldType.FieldTemplate, false);
Assert.AreEqual(" TEMPLATE ", field.GetFieldCode());

builder.Writeln();
field = (FieldTemplate)builder.InsertField(FieldType.FieldTemplate, false);
field.IncludeFullPath = true;

Assert.AreEqual(" TEMPLATE  \\p", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TEMPLATE.docx");
```

### Смотрите также

* class [FieldTemplate](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
