---
title: Run.Accept
second_title: Справочник по API Aspose.Words для .NET
description: Run метод. Принимает посетителя.
type: docs
weight: 40
url: /ru/net/aspose.words/run/accept/
---
## Run.Accept method

Принимает посетителя.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| visitor | DocumentVisitor | Посетитель, который посетит узел. |

### Возвращаемое значение

False, если посетитель запросил остановку перечисления.

### Примечания

Вызывает DocumentVisitor.VisitRun.

Дополнительные сведения см. в шаблоне проектирования «Посетитель».

### Примеры

Показывает, как напечатать структуру узла каждого верхнего и нижнего колонтитула в документе.

```csharp
public void HeaderFooterToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    HeaderFooterStructurePrinter visitor = new HeaderFooterStructurePrinter();

    // Когда составной узел принимает посетителя документа, посетитель посещает принимающий узел,
    // а затем обходит все дочерние элементы узла в порядке глубины.
    // Посетитель может читать и изменять каждый посещаемый узел.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());

    // Альтернативный способ доступа к верхнему/нижнему колонтитулу документа по разделам — доступ к коллекции.
    HeaderFooter[] headerFooters = doc.FirstSection.HeadersFooters.ToArray();
    Assert.AreEqual(3, headerFooters.Length);
}

/// <summary>
/// Обходит небинарное дерево дочерних узлов узла.
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

* class [DocumentVisitor](../../documentvisitor/)
* class [Run](../)
* пространство имен [Aspose.Words](../../run/)
* сборка [Aspose.Words](../../../)


