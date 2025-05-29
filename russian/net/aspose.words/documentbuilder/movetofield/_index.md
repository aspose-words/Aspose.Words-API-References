---
title: DocumentBuilder.MoveToField
linktitle: MoveToField
articleTitle: MoveToField
second_title: Aspose.Words для .NET
description: Легко перемещайтесь по документам с помощью метода MoveToField в DocumentBuilder, который позволяет быстро перемещать курсор в любое поле для повышения эффективности редактирования.
type: docs
weight: 570
url: /ru/net/aspose.words/documentbuilder/movetofield/
---
## DocumentBuilder.MoveToField method

Перемещает курсор в поле в документе.

```csharp
public void MoveToField(Field field, bool isAfter)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| field | Field | Поле, в которое необходимо переместить курсор. |
| isAfter | Boolean | Когда`истинный` , перемещает курсор в положение после конца поля. Когда`ЛОЖЬ`, перемещает курсор в положение перед началом поля. |

## Примеры

Показывает, как переместить курсор точки вставки узла конструктора документов в определенное поле.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте поле с помощью DocumentBuilder и добавьте после него текст.
Field field = builder.InsertField(" AUTHOR \"John Doe\" ");

// Курсор конструктора в данный момент находится в конце документа.
Assert.Null(builder.CurrentNode);

// Перемещаем курсор в поле, указывая, следует ли поместить курсор до или после поля.
builder.MoveToField(field, moveCursorToAfterTheField);

// Обратите внимание, что в обоих случаях курсор находится за пределами поля.
// Это означает, что мы не можем редактировать поле с помощью конструктора таким образом.
// Чтобы редактировать поле, мы можем использовать метод MoveTo конструктора для FieldStart поля
// или узел FieldSeparator для размещения курсора внутри.
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
