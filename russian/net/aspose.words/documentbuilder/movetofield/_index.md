---
title: DocumentBuilder.MoveToField
second_title: Справочник по API Aspose.Words для .NET
description: DocumentBuilder метод. Перемещает курсор в поле документа.
type: docs
weight: 510
url: /ru/net/aspose.words/documentbuilder/movetofield/
---
## DocumentBuilder.MoveToField method

Перемещает курсор в поле документа.

```csharp
public void MoveToField(Field field, bool isAfter)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| field | Field | Поле для перемещения курсора. |
| isAfter | Boolean | При значении true курсор перемещается после конца поля. При значении false курсор перемещается перед началом поля. |

### Примеры

Показывает, как переместить курсор точки вставки узла компоновщика документов в определенное поле.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем поле с помощью DocumentBuilder и добавляем после него текст.
Field field = builder.InsertField(" AUTHOR \"John Doe\" ");

// Курсор построителя в настоящее время находится в конце документа.
Assert.Null(builder.CurrentNode);

// Переместите курсор в поле, указав, следует ли размещать этот курсор до или после поля.
builder.MoveToField(field, moveCursorToAfterTheField);

// Обратите внимание, что курсор находится за пределами поля в обоих случаях.
// Это означает, что мы не можем редактировать поле с помощью конструктора вот так.
// Чтобы отредактировать поле, мы можем использовать метод MoveTo построителя для поля FieldStart
// или узел FieldSeparator для размещения внутри него курсора.
if (moveCursorToAfterTheField)
{
    Assert.Null(builder.CurrentNode);
    builder.Write(" Text immediately after the field.");

    Assert.AreEqual("\u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015 Text immediately after the field.", 
        doc.GetText().Trim());
}
else
{
    Assert.AreEqual(field.Start, builder.CurrentNode);
    builder.Write("Text immediately before the field. ");

    Assert.AreEqual("Text immediately before the field. \u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015", 
        doc.GetText().Trim());
}
```

### Смотрите также

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)


