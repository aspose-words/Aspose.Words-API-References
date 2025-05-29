---
title: DocumentVisitor.VisitCommentEnd
linktitle: VisitCommentEnd
articleTitle: VisitCommentEnd
second_title: .NET için Aspose.Words
description: Projelerinizdeki belge işleme süreçlerini kusursuz hale getirmek için yorum metni numaralandırmasını geliştirmek üzere tasarlanmış DocumentVisitor VisitCommentEnd yöntemini keşfedin.
type: docs
weight: 100
url: /tr/net/aspose.words/documentvisitor/visitcommentend/
---
## DocumentVisitor.VisitCommentEnd method

Bir yorum metninin numaralandırılması sona erdiğinde çağrılır.

```csharp
public virtual VisitorAction VisitCommentEnd(Comment comment)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| comment | Comment | Ziyaret edilen nesne. |

### Geri dönüş değeri

A[`VisitorAction`](../../visitoraction/) sayımın nasıl devam edeceğini belirten değer.

## Örnekler

Bir belgedeki her yorumun ve yorum aralığının düğüm yapısının nasıl yazdırılacağını gösterir.

```csharp
public void CommentsToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    CommentStructurePrinter visitor = new CommentStructurePrinter();

    // Bir belge ziyaretçisini kabul etmek için bir bileşik düğüm aldığımızda, ziyaretçi kabul eden düğümü ziyaret eder,
    // ve sonra düğümün tüm çocuklarını derinlemesine bir şekilde dolaşır.
    // Ziyaretçi ziyaret edilen her düğümü okuyabilir ve değiştirebilir.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Bir düğümün alt düğümlerinin ikili olmayan ağacını dolaşır.
/// Karşılaşılan tüm Yorum/YorumAralığı düğümlerini ve bunların alt öğelerini içeren bir dize biçiminde bir harita oluşturur.
/// </summary>
public class CommentStructurePrinter : DocumentVisitor
{
    public CommentStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideComment = false;
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Belgede bir Çalıştırma düğümüyle karşılaşıldığında çağrılır.
    /// Bir Çalıştırma yalnızca bir Yorum veya YorumAralığı düğümünün çocuğuysa kaydedilir.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideComment) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

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
        IndentAndAppendLine("[Comment range end]");
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
    /// Bir Yorum düğümünün tüm alt düğümleri ziyaret edildikten sonra çağrılır.
    /// </summary>
    public override VisitorAction VisitCommentEnd(Comment comment)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Comment end]");
        mVisitorIsInsideComment = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// StringBuilder'a bir satır ekleyin ve ziyaretçinin derinliğine bağlı olarak girintisini ayarlayın
    /// bir yorum/yorum aralığının alt düğüm ağacına.
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

* enum [VisitorAction](../../visitoraction/)
* class [Comment](../../comment/)
* class [DocumentVisitor](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
