---
title: DocumentVisitor.VisitStructuredDocumentTagEnd
second_title: Aspose.Words for .NET API Referansı
description: DocumentVisitor yöntem. Yapılandırılmış bir belge etiketinin numaralandırılması sona erdiğinde çağrılır.
type: docs
weight: 440
url: /tr/net/aspose.words/documentvisitor/visitstructureddocumenttagend/
---
## DocumentVisitor.VisitStructuredDocumentTagEnd method

Yapılandırılmış bir belge etiketinin numaralandırılması sona erdiğinde çağrılır.

```csharp
public virtual VisitorAction VisitStructuredDocumentTagEnd(StructuredDocumentTag sdt)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| sdt | StructuredDocumentTag | Ziyaret edilen nesne. |

### Geri dönüş değeri

A[`VisitorAction`](../../visitoraction/) numaralandırmaya nasıl devam edileceğini belirten değer.

### Örnekler

Bir belgedeki her yapılandırılmış belge etiketinin düğüm yapısının nasıl yazdırılacağını gösterir.

```csharp
public void StructuredDocumentTagToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    StructuredDocumentTagNodePrinter visitor = new StructuredDocumentTagNodePrinter();

    // Bir belge ziyaretçisini kabul etmek için bir bileşik düğüm aldığımızda, ziyaretçi kabul eden düğümü ziyaret eder,
    // ve ardından tüm düğümün alt öğelerini derinlik öncelikli bir şekilde çaprazlar.
    // Ziyaretçi, ziyaret edilen her düğümü okuyabilir ve değiştirebilir.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Bir düğümün ikili olmayan alt düğümler ağacında çapraz geçiş yapar.
/// Karşılaşılan tüm StructuredDocumentTag düğümlerinin ve bunların alt öğelerinin bir dizesi biçiminde bir harita oluşturur.
/// </summary>
public class StructuredDocumentTagNodePrinter : DocumentVisitor
{
    public StructuredDocumentTagNodePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideStructuredDocumentTag = false;
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
        if (mVisitorIsInsideStructuredDocumentTag) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede StructuredDocumentTag düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitStructuredDocumentTagStart(StructuredDocumentTag sdt)
    {
        IndentAndAppendLine("[StructuredDocumentTag start] Title: " + sdt.Title);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// StructuredDocumentTag düğümünün tüm alt düğümleri ziyaret edildikten sonra çağrılır.
    /// </summary>
    public override VisitorAction VisitStructuredDocumentTagEnd(StructuredDocumentTag sdt)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[StructuredDocumentTag end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// StringBuilder'a bir satır ekleyin ve ziyaretçinin belge ağacında ne kadar derin olduğuna bağlı olarak girinti yapın.
    /// </summary>
    /// <param name="metin"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private readonly bool mVisitorIsInsideStructuredDocumentTag;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Ayrıca bakınız

* enum [VisitorAction](../../visitoraction/)
* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* class [DocumentVisitor](../)
* ad alanı [Aspose.Words](../../documentvisitor/)
* toplantı [Aspose.Words](../../../)


