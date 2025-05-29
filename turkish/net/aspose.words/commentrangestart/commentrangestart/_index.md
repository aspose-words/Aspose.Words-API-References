---
title: CommentRangeStart
linktitle: CommentRangeStart
articleTitle: CommentRangeStart
second_title: .NET için Aspose.Words
description: CommentRangeStart oluşturucusunu keşfedin. Gelişmiş kodlama verimliliği ve akıcı geliştirme için bu sınıfın yeni örneklerini kolayca oluşturun.
type: docs
weight: 10
url: /tr/net/aspose.words/commentrangestart/commentrangestart/
---
## CommentRangeStart constructor

Bu sınıfın yeni bir örneğini başlatır.

```csharp
public CommentRangeStart(DocumentBase doc, int id)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| doc | DocumentBase | Sahip belgesi. |
| id | Int32 | Bu nesnenin bağlı olduğu yorum tanımlayıcısı. |

## Notlar

Ne zaman[`CommentRangeStart`](../) oluşturulduğunda, belirtilen belgeye aittir, ancak henüz belgenin bir parçası değildir ve[`ParentNode`](../../node/parentnode/) dır`hükümsüz`.

Birini eklemek için[`CommentRangeStart`](../) Yorumun eklenmesini istediğiniz paragrafta InsertAfter veya InsertBefore kullanın.

## Örnekler

Bir belge ziyaretçisi kullanarak tüm yorumların içeriklerinin ve yorum aralıklarının nasıl yazdırılacağını gösterir.

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

    // Belgeye metin ekleyin, metni bir yorum aralığında bükün ve ardından yorumunuzu ekleyin.
    Paragraph para = doc.FirstSection.Body.FirstParagraph;
    para.AppendChild(new CommentRangeStart(doc, newComment.Id));
    para.AppendChild(new Run(doc, "Commented text."));
    para.AppendChild(new CommentRangeEnd(doc, newComment.Id));
    para.AppendChild(newComment); 

    // Yoruma iki yanıt ekleyin.
    newComment.AddReply("John Doe", "JD", DateTime.Now, "New reply.");
    newComment.AddReply("John Doe", "JD", DateTime.Now, "Another reply.");

    PrintAllCommentInfo(doc.GetChildNodes(NodeType.Comment, true));
}

/// <summary>
/// Her üst düzey yorum üzerinde yineleme yapar ve yorum aralığını, içeriklerini ve yanıtlarını yazdırır.
/// </summary>
private static void PrintAllCommentInfo(NodeCollection comments)
{
    CommentInfoPrinter commentVisitor = new CommentInfoPrinter();

    // Tüm üst düzey yorumlar üzerinde yineleme yap. Cevap türü yorumların aksine, üst düzey yorumların bir atası yoktur.
    foreach (Comment comment in comments.Where(c => ((Comment)c).Ancestor == null).ToList())
    {
        // Öncelikle yorum aralığının başlangıcını ziyaret edin.
        CommentRangeStart commentRangeStart = (CommentRangeStart)comment.PreviousSibling.PreviousSibling.PreviousSibling;
        commentRangeStart.Accept(commentVisitor);

        // Daha sonra yorumu ve varsa yorumdaki yanıtları ziyaret edin.
        comment.Accept(commentVisitor);
        // Sadece yorumun başlangıcını ziyaret et.
        comment.AcceptStart(commentVisitor);
        // Sadece yorumun sonunu ziyaret edin.
        comment.AcceptEnd(commentVisitor);

        foreach (Comment reply in comment.Replies)
            reply.Accept(commentVisitor);

        // Son olarak yorum aralığının sonuna gidin ve ardından ziyaretçinin metin içeriğini yazdırın.
        CommentRangeEnd commentRangeEnd = (CommentRangeEnd)comment.PreviousSibling;
        commentRangeEnd.Accept(commentVisitor);

        Console.WriteLine(commentVisitor.GetText());
    }
}

/// <summary>
/// Belgede karşılaşılan tüm yorumların ve yorum aralıklarının bilgilerini ve içeriklerini yazdırır.
/// </summary>
public class CommentInfoPrinter : DocumentVisitor
{
    public CommentInfoPrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideComment = false;
    }

    /// <summary>
    /// Ziyaretçinin topladığı belgenin düz metnini alır.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Belgede bir Çalıştırma düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideComment) IndentAndAppendLine("[Run] \"" + run.Text + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir CommentRangeStart düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitCommentRangeStart(CommentRangeStart commentRangeStart)
    {
        IndentAndAppendLine("[Comment range start] ID: " + commentRangeStart.Id);
        mDocTraversalDepth++;
        mVisitorIsInsideComment = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir CommentRangeEnd düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitCommentRangeEnd(CommentRangeEnd commentRangeEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment range end] ID: " + commentRangeEnd.Id + "\n");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Yorum düğümüyle karşılaşıldığında çağrılır.
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
    /// Belgede bir Yorum düğümünün ziyareti sona erdiğinde çağrılır.
    /// </summary>
    public override VisitorAction VisitCommentEnd(Comment comment)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment end]");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// StringBuilder'a bir satır ekleyin ve ziyaretçinin belge ağacında ne kadar derine indiğine bağlı olarak girintisini ayarlayın.
    /// </summary>
    /// <param adı="metin"></param>
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

### Ayrıca bakınız

* class [DocumentBase](../../documentbase/)
* class [CommentRangeStart](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
