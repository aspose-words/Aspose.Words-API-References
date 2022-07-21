---
title: VisitSubDocument
second_title: Aspose.Words for .NET API Referansı
description: Bir alt Belge ile karşılaşıldığında çağrılır.
type: docs
weight: 480
url: /tr/net/aspose.words/documentvisitor/visitsubdocument/
---
## DocumentVisitor.VisitSubDocument method

Bir alt Belge ile karşılaşıldığında çağrılır.

```csharp
public virtual VisitorAction VisitSubDocument(SubDocument subDocument)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| subDocument | SubDocument | Ziyaret edilen nesne. |

### Geri dönüş değeri

A[`VisitorAction`](../../visitoraction) numaralandırmaya nasıl devam edileceğini belirten değer.

### Örnekler

Bir belgenin düğüm yapısını yazdırmak için belge ziyaretçisinin nasıl kullanılacağını gösterir.

```csharp
public void DocStructureToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    DocStructurePrinter visitor = new DocStructurePrinter();

    // Bir belge ziyaretçisini kabul etmek için bir bileşik düğüm aldığımızda, ziyaretçi kabul eden düğümü ziyaret eder,
    // ve ardından tüm düğümün alt öğelerini derinlik öncelikli bir şekilde çaprazlar.
    // Ziyaretçi, ziyaret edilen her düğümü okuyabilir ve değiştirebilir.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Bir düğümün alt düğümler ağacında çapraz geçiş yapar.
/// Bu ağacın bir dizge biçiminde bir haritasını oluşturur.
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
    /// Bir Belge düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitDocumentStart(Document doc)
    {
        int childNodeCount = doc.GetChildNodes(NodeType.Any, true).Count;

        IndentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
        mDocTraversalDepth++;

        // Ziyaretçinin diğer düğümleri ziyaret etmeye devam etmesine izin ver.
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belge düğümünün tüm alt düğümleri ziyaret edildikten sonra çağrılır.
    /// </summary>
    public override VisitorAction VisitDocumentEnd(Document doc)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Document end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Bölüm düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitSectionStart(Section section)
    {
        // Belge içindeki bölümümüzün indeksini alın.
        NodeCollection docSections = section.Document.GetChildNodes(NodeType.Section, false);
        int sectionIndex = docSections.IndexOf(section);

        IndentAndAppendLine("[Section start] Section index: " + sectionIndex);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Bir Bölüm düğümünün tüm alt düğümleri ziyaret edildikten sonra çağrılır.
    /// </summary>
    public override VisitorAction VisitSectionEnd(Section section)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Section end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Gövde düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitBodyStart(Body body)
    {
        int paragraphCount = body.Paragraphs.Count;
        IndentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Bir Body düğümünün tüm alt düğümleri ziyaret edildikten sonra çağrılır.
    /// </summary>
    public override VisitorAction VisitBodyEnd(Body body)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Body end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Paragraf düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        IndentAndAppendLine("[Paragraph start]");
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Paragraf düğümünün tüm alt düğümleri ziyaret edildikten sonra çağrılır.
    /// </summary>
    public override VisitorAction VisitParagraphEnd(Paragraph paragraph)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Paragraph end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Çalıştırma düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Alt Belge düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitSubDocument(SubDocument subDocument)
    {
        IndentAndAppendLine("[SubDocument]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// StringBuilder'a bir satır ekleyin ve ziyaretçinin belge ağacında ne kadar derin olduğuna bağlı olarak girinti yapın.
    /// </summary>
    /// <param name="metin"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mAcceptingNodeChildTree.Append("|  ");

        mAcceptingNodeChildTree.AppendLine(text);
    }

    private int mDocTraversalDepth;
    private readonly StringBuilder mAcceptingNodeChildTree;
}
```

### Ayrıca bakınız

* enum [VisitorAction](../../visitoraction)
* class [SubDocument](../../subdocument)
* class [DocumentVisitor](../../documentvisitor)
* ad alanı [Aspose.Words](../../documentvisitor)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
