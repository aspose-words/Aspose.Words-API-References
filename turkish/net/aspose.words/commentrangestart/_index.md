---
title: Class CommentRangeStart
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.CommentRangeStart sınıf. Kendisiyle ilişkilendirilmiş bir yorumu olan bir metin bölgesinin başlangıcını belirtir.
type: docs
weight: 250
url: /tr/net/aspose.words/commentrangestart/
---
## CommentRangeStart class

Kendisiyle ilişkilendirilmiş bir yorumu olan bir metin bölgesinin başlangıcını belirtir.

```csharp
public sealed class CommentRangeStart : Node
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [CommentRangeStart](commentrangestart/)(DocumentBase, int) | Bu sınıfın yeni bir örneğini başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [Id](../../aspose.words/commentrangestart/id/) { get; set; } | Bu bölgenin bağlı olduğu yorumun tanımlayıcısını belirtir. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Bu düğüm başka düğümler içerebiliyorsa true değerini döndürür. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümden hemen sonraki düğümü alır. |
| override [NodeType](../../aspose.words/commentrangestart/nodetype/) { get; } | İadeCommentRangeStart . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün hemen üst öğesini alır. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir döndürür **Menzil** belgenin bu düğümde bulunan bölümünü temsil eden nesne. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words/commentrangestart/accept/)(DocumentVisitor) | Bir ziyaretçiyi kabul eder. |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Belirtilenin ilk atasını alır[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Belirtilen nesne türünün ilk üst öğesini alır. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Bu düğümün ve tüm alt öğelerinin metnini alır. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini üst öğeden kaldırır. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

### Notlar

Metnin bir bölgesine sabitlenmiş bir yorum oluşturmak için, bir[`Comment`](../comment/) and sonra oluştur`CommentRangeStart` ve[`CommentRangeEnd`](../commentrangeend/)ve tanımlayıcılarını aynı şekilde ayarlayın[`Id`](../comment/id/) değer.

`CommentRangeStart` satır içi düzey bir düğümdür ve yalnızca alt öğesi olabilir[`Paragraph`](../paragraph/).

### Örnekler

Bir belge ziyaretçisi kullanılarak tüm yorumların içeriğinin ve yorum aralıklarının nasıl yazdırıldığını gösterir.

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

    // Belgeye metin ekleyin, bir yorum aralığında çarpıtın ve ardından yorumunuzu ekleyin.
    Paragraph para = doc.FirstSection.Body.FirstParagraph;
    para.AppendChild(new CommentRangeStart(doc, newComment.Id));
    para.AppendChild(new Run(doc, "Commented text."));
    para.AppendChild(new CommentRangeEnd(doc, newComment.Id));
    para.AppendChild(newComment); 

    // Yoruma iki cevap ekleyin.
    newComment.AddReply("John Doe", "JD", DateTime.Now, "New reply.");
    newComment.AddReply("John Doe", "JD", DateTime.Now, "Another reply.");

    PrintAllCommentInfo(doc.GetChildNodes(NodeType.Comment, true));
}

/// <summary>
/// Her üst düzey yorumu yineler ve yorum aralığını, içeriğini ve yanıtlarını yazdırır.
/// </summary>
private static void PrintAllCommentInfo(NodeCollection comments)
{
    CommentInfoPrinter commentVisitor = new CommentInfoPrinter();

    // Tüm üst düzey yorumları yineleyin. Yanıt türündeki yorumların aksine, üst düzey yorumların atası yoktur.
    foreach (Comment comment in comments.Where(c => ((Comment)c).Ancestor == null))
    {
        // İlk olarak, yorum aralığının başlangıcını ziyaret edin.
        CommentRangeStart commentRangeStart = (CommentRangeStart)comment.PreviousSibling.PreviousSibling.PreviousSibling;
        commentRangeStart.Accept(commentVisitor);

        // Ardından, yorumu ve sahip olabileceği yanıtları ziyaret edin.
        comment.Accept(commentVisitor);

        foreach (Comment reply in comment.Replies)
            reply.Accept(commentVisitor);

        // Son olarak, yorum aralığının sonunu ziyaret edin ve ardından ziyaretçinin metin içeriğini yazdırın.
        CommentRangeEnd commentRangeEnd = (CommentRangeEnd)comment.PreviousSibling;
        commentRangeEnd.Accept(commentVisitor);

        Console.WriteLine(commentVisitor.GetText());
    }
}

/// <summary>
/// Belgede karşılaşılan tüm yorum ve yorum aralıklarının bilgi ve içeriğini yazdırır.
/// </summary>
public class CommentInfoPrinter : DocumentVisitor
{
    public CommentInfoPrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideComment = false;
    }

    /// <summary>
    /// Ziyaretçi tarafından toplanan belgenin düz metnini alır.
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
    /// StringBuilder'a bir satır ekleyin ve ziyaretçinin belge ağacında ne kadar derin olduğuna bağlı olarak girinti yapın.
    /// </summary>
    /// <param name="metin"></param>
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

* class [Node](../node/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


