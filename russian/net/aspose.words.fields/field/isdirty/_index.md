---
title: Field.IsDirty
linktitle: IsDirty
articleTitle: IsDirty
second_title: Aspose.Words для .NET
description: Управляйте свойством IsDirty, чтобы гарантировать точность и актуальность полевых данных, повышая целостность и производительность документов.
type: docs
weight: 40
url: /ru/net/aspose.words.fields/field/isdirty/
---
## Field.IsDirty property

Возвращает или задает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ.

```csharp
public bool IsDirty { get; set; }
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

* class [Field](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
