---
title: DocumentVisitor.VisitAbsolutePositionTab
linktitle: VisitAbsolutePositionTab
articleTitle: VisitAbsolutePositionTab
second_title: .NET için Aspose.Words
description: AbsolutePositionTab düğümlerini verimli bir şekilde işleyerek belge işlemeyi geliştirmek için tasarlanmış DocumentVisitor VisitAbsolutePositionTab yöntemini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words/documentvisitor/visitabsolutepositiontab/
---
## DocumentVisitor.VisitAbsolutePositionTab method

Bir çağrı yapıldığında çağrılır[`AbsolutePositionTab`](../../absolutepositiontab/) Belgede düğümle karşılaşıldı.

```csharp
public virtual VisitorAction VisitAbsolutePositionTab(AbsolutePositionTab tab)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| tab | AbsolutePositionTab | Ziyaret edilen nesne. |

### Geri dönüş değeri

A[`VisitorAction`](../../visitoraction/) sayımın nasıl devam edeceğini belirten değer.

## Örnekler

Belge ziyaretçisiyle mutlak konum sekme karakterlerinin nasıl işleneceğini gösterir.

```csharp
public void DocumentToTxt()
{
    Document doc = new Document(MyDir + "Absolute position tab.docx");

    // Bu özel belge ziyaretçisini kabul ederek belgemizin metin içeriğini çıkaralım.
    DocTextExtractor myDocTextExtractor = new DocTextExtractor();
    Section fisrtSection = doc.FirstSection;
    fisrtSection.Body.Accept(myDocTextExtractor);
    // Sadece belge gövdesinin başlangıcını ziyaret et.
    fisrtSection.Body.AcceptStart(myDocTextExtractor);
    // Sadece belge gövdesinin sonunu ziyaret et.
    fisrtSection.Body.AcceptEnd(myDocTextExtractor);

    // Dize biçiminde karşılığı olmayan mutlak konum sekmesi açıkça bir sekme karakterine dönüştürüldü.
    Assert.AreEqual("Before AbsolutePositionTab\tAfter AbsolutePositionTab", myDocTextExtractor.GetText());

    // Bir AbsolutePositionTab, bir DocumentVisitor'ı kendi başına da kabul edebilir.
    AbsolutePositionTab absPositionTab = (AbsolutePositionTab)doc.FirstSection.Body.FirstParagraph.GetChild(NodeType.SpecialChar, 0, true);

    myDocTextExtractor = new DocTextExtractor();
    absPositionTab.Accept(myDocTextExtractor);

    Assert.AreEqual("\t", myDocTextExtractor.GetText());
}

/// <summary>
/// Ziyaret edilen belgedeki tüm çalıştırmaların metin içeriklerini toplar. Tüm mutlak sekme karakterlerini sıradan sekmelerle değiştirir.
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
    /// Belgede bir AbsolutePositionTab düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitAbsolutePositionTab(AbsolutePositionTab tab)
    {
        mBuilder.Append("\t");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Mevcut çıktıya metin ekler. Etkin/devre dışı çıkış bayrağını dikkate alır.
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
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
