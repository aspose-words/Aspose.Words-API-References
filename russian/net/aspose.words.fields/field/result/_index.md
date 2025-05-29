---
title: Field.Result
linktitle: Result
articleTitle: Result
second_title: Aspose.Words для .NET
description: Управляйте свойствами результата поля без усилий. Получайте доступ к тексту между разделителями полей или изменяйте его для упрощения обработки данных и повышения эффективности.
type: docs
weight: 70
url: /ru/net/aspose.words.fields/field/result/
---
## Field.Result property

Возвращает или задает текст, который находится между разделителем полей и концом поля.

```csharp
public string Result { get; set; }
```

## Примеры

Показывает, как вставить поле в документ, используя код поля.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Эта перегрузка метода InsertField автоматически обновляет вставленные поля.
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

### Смотрите также

* class [Field](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
