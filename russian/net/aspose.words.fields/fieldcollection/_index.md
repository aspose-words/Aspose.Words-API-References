---
title: Class FieldCollection
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Fields.FieldCollection сорт. КоллекцияField объекты представляющие поля в указанном диапазоне.
type: docs
weight: 1540
url: /ru/net/aspose.words.fields/fieldcollection/
---
## FieldCollection class

Коллекция[`Field`](../field/) объекты, представляющие поля в указанном диапазоне.

```csharp
public class FieldCollection : IEnumerable<Field>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.fields/fieldcollection/count/) { get; } | Возвращает количество полей в коллекции. |
| [Item](../../aspose.words.fields/fieldcollection/item/) { get; } | Возвращает поле по указанному индексу. |

## Методы

| Имя | Описание |
| --- | --- |
| [Clear](../../aspose.words.fields/fieldcollection/clear/)() | Удаляет все поля этой коллекции из документа и из самой этой коллекции. |
| [GetEnumerator](../../aspose.words.fields/fieldcollection/getenumerator/)() | Возвращает объект перечислителя. |
| [Remove](../../aspose.words.fields/fieldcollection/remove/)(Field) | Удаляет указанное поле из этой коллекции и из документа. |
| [RemoveAt](../../aspose.words.fields/fieldcollection/removeat/)(int) | Удаляет поле с указанным индексом из этой коллекции и из документа. |

### Примечания

Экземпляр этой коллекции перебирает поля, которые начинают попадать в указанный диапазон.

`FieldCollection` коллекция не владеет содержащимися в ней полями, а представляет собой просто набор полей.

`FieldCollection` коллекция является "живой", т.е. изменения дочерних элементов узла object , из которого она была создана, немедленно отражаются в полях, возвращаемых`FieldCollection` свойства и методы.

### Примеры

Показывает, как удалить поля из коллекции полей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
builder.InsertField(" TIME ");
builder.InsertField(" REVNUM ");
builder.InsertField(" AUTHOR  \"John Doe\" ");
builder.InsertField(" SUBJECT \"My Subject\" ");
builder.InsertField(" QUOTE \"Hello world!\" ");
doc.UpdateFields();

FieldCollection fields = doc.Range.Fields;

Assert.AreEqual(6, fields.Count);

// Ниже приведены четыре способа удаления полей из набора полей.
// 1 - Получить поле для удаления самого себя:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - Получить коллекцию для удаления поля, которое мы передаем в метод ее удаления:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - Удалить поле из коллекции по индексу:
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - Удалить сразу все поля из коллекции:
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

Показывает, как работать с коллекцией полей.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
    builder.InsertField(" TIME ");
    builder.InsertField(" REVNUM ");
    builder.InsertField(" AUTHOR  \"John Doe\" ");
    builder.InsertField(" SUBJECT \"My Subject\" ");
    builder.InsertField(" QUOTE \"Hello world!\" ");
    doc.UpdateFields();

    FieldCollection fields = doc.Range.Fields;

    Assert.AreEqual(6, fields.Count);

    // Перебираем коллекцию полей и печатаем содержимое и тип
    // каждого поля с использованием пользовательской реализации посетителя.
    FieldVisitor fieldVisitor = new FieldVisitor();

    using (IEnumerator<Field> fieldEnumerator = fields.GetEnumerator())
    {
        while (fieldEnumerator.MoveNext())
        {
            if (fieldEnumerator.Current != null)
            {
                fieldEnumerator.Current.Start.Accept(fieldVisitor);
                fieldEnumerator.Current.Separator?.Accept(fieldVisitor);
                fieldEnumerator.Current.End.Accept(fieldVisitor);
            }
            else
            {
                Console.WriteLine("There are no fields in the document.");
            }
        }
    }

    Console.WriteLine(fieldVisitor.GetText());

/// <summary>
/// Реализация посетителя документа, которая печатает информацию о поле.
/// </summary>
public class FieldVisitor : DocumentVisitor
{
    public FieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Получает обычный текст документа, который накопил посетитель.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел FieldStart.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        mBuilder.AppendLine("Found field: " + fieldStart.FieldType);
        mBuilder.AppendLine("\tField code: " + fieldStart.GetField().GetFieldCode());
        mBuilder.AppendLine("\tDisplayed as: " + fieldStart.GetField().Result);

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел FieldSeparator.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        mBuilder.AppendLine("\tFound separator: " + fieldSeparator.GetText());

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел FieldEnd.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mBuilder.AppendLine("End of field: " + fieldEnd.FieldType);

        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
}
```

### Смотрите также

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)


