---
title: Comment
second_title: Справочник по API Aspose.Words для .NET
description: Инициализирует новый экземпляр Комментарий класс.
type: docs
weight: 10
url: /ru/net/aspose.words/comment/comment/
---
## Comment(DocumentBase) {#constructor}

Инициализирует новый экземпляр **Комментарий** класс.

```csharp
public Comment(DocumentBase doc)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | DocumentBase | Документ владельца. |

### Примечания

Когда **Комментарий** создан, он принадлежит указанному документу, но не является частью документа и **Родительский узел** нулевой.

Чтобы добавить **Комментарий** к документу используйте InsertAfter или InsertBefore в абзаце, куда вы хотите вставить комментарий.

После создания комментария не забудьте установить его[`Author`](../author) , [`Initial`](../initial) а также[`DateTime`](../datetime) характеристики.

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

* class [DocumentBase](../../documentbase)
* class [Comment](../../comment)
* пространство имен [Aspose.Words](../../comment)
* сборка [Aspose.Words](../../../)

---

## Comment(DocumentBase, string, string, DateTime) {#constructor_1}

Инициализирует новый экземпляр **Комментарий** класс.

```csharp
public Comment(DocumentBase doc, string author, string initial, DateTime dateTime)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | DocumentBase | Документ владельца. |
| author | String | Имя автора комментария. Не может быть нулевым. |
| initial | String | Инициалы автора комментария. Не может быть нулевым. |
| dateTime | DateTime | Дата и время комментария. |

### Примеры

Показывает, как добавить комментарий к абзацу.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "JD", DateTime.Today);
builder.CurrentParagraph.AppendChild(comment);
builder.MoveTo(comment.AppendChild(new Paragraph(doc)));
builder.Write("Comment text.");

Assert.AreEqual(DateTime.Today, comment.DateTime);

// В Microsoft Word мы можем щелкнуть правой кнопкой мыши этот комментарий в теле документа, чтобы отредактировать его или ответить на него. 
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

### Смотрите также

* class [DocumentBase](../../documentbase)
* class [Comment](../../comment)
* пространство имен [Aspose.Words](../../comment)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
