---
title: Document.AcceptEnd
linktitle: AcceptEnd
articleTitle: AcceptEnd
second_title: Aspose.Words для .NET
description: Изучите метод Document AcceptEnd для эффективного управления доступом посетителей в конце документа. Улучшите пользовательский опыт с помощью бесшовной навигации.
type: docs
weight: 550
url: /ru/net/aspose.words/document/acceptend/
---
## Document.AcceptEnd method

Принимает посетителя для посещения конца документа.

```csharp
public override VisitorAction AcceptEnd(DocumentVisitor visitor)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| visitor | DocumentVisitor | Посетитель документа. |

### Возвращаемое значение

Действие, которое должен предпринять посетитель.

## Примеры

Показывает, как использовать посетитель документа для печати структуры узлов документа.

```csharp
public void DocStructureToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    DocStructurePrinter visitor = new DocStructurePrinter();

    // Когда мы заставляем составной узел принять посетителя документа, посетитель посещает принимающий узел,
    // а затем обходит все дочерние узлы в глубину.
    // Посетитель может читать и изменять каждый посещенный узел.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Обходит дерево дочерних узлов узла.
/// Создает карту этого дерева в виде строки.
/// </summary>
public class DocStructurePrinter : DocumentVisitor
{
    public DocStructurePrinter()
    {
        mAcceptingNodeChildTree = new StringBuilder();
    }

    public string GetText()
    {
        return mAcceptingNodeChildTree.ToString();
    }

    /// <summary>
    /// Вызывается при обнаружении узла документа.
    /// </summary>
    public override VisitorAction VisitDocumentStart(Document doc)
    {
        int childNodeCount = doc.GetChildNodes(NodeType.Any, true).Count;

        IndentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
        mDocTraversalDepth++;

        // Разрешить посетителю продолжить посещение других узлов.
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается после посещения всех дочерних узлов узла Document.
    /// </summary>
    public override VisitorAction VisitDocumentEnd(Document doc)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Document end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел Раздела.
    /// </summary>
    public override VisitorAction VisitSectionStart(Section section)
    {
        // Получаем индекс нашего раздела в документе.
        NodeCollection docSections = section.Document.GetChildNodes(NodeType.Section, false);
        int sectionIndex = docSections.IndexOf(section);

        IndentAndAppendLine("[Section start] Section index: " + sectionIndex);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается после посещения всех дочерних узлов узла Section.
    /// </summary>
    public override VisitorAction VisitSectionEnd(Section section)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Section end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел Body.
    /// </summary>
    public override VisitorAction VisitBodyStart(Body body)
    {
        int paragraphCount = body.Paragraphs.Count;
        IndentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается после посещения всех дочерних узлов узла Body.
    /// </summary>
    public override VisitorAction VisitBodyEnd(Body body)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Body end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел «Абзац».
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        IndentAndAppendLine("[Paragraph start]");
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается после посещения всех дочерних узлов узла Paragraph.
    /// </summary>
    public override VisitorAction VisitParagraphEnd(Paragraph paragraph)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Paragraph end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел Run.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел SubDocument.
    /// </summary>
    public override VisitorAction VisitSubDocument(SubDocument subDocument)
    {
        IndentAndAppendLine("[SubDocument]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел SubDocument.
    /// </summary>
    public override VisitorAction VisitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)
    {
        IndentAndAppendLine("[SdtRangeStart]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел SubDocument.
    /// </summary>
    public override VisitorAction VisitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)
    {
        IndentAndAppendLine("[SdtRangeEnd]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Добавляем строку в StringBuilder и делаем отступ в зависимости от того, насколько глубоко посетитель находится в дереве документа.
    /// </summary>
    /// <param name="text"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mAcceptingNodeChildTree.Append("|  ");

        mAcceptingNodeChildTree.AppendLine(text);
    }

    private int mDocTraversalDepth;
    private readonly StringBuilder mAcceptingNodeChildTree;
}
```

### Смотрите также

* enum [VisitorAction](../../visitoraction/)
* class [DocumentVisitor](../../documentvisitor/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
