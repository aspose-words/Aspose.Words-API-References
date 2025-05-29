---
title: Document.Accept
linktitle: Accept
articleTitle: Accept
second_title: .NET için Aspose.Words
description: Belge Kabul yöntemimizle ziyaretçi yönetiminizi kolaylaştırın. Sorunsuz bir deneyim için güvenliği ve verimliliği artırın.
type: docs
weight: 530
url: /tr/net/aspose.words/document/accept/
---
## Document.Accept method

Bir ziyaretçiyi kabul eder.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| visitor | DocumentVisitor | Düğümleri ziyaret edecek ziyaretçi. |

### Geri dönüş değeri

Tüm düğümler ziyaret edildiyse doğru; eğer ziyaret edilmediyse yanlış[`DocumentVisitor`](../../documentvisitor/) tüm düğümleri ziyaret etmeden önce işlemi durdurdu.

## Notlar

Bu düğüm ve tüm alt düğümleri üzerinde numaralandırma yapar. Her düğüm, ilgili bir yöntemi çağırır[`DocumentVisitor`](../../documentvisitor/).

Daha fazla bilgi için Ziyaretçi tasarım desenine bakın.

Çağrılar[`VisitDocumentStart`](../../documentvisitor/visitdocumentstart/) , sonra arar[`Accept`](../../node/accept/) document ve çağrıların tüm alt düğümleri için[`VisitDocumentEnd`](../../documentvisitor/visitdocumentend/) sonunda.

## Örnekler

Bir belgenin düğüm yapısını yazdırmak için belge ziyaretçisinin nasıl kullanılacağını gösterir.

```csharp
public void DocStructureToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    DocStructurePrinter visitor = new DocStructurePrinter();

    // Bir belge ziyaretçisini kabul etmek için bir bileşik düğüm aldığımızda, ziyaretçi kabul eden düğümü ziyaret eder,
    // ve sonra düğümün tüm çocuklarını derinlemesine bir şekilde dolaşır.
    // Ziyaretçi ziyaret edilen her düğümü okuyabilir ve değiştirebilir.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Bir düğümün alt düğümlerinin ağacını dolaşır.
/// Bu ağacın bir haritasını dize biçiminde oluşturur.
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
    /// Bir Belge düğümünün tüm alt düğümleri ziyaret edildikten sonra çağrılır.
    /// </summary>
    public override VisitorAction VisitDocumentEnd(Document doc)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Document end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Section düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitSectionStart(Section section)
    {
        // Belge içerisindeki bölümümüzün dizinini al.
        NodeCollection docSections = section.Document.GetChildNodes(NodeType.Section, false);
        int sectionIndex = docSections.IndexOf(section);

        IndentAndAppendLine("[Section start] Section index: " + sectionIndex);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Bir Section düğümünün tüm alt düğümleri ziyaret edildikten sonra çağrılır.
    /// </summary>
    public override VisitorAction VisitSectionEnd(Section section)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Section end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Body düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitBodyStart(Body body)
    {
        int paragraphCount = body.Paragraphs.Count;
        IndentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Bir Gövde düğümünün tüm alt düğümleri ziyaret edildikten sonra çağrılır.
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
    /// Bir Paragraf düğümünün tüm alt düğümleri ziyaret edildikten sonra çağrılır.
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
    /// Belgede bir Alt Belge düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)
    {
        IndentAndAppendLine("[SdtRangeStart]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Alt Belge düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)
    {
        IndentAndAppendLine("[SdtRangeEnd]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// StringBuilder'a bir satır ekleyin ve ziyaretçinin belge ağacında ne kadar derine indiğine bağlı olarak girintisini ayarlayın.
    /// </summary>
    /// <param adı="metin"></param>
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

* class [DocumentVisitor](../../documentvisitor/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
