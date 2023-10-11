---
title: DocumentVisitor.VisitAbsolutePositionTab
second_title: Aspose.Words for .NET API Referansı
description: DocumentVisitor yöntem. Şu durumlarda çağrılırAbsolutePositionTab Belgede düğümle karşılaşıldı.
type: docs
weight: 10
url: /tr/net/aspose.words/documentvisitor/visitabsolutepositiontab/
---
## DocumentVisitor.VisitAbsolutePositionTab method

Şu durumlarda çağrılır:[`AbsolutePositionTab`](../../absolutepositiontab/) Belgede düğümle karşılaşıldı.

```csharp
public virtual VisitorAction VisitAbsolutePositionTab(AbsolutePositionTab tab)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| tab | AbsolutePositionTab | Ziyaret edilen nesne. |

### Geri dönüş değeri

A[`VisitorAction`](../../visitoraction/) numaralandırmaya nasıl devam edileceğini belirten değer.

### Örnekler

Mutlak konum sekmesi karakterlerinin bir belge ziyaretçisiyle nasıl işleneceğini gösterir.

```csharp
public void DocumentToTxt()
{
    Document doc = new Document(MyDir + "Absolute position tab.docx");

    // Bu özel belge ziyaretçisini kabul ederek belgemizin metin içeriğini çıkartın.
    DocTextExtractor myDocTextExtractor = new DocTextExtractor();
    doc.FirstSection.Body.Accept(myDocTextExtractor);

    // String biçiminde eşdeğeri olmayan mutlak konum sekmesi açıkça bir sekme karakterine dönüştürüldü.
    Assert.AreEqual("Before AbsolutePositionTab\tAfter AbsolutePositionTab", myDocTextExtractor.GetText());

    // AbsolutePositionTab tek başına bir DocumentVisitor'ı da kabul edebilir.
    AbsolutePositionTab absPositionTab = (AbsolutePositionTab)doc.FirstSection.Body.FirstParagraph.GetChild(NodeType.SpecialChar, 0, true);

    myDocTextExtractor = new DocTextExtractor();
    absPositionTab.Accept(myDocTextExtractor);

    Assert.AreEqual("\t", myDocTextExtractor.GetText());
}

/// <summary>
/// Ziyaret edilen belgedeki tüm çalıştırmaların metin içeriğini toplar. Tüm mutlak sekme karakterlerini sıradan sekmelerle değiştirir.
/// </summary>
public class DocTextExtractor : DocumentVisitor
{
    public DocTextExtractor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Belgede bir Çalıştırma düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        AppendText(run.Text);
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede AbsolutePositionTab düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitAbsolutePositionTab(AbsolutePositionTab tab)
    {
        mBuilder.Append("\t");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Geçerli çıktıya metin ekler. Etkin/devre dışı çıkış bayrağını dikkate alır.
    /// </summary>
    private void AppendText(string text)
    {
        mBuilder.Append(text);
    }

    /// <summary>
    /// Ziyaretçinin biriktirdiği belgenin düz metni.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    private readonly StringBuilder mBuilder;
}
```

### Ayrıca bakınız

* enum [VisitorAction](../../visitoraction/)
* class [AbsolutePositionTab](../../absolutepositiontab/)
* class [DocumentVisitor](../)
* ad alanı [Aspose.Words](../../documentvisitor/)
* toplantı [Aspose.Words](../../../)


