---
title: HeaderFooter.Accept
linktitle: Accept
articleTitle: Accept
second_title: .NET için Aspose.Words
description: Ziyaretçi katılımını artırmak ve web sitenizdeki etkileşimleri zahmetsizce kolaylaştırmak için HeaderFooter Accept yöntemini keşfedin.
type: docs
weight: 70
url: /tr/net/aspose.words/headerfooter/accept/
---
## HeaderFooter.Accept method

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

Çağrılar[`VisitHeaderFooterStart`](../../documentvisitor/visitheaderfooterstart/) , sonra arar[`Accept`](../../node/accept/) section ve çağrıların tüm alt düğümleri için[`VisitHeaderFooterEnd`](../../documentvisitor/visitheaderfooterend/) sonunda.

## Örnekler

Bir belgedeki her başlık ve alt bilginin düğüm yapısının nasıl yazdırılacağını gösterir.

```csharp
public void HeaderFooterToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    HeaderFooterStructurePrinter visitor = new HeaderFooterStructurePrinter();

    // Bir belge ziyaretçisini kabul etmek için bir bileşik düğüm aldığımızda, ziyaretçi kabul eden düğümü ziyaret eder,
    // ve sonra düğümün tüm çocuklarını derinlemesine bir şekilde dolaşır.
    // Ziyaretçi ziyaret edilen her düğümü okuyabilir ve değiştirebilir.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());

    // Bir belgenin başlık/altbilgilerine bölüm bölüm erişmenin alternatif bir yolu koleksiyona erişmektir.
    HeaderFooter[] headerFooters = doc.FirstSection.HeadersFooters.ToArray();
    Assert.AreEqual(3, headerFooters.Length);
}

/// <summary>
/// Bir düğümün alt düğümlerinin ikili olmayan ağacını dolaşır.
/// Karşılaşılan tüm HeaderFooter düğümlerini ve bunların alt öğelerini içeren bir dize biçiminde bir harita oluşturur.
/// </summary>
public class HeaderFooterStructurePrinter : DocumentVisitor
{
    public HeaderFooterStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideHeaderFooter = false;
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Belgede bir Çalıştırma düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideHeaderFooter) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir HeaderFooter düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitHeaderFooterStart(HeaderFooter headerFooter)
    {
        IndentAndAppendLine("[HeaderFooter start] HeaderFooterType: " + headerFooter.HeaderFooterType);
        mDocTraversalDepth++;
        mVisitorIsInsideHeaderFooter = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Bir HeaderFooter düğümünün tüm alt düğümleri ziyaret edildikten sonra çağrılır.
    /// </summary>
    public override VisitorAction VisitHeaderFooterEnd(HeaderFooter headerFooter)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[HeaderFooter end]");
        mVisitorIsInsideHeaderFooter = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// StringBuilder'a bir satır ekleyin ve ziyaretçinin belge ağacında ne kadar derine indiğine bağlı olarak girintisini ayarlayın.
    /// </summary>
    /// <param adı="metin"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideHeaderFooter;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Ayrıca bakınız

* class [DocumentVisitor](../../documentvisitor/)
* class [HeaderFooter](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
