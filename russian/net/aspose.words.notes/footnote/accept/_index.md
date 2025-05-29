---
title: Footnote.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words для .NET
description: Откройте для себя метод Footnote Accept для повышения вовлеченности посетителей и оптимизации пользовательского опыта вашего веб-сайта. Увеличьте конверсию сегодня!
type: docs
weight: 80
url: /ru/net/aspose.words.notes/footnote/accept/
---
## Footnote.Accept method

Принимает посетителя.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| visitor | DocumentVisitor | Посетитель, который посетит узлы. |

### Возвращаемое значение

True, если все узлы были посещены; false, если[`DocumentVisitor`](../../../aspose.words/documentvisitor/) остановил операцию до посещения всех узлов.

## Примечания

Перечисляет этот узел и всех его потомков. Каждый узел вызывает соответствующий метод на[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

Более подробную информацию см. в шаблоне проектирования «Посетитель».

Вызывает DocumentVisitor.VisitFootnoteStart, затем вызывает Accept для всех дочерних узлов сноски и вызывает DocumentVisitor.VisitFootnoteEnd в конце.

## Примеры

Показывает, как распечатать структуру узлов каждой сноски в документе.

```csharp
public void FootnoteToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    FootnoteStructurePrinter visitor = new FootnoteStructurePrinter();

    // Когда мы заставляем составной узел принять посетителя документа, посетитель посещает принимающий узел,
    // а затем обходит все дочерние узлы в глубину.
    // Посетитель может читать и изменять каждый посещенный узел.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Обходит недвоичное дерево дочерних узлов узла.
/// Создает карту в виде строки всех встреченных узлов сносок и их дочерних элементов.
/// </summary>
public class FootnoteStructurePrinter : DocumentVisitor
{
    public FootnoteStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideFootnote = false;
    }

    /// <summary>
    /// Получает простой текст документа, накопленный посетителем.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел сноски.
    /// </summary>
    public override VisitorAction VisitFootnoteStart(Footnote footnote)
    {
        IndentAndAppendLine("[Footnote start] Type: " + footnote.FootnoteType);
        mDocTraversalDepth++;
        mVisitorIsInsideFootnote = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается после посещения всех дочерних узлов узла сноски.
    /// </summary>
    public override VisitorAction VisitFootnoteEnd(Footnote footnote)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Footnote end]");
        mVisitorIsInsideFootnote = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел Run.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideFootnote) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

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

    private bool mVisitorIsInsideFootnote;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Смотрите также

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [Footnote](../)
* пространство имен [Aspose.Words.Notes](../../../aspose.words.notes/)
* сборка [Aspose.Words](../../../)
