---
title: CommentRangeEnd.CommentRangeEnd
second_title: Справочник по API Aspose.Words для .NET
description: CommentRangeEnd строитель. Инициализирует новый экземпляр этого класса.
type: docs
weight: 10
url: /ru/net/aspose.words/commentrangeend/commentrangeend/
---
## CommentRangeEnd constructor

Инициализирует новый экземпляр этого класса.

```csharp
public CommentRangeEnd(DocumentBase doc, int id)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | DocumentBase | Документ владельца. |
| id | Int32 | Идентификатор комментария, с которым связан этот объект. |

### Примечания

Когда[`CommentRangeEnd`](../) создан, он принадлежит указанному документу, но не является частью документа и[`ParentNode`](../../node/parentnode/) нулевой.

Чтобы добавить[`CommentRangeEnd`](../) к документу используйте InsertAfter или InsertBefore в абзаце, куда вы хотите вставить комментарий.

### Примеры

Показывает, как распечатать содержимое всех комментариев и их диапазоны комментариев с помощью посетителя документа.

```csharp
public void CreateCommentsAndPrintAllInfo()
{
    Document doc = new Document();

    Comment newComment = new Comment(doc)
    {
        Author = "VDeryushev",
        Initial = "VD",
        DateTime = DateTime.Now
    };

    newComment.SetText("Comment regarding text.");

    // Добавьте текст в документ, деформируйте его в диапазоне комментариев, а затем добавьте свой комментарий.
    Paragraph para = doc.FirstSection.Body.FirstParagraph;
    para.AppendChild(new CommentRangeStart(doc, newComment.Id));
    para.AppendChild(new Run(doc, "Commented text."));
    para.AppendChild(new CommentRangeEnd(doc, newComment.Id));
    para.AppendChild(newComment); 

    // Добавляем два ответа на комментарий.
    newComment.AddReply("John Doe", "JD", DateTime.Now, "New reply.");
    newComment.AddReply("John Doe", "JD", DateTime.Now, "Another reply.");

    PrintAllCommentInfo(doc.GetChildNodes(NodeType.Comment, true));
}

/// <summary>
/// Перебирает каждый комментарий верхнего уровня и печатает его диапазон комментариев, содержимое и ответы.
/// </summary>
private static void PrintAllCommentInfo(NodeCollection comments)
{
    CommentInfoPrinter commentVisitor = new CommentInfoPrinter();

    // Перебираем все комментарии верхнего уровня. В отличие от комментариев типа ответа, комментарии верхнего уровня не имеют предка.
    foreach (Comment comment in comments.Where(c => ((Comment)c).Ancestor == null))
    {
        // Во-первых, посетите начало диапазона комментариев.
        CommentRangeStart commentRangeStart = (CommentRangeStart)comment.PreviousSibling.PreviousSibling.PreviousSibling;
        commentRangeStart.Accept(commentVisitor);

        // Затем перейдите к комментарию и любым возможным ответам на него.
        comment.Accept(commentVisitor);

        foreach (Comment reply in comment.Replies)
            reply.Accept(commentVisitor);

        // Наконец, перейдите в конец диапазона комментариев, а затем распечатайте текстовое содержимое посетителя.
        CommentRangeEnd commentRangeEnd = (CommentRangeEnd)comment.PreviousSibling;
        commentRangeEnd.Accept(commentVisitor);

        Console.WriteLine(commentVisitor.GetText());
    }
}

/// <summary>
/// Выводит информацию и содержимое всех комментариев и диапазонов комментариев, встречающихся в документе.
/// </summary>
public class CommentInfoPrinter : DocumentVisitor
{
    public CommentInfoPrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideComment = false;
    }

    /// <summary>
    /// Получает обычный текст документа, который накопил посетитель.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел Run.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideComment) IndentAndAppendLine("[Run] \"" + run.Text + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел CommentRangeStart.
    /// </summary>
    public override VisitorAction VisitCommentRangeStart(CommentRangeStart commentRangeStart)
    {
        IndentAndAppendLine("[Comment range start] ID: " + commentRangeStart.Id);
        mDocTraversalDepth++;
        mVisitorIsInsideComment = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел CommentRangeEnd.
    /// </summary>
    public override VisitorAction VisitCommentRangeEnd(CommentRangeEnd commentRangeEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment range end] ID: " + commentRangeEnd.Id + "\n");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел комментариев.
    /// </summary>
    public override VisitorAction VisitCommentStart(Comment comment)
    {
        IndentAndAppendLine(
            $"[Comment start] For comment range ID {comment.Id}, By {comment.Author} on {comment.DateTime}");
        mDocTraversalDepth++;
        mVisitorIsInsideComment = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе заканчивается посещение узла комментариев.
    /// </summary>
    public override VisitorAction VisitCommentEnd(Comment comment)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment end]");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Добавляем строку в StringBuilder и делаем отступ в зависимости от того, насколько глубоко посетитель находится в дереве документа.
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

    private bool mVisitorIsInsideComment;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Смотрите также

* class [DocumentBase](../../documentbase/)
* class [CommentRangeEnd](../)
* пространство имен [Aspose.Words](../../commentrangeend/)
* сборка [Aspose.Words](../../../)


