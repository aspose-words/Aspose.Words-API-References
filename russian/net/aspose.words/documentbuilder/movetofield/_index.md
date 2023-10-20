---
title: DocumentBuilder.MoveToField
linktitle: MoveToField
articleTitle: MoveToField
second_title: Aspose.Words для .NET
description: DocumentBuilder MoveToField метод. Перемещает курсор в поле документа на С#.
type: docs
weight: 530
url: /ru/net/aspose.words/documentbuilder/movetofield/
---
## DocumentBuilder.MoveToField method

Перемещает курсор в поле документа.

```csharp
public void MoveToField(Field field, bool isAfter)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| field | Field | Поле, на которое необходимо переместить курсор. |
| isAfter | Boolean | Когда`истинный` , перемещает курсор после конца поля. Когда`ЛОЖЬ`, перемещает курсор до начала поля. |

## Примеры

Показывает, как переместить курсор точки вставки узла компоновщика документов в определенное поле.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте поле с помощью DocumentBuilder и добавьте после него текст.
Field field = builder.InsertField(" AUTHOR \"John Doe\" ");

// Курсор конструктора сейчас находится в конце документа.
Assert.Null(builder.CurrentNode);

// Переместите курсор в поле, указав, следует ли разместить этот курсор до или после поля.
builder.MoveToField(field, moveCursorToAfterTheField);

// Обратите внимание, что в обоих случаях курсор находится за пределами поля.
// Это означает, что мы не можем редактировать поле с помощью построителя таким образом.
// Чтобы отредактировать поле, мы можем использовать метод компоновщика MoveTo для FieldStart поля.
// или узел FieldSeparator, чтобы поместить внутрь курсор.
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
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
