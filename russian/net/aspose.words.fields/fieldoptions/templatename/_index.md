---
title: FieldOptions.TemplateName
second_title: Справочник по API Aspose.Words для .NET
description: FieldOptions свойство. Получает или задает имя файла шаблона используемого документом.
type: docs
weight: 190
url: /ru/net/aspose.words.fields/fieldoptions/templatename/
---
## FieldOptions.TemplateName property

Получает или задает имя файла шаблона, используемого документом.

```csharp
public string TemplateName { get; set; }
```

### Примечания

Это свойство используется[`FieldTemplate`](../../fieldtemplate/) поле, если[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) недвижимость пуста.

Если это свойство пусто, имя файла шаблона по умолчанию`Нормальный.dotm` используется.

### Примеры

Показывает, как использовать поле ШАБЛОН для отображения местоположения шаблона документа в локальной файловой системе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Мы можем установить имя шаблона, используя поля. Это свойство используется, когда «doc.AttachedTemplate» пуст.
// Если это свойство пусто, используется имя файла шаблона по умолчанию «Normal.dotm».
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

* class [FieldOptions](../)
* пространство имен [Aspose.Words.Fields](../../fieldoptions/)
* сборка [Aspose.Words](../../../)


