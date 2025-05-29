---
title: LoadOptions.UpdateDirtyFields
linktitle: UpdateDirtyFields
articleTitle: UpdateDirtyFields
second_title: Aspose.Words для .NET
description: Узнайте, как свойство LoadOptions UpdateDirtyFields повышает целостность данных, выборочно обновляя поля, помеченные как «грязные», для оптимальной производительности.
type: docs
weight: 160
url: /ru/net/aspose.words.loading/loadoptions/updatedirtyfields/
---
## LoadOptions.UpdateDirtyFields property

Указывает, следует ли обновлять поля с помощью`грязный` атрибут.

```csharp
public bool UpdateDirtyFields { get; set; }
```

## Примеры

Показывает, как использовать специальное свойство для обновления результата поля.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Присвойте встроенному свойству документа значение «Автор», а затем отобразите его с помощью поля.
doc.BuiltInDocumentProperties.Author = "John Doe";
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);

Assert.False(field.IsDirty);
Assert.AreEqual("John Doe", field.Result);

// Обновляем свойство. Поле по-прежнему отображает старое значение.
doc.BuiltInDocumentProperties.Author = "John & Jane Doe";

Assert.AreEqual("John Doe", field.Result);

// Поскольку значение поля устарело, мы можем пометить его как «грязное».
// Это значение останется устаревшим, пока мы не обновим поле вручную с помощью метода Field.Update().
field.IsDirty = true;

using (MemoryStream docStream = new MemoryStream())
{
    // Если мы сохраняем без вызова метода обновления,
    // в выходном документе поле будет по-прежнему отображать устаревшее значение.
    doc.Save(docStream, SaveFormat.Docx);

    // Объект LoadOptions имеет возможность обновить все поля
    // отмечен как «грязный» при загрузке документа.
    LoadOptions options = new LoadOptions();
    options.UpdateDirtyFields = updateDirtyFields;
    doc = new Document(docStream, options);

    Assert.AreEqual("John & Jane Doe", doc.BuiltInDocumentProperties.Author);

    field = (FieldAuthor)doc.Range.Fields[0];

    // Обновление грязных полей, подобное этому, автоматически устанавливает их флаг «IsDirty» в значение false.
    if (updateDirtyFields)
    {
        Assert.AreEqual("John & Jane Doe", field.Result);
        Assert.False(field.IsDirty);
    }
    else
    {
        Assert.AreEqual("John Doe", field.Result);
        Assert.True(field.IsDirty);
    }
}
```

### Смотрите также

* class [LoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
