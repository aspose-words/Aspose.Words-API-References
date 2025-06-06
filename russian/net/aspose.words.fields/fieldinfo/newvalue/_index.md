---
title: FieldInfo.NewValue
linktitle: NewValue
articleTitle: NewValue
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldInfo NewValue, легко управляйте дополнительными значениями, чтобы улучшить обновления данных и оптимизировать процесс кодирования.
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldinfo/newvalue/
---
## FieldInfo.NewValue property

Возвращает или задает необязательное значение, которое обновляет свойство.

```csharp
public string NewValue { get; set; }
```

## Примеры

Показывает, как работать с полями INFO.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Задайте значение для встроенного свойства «Комментарии», а затем вставьте поле INFO для отображения значения этого свойства.
doc.BuiltInDocumentProperties.Comments = "My comment";
FieldInfo field = (FieldInfo)builder.InsertField(FieldType.FieldInfo, true);
field.InfoType = "Comments";
field.Update();

Assert.AreEqual(" INFO  Comments", field.GetFieldCode());
Assert.AreEqual("My comment", field.Result);

builder.Writeln();

// Установка значения для свойства NewValue поля и обновление
// поле также перезапишет соответствующее встроенное свойство новым значением.
field = (FieldInfo)builder.InsertField(FieldType.FieldInfo, true);
field.InfoType = "Comments";
field.NewValue = "New comment";
field.Update();

Assert.AreEqual(" INFO  Comments \"New comment\"", field.GetFieldCode());
Assert.AreEqual("New comment", field.Result);
Assert.AreEqual("New comment", doc.BuiltInDocumentProperties.Comments);

doc.Save(ArtifactsDir + "Field.INFO.docx");
```

### Смотрите также

* class [FieldInfo](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
