---
title: Comment
linktitle: Comment
articleTitle: Comment
second_title: .NET için Aspose.Words
description: Yorum oluşturucumuzla zahmetsizce ilgi çekici yorumlar oluşturun. Yeni bir Yorum sınıf örneği başlatın ve kullanıcı etkileşimini sorunsuz bir şekilde geliştirin!
type: docs
weight: 10
url: /tr/net/aspose.words/comment/comment/
---
## Comment(*[DocumentBase](../../documentbase/)*) {#constructor}

Yeni bir örneğini başlatır[`Comment`](../) sınıf.

```csharp
public Comment(DocumentBase doc)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| doc | DocumentBase | Sahip belgesi. |

## Notlar

Ne zaman[`Comment`](../) oluşturulduğunda, belirtilen belgeye aittir, ancak henüz belgenin bir parçası değildir ve[`ParentNode`](../../node/parentnode/) dır`hükümsüz`.

Eklemek için[`Comment`](../) belge kullanımına[`InsertAfter`](../../compositenode/insertafter/) veya[`InsertBefore`](../../compositenode/insertbefore/) Yorumun eklenmesini istediğiniz paragrafın üzerine yazın.

Yorum oluşturduktan sonra yorumunu ayarlamayı unutmayın[`Author`](../author/) , [`Initial`](../initial/) Ve[`DateTime`](../datetime/) özellikler.

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
* class [Comment](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## Comment(*[DocumentBase](../../documentbase/), string, string, DateTime*) {#constructor_1}

Yeni bir örneğini başlatır[`Comment`](../) sınıf.

```csharp
public Comment(DocumentBase doc, string author, string initial, DateTime dateTime)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| doc | DocumentBase | Sahip belgesi. |
| author | String | Yorumun yazar adı. Olamaz`hükümsüz`. |
| initial | String | Yazar yorum için baş harflerini kullanır. Olamaz`hükümsüz`. |
| dateTime | DateTime | Yorumun tarihi ve saati. |

## Örnekler

Bir paragrafa yorum eklemenin nasıl yapılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "JD", DateTime.Today);
builder.CurrentParagraph.AppendChild(comment);
builder.MoveTo(comment.AppendChild(new Paragraph(doc)));
builder.Write("Comment text.");

Assert.AreEqual(DateTime.Today, comment.DateTime);

 // Microsoft Word'de, bu yorumu belge gövdesinde sağ tıklayarak düzenleyebilir veya yanıtlayabiliriz.
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

### Ayrıca bakınız

* class [DocumentBase](../../documentbase/)
* class [Comment](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
