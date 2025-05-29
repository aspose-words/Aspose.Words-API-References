---
title: DocumentVisitor.VisitHeaderFooterEnd
linktitle: VisitHeaderFooterEnd
articleTitle: VisitHeaderFooterEnd
second_title: Aspose.Words для .NET
description: Откройте для себя метод DocumentVisitor VisitHeaderFooterEnd, необходимый для эффективного управления перечислением верхних и нижних колонтитулов в ваших документах.
type: docs
weight: 280
url: /ru/net/aspose.words/documentvisitor/visitheaderfooterend/
---
## DocumentVisitor.VisitHeaderFooterEnd method

Вызывается, когда перечисление верхнего или нижнего колонтитула в разделе завершено.

```csharp
public virtual VisitorAction VisitHeaderFooterEnd(HeaderFooter headerFooter)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| headerFooter | HeaderFooter | Посещаемый объект. |

### Возвращаемое значение

А[`VisitorAction`](../../visitoraction/) значение, указывающее, как продолжить перечисление.

## Примеры

Показывает, как распечатать структуру узлов каждого верхнего и нижнего колонтитула в документе.

```csharp
public void HeaderFooterToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    HeaderFooterStructurePrinter visitor = new HeaderFooterStructurePrinter();

    // Когда мы заставляем составной узел принять посетителя документа, посетитель посещает принимающий узел,
    // а затем обходит все дочерние узлы в глубину.
    // Посетитель может читать и изменять каждый посещенный узел.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());

    // Альтернативный способ доступа к верхним и нижним колонтитулам документа по разделам — доступ к коллекции.
    HeaderFooter[] headerFooters = doc.FirstSection.HeadersFooters.ToArray();
    Assert.AreEqual(3, headerFooters.Length);
}

/// <summary>
/// Обходит недвоичное дерево дочерних узлов узла.
/// Создает карту в виде строки всех встреченных узлов HeaderFooter и их дочерних элементов.
/// </summary>
public class HeaderFooterStructurePrinter : DocumentVisitor
{
    public HeaderFooterStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideHeaderFooter = false;
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
        if (mVisitorIsInsideHeaderFooter) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел HeaderFooter.
    /// </summary>
    public override VisitorAction VisitHeaderFooterStart(HeaderFooter headerFooter)
    {
        IndentAndAppendLine("[HeaderFooter start] HeaderFooterType: " + headerFooter.HeaderFooterType);
        mDocTraversalDepth++;
        mVisitorIsInsideHeaderFooter = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается после посещения всех дочерних узлов узла HeaderFooter.
    /// </summary>
    public override VisitorAction VisitHeaderFooterEnd(HeaderFooter headerFooter)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[HeaderFooter end]");
        mVisitorIsInsideHeaderFooter = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Добавляем строку в StringBuilder и делаем отступ в зависимости от того, насколько глубоко посетитель находится в дереве документа.
    /// </summary>
    /// <param name="text"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideHeaderFooter;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Смотрите также

* enum [VisitorAction](../../visitoraction/)
* class [HeaderFooter](../../headerfooter/)
* class [DocumentVisitor](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
