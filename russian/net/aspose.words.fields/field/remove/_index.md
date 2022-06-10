---
title: Remove
second_title: Справочник по API Aspose.Words для .NET
description: Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла возвращает его родительский абзац. Если поле уже удалено возвращает null .
type: docs
weight: 120
url: /ru/net/aspose.words.fields/field/remove/
---
## Field.Remove method

Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает **null** .

```csharp
public Node Remove()
```

### Примеры

Показывает, как удалять поля из набора полей.

```csharp
{
    // Откройте документ Corel WordPerfect, который мы преобразовали в формат .docx.
    Document doc = new Document(MyDir + "Field sample - PRIVATE.docx");

    // Документы WordPerfect 5.x/6.x, подобные загруженному нами, могут содержать PRIVATE поля.
    // Microsoft Word сохраняет PRIVATE поля во время операций загрузки/сохранения,
    // но не предоставляет для них никакой функциональности.
    FieldPrivate field = (FieldPrivate)doc.Range.Fields[0];

    Assert.AreEqual(" PRIVATE \"My value\" ", field.GetFieldCode());
    Assert.AreEqual(FieldType.FieldPrivate, field.Type);

    // Мы также можем вставлять ЧАСТНЫЕ поля с помощью конструктора документов.
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(FieldType.FieldPrivate, true);

    // Эти поля не являются жизнеспособным способом защиты конфиденциальной информации.
    // Если не требуется обратная совместимость со старыми версиями WordPerfect,
    // мы можем безопасно удалить эти поля. Мы можем сделать это, используя реализацию DocumentVisiitor.
    Assert.AreEqual(2, doc.Range.Fields.Count);

    FieldPrivateRemover remover = new FieldPrivateRemover();
    doc.Accept(remover);

    Assert.AreEqual(2, remover.GetFieldsRemovedCount());
    Assert.AreEqual(0, doc.Range.Fields.Count);
}

/// <summary>
/// Удаляет все встречающиеся поля PRIVATE.
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
    /// Если узел принадлежит ЧАСТНОМУ полю, все поле удаляется.
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

Показывает, как обрабатывать PRIVATE поля.

```csharp
{
    // Откройте документ Corel WordPerfect, который мы преобразовали в формат .docx.
    Document doc = new Document(MyDir + "Field sample - PRIVATE.docx");

    // Документы WordPerfect 5.x/6.x, подобные загруженному нами, могут содержать PRIVATE поля.
    // Microsoft Word сохраняет PRIVATE поля во время операций загрузки/сохранения,
    // но не предоставляет для них никакой функциональности.
    FieldPrivate field = (FieldPrivate)doc.Range.Fields[0];

    Assert.AreEqual(" PRIVATE \"My value\" ", field.GetFieldCode());
    Assert.AreEqual(FieldType.FieldPrivate, field.Type);

    // Мы также можем вставлять ЧАСТНЫЕ поля с помощью конструктора документов.
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(FieldType.FieldPrivate, true);

    // Эти поля не являются жизнеспособным способом защиты конфиденциальной информации.
    // Если не требуется обратная совместимость со старыми версиями WordPerfect,
    // мы можем безопасно удалить эти поля. Мы можем сделать это, используя реализацию DocumentVisiitor.
    Assert.AreEqual(2, doc.Range.Fields.Count);

    FieldPrivateRemover remover = new FieldPrivateRemover();
    doc.Accept(remover);

    Assert.AreEqual(2, remover.GetFieldsRemovedCount());
    Assert.AreEqual(0, doc.Range.Fields.Count);
}

/// <summary>
/// Удаляет все встречающиеся поля PRIVATE.
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
    /// Если узел принадлежит ЧАСТНОМУ полю, все поле удаляется.
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

* class [Node](../../../aspose.words/node)
* class [Field](../../field)
* пространство имен [Aspose.Words.Fields](../../field)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
