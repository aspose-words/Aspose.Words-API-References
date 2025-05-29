---
title: Field.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words для .NET
description: Легко удаляйте поля из документов с помощью метода Field Remove. Получайте точные возвраты узлов и легко обрабатывайте пустые поля. Оптимизируйте свой рабочий процесс!
type: docs
weight: 120
url: /ru/net/aspose.words.fields/field/remove/
---
## Field.Remove method

Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля — последний child его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает`нулевой` .

```csharp
public Node Remove()
```

## Примеры

Показывает, как удалять поля из коллекции полей.

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

// Ниже приведены четыре способа удаления полей из коллекции полей.
// 1 - Получить поле для удаления:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - Получаем коллекцию для удаления поля, которое передаем ее методу удаления:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - Удалить поле из коллекции по индексу:
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - Удалить все поля из коллекции сразу:
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

Показывает, как обрабатывать ЧАСТНЫЕ поля.

```csharp
public void FieldPrivate()
{
    // Открываем документ Corel WordPerfect, который мы конвертировали в формат .docx.
    Document doc = new Document(MyDir + "Field sample - PRIVATE.docx");

    // Документы WordPerfect 5.x/6.x, подобные загруженному нами, могут содержать ЧАСТНЫЕ поля.
    // Microsoft Word сохраняет ЧАСТНЫЕ поля во время операций загрузки/сохранения,
    // но не предоставляет для них никакой функциональности.
    FieldPrivate field = (FieldPrivate)doc.Range.Fields[0];

    Assert.AreEqual(" PRIVATE \"My value\" ", field.GetFieldCode());
    Assert.AreEqual(FieldType.FieldPrivate, field.Type);

    // Мы также можем вставлять ЧАСТНЫЕ поля с помощью конструктора документов.
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(FieldType.FieldPrivate, true);

    // Эти поля не являются эффективным способом защиты конфиденциальной информации.
    // Если обратная совместимость со старыми версиями WordPerfect не является существенной,
    // мы можем безопасно удалить эти поля. Мы можем сделать это с помощью реализации DocumentVisiitor.
    Assert.AreEqual(2, doc.Range.Fields.Count);

    FieldPrivateRemover remover = new FieldPrivateRemover();
    doc.Accept(remover);

    Assert.AreEqual(2, remover.GetFieldsRemovedCount());
    Assert.AreEqual(0, doc.Range.Fields.Count);
}

/// <summary>
/// Удаляет все обнаруженные ЧАСТНЫЕ поля.
/// </summary>
public class FieldPrivateRemover : DocumentVisitor
{
    public FieldPrivateRemover()
    {
        mFieldsRemovedCount = 0;
    }

    public int GetFieldsRemovedCount()
    {
        return mFieldsRemovedCount;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел FieldEnd.
    /// Если узел принадлежит полю PRIVATE, удаляется все поле.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        if (fieldEnd.FieldType == FieldType.FieldPrivate)
        {
            fieldEnd.GetField().Remove();
            mFieldsRemovedCount++;
        }

        return VisitorAction.Continue;
    }

    private int mFieldsRemovedCount;
}
```

### Смотрите также

* class [Node](../../../aspose.words/node/)
* class [Field](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
