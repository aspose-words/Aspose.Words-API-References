---
title: DocumentVisitor.VisitFieldEnd
second_title: Справочник по API Aspose.Words для .NET
description: DocumentVisitor метод. Вызывается когда поле заканчивается в документе.
type: docs
weight: 180
url: /ru/net/aspose.words/documentvisitor/visitfieldend/
---
## DocumentVisitor.VisitFieldEnd method

Вызывается, когда поле заканчивается в документе.

```csharp
public virtual VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldEnd | FieldEnd | Объект, который посещается. |

### Возвращаемое значение

А[`VisitorAction`](../../visitoraction/) значение, указывающее, как продолжить перечисление.

### Примечания

Для получения дополнительной информации см.[`VisitFieldStart`](../visitfieldstart/)

### Примеры

Показывает, как напечатать структуру узла каждого поля в документе.

```csharp
public void FieldToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    FieldStructurePrinter visitor = new FieldStructurePrinter();

    // Когда составной узел принимает посетителя документа, посетитель посещает принимающий узел,
    // а затем обходит все дочерние элементы узла в порядке глубины.
    // Посетитель может читать и изменять каждый посещаемый узел.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Обходит небинарное дерево дочерних узлов узла.
/// Создает карту в виде строки всех встреченных узлов Field и их дочерних элементов.
/// </summary>
public class FieldStructurePrinter : DocumentVisitor
{
    public FieldStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideField = false;
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел Run.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideField) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел FieldStart.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        IndentAndAppendLine("[Field start] FieldType: " + fieldStart.FieldType);
        mDocTraversalDepth++;
        mVisitorIsInsideField = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел FieldEnd.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Field end]");
        mVisitorIsInsideField = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел FieldSeparator.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        IndentAndAppendLine("[FieldSeparator]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Добавляем строку в StringBuilder и делаем отступ в зависимости от того, насколько глубоко находится посетитель
    /// в дерево дочерних узлов поля.
    /// </summary>
    /// <param name="text"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++)
        {
            mBuilder.Append("|  ");
        }

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideField;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Смотрите также

* enum [VisitorAction](../../visitoraction/)
* class [FieldEnd](../../../aspose.words.fields/fieldend/)
* class [DocumentVisitor](../)
* пространство имен [Aspose.Words](../../documentvisitor/)
* сборка [Aspose.Words](../../../)


