---
title: Run.GetText
second_title: Aspose.Words for .NET API Referansı
description: Run yöntem. Çalıştırmanın metnini alır.
type: docs
weight: 50
url: /tr/net/aspose.words/run/gettext/
---
## Run.GetText method

Çalıştırmanın metnini alır.

```csharp
public override string GetText()
```

### Geri dönüş değeri

Koşunun metni.

### Örnekler

Bir belgedeki her üstbilgi ve altbilginin düğüm yapısının nasıl yazdırılacağını gösterir.

```csharp
public void HeaderFooterToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    HeaderFooterStructurePrinter visitor = new HeaderFooterStructurePrinter();

    // Bir belge ziyaretçisini kabul etmek için bir bileşik düğüm aldığımızda, ziyaretçi kabul eden düğümü ziyaret eder,
    // ve ardından tüm düğümün alt öğelerini derinlik öncelikli bir şekilde çaprazlar.
    // Ziyaretçi, ziyaret edilen her düğümü okuyabilir ve değiştirebilir.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());

    // Bir belgenin üstbilgi/altbilgilerine bölüm bölüm erişmenin alternatif bir yolu, koleksiyona erişmektir.
    HeaderFooter[] headerFooters = doc.FirstSection.HeadersFooters.ToArray();
    Assert.AreEqual(3, headerFooters.Length);
}

/// <summary>
/// Bir düğümün ikili olmayan alt düğümler ağacında çapraz geçiş yapar.
/// Karşılaşılan tüm HeaderFooter düğümlerinin ve bunların alt öğelerinin bir dizesi biçiminde bir harita oluşturur.
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
    /// Belgede HeaderFooter düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitHeaderFooterStart(HeaderFooter headerFooter)
    {
        IndentAndAppendLine("[HeaderFooter start] HeaderFooterType: " + headerFooter.HeaderFooterType);
        mDocTraversalDepth++;
        mVisitorIsInsideHeaderFooter = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// HeaderFooter düğümünün tüm alt düğümleri ziyaret edildikten sonra çağrılır.
    /// </summary>
    public override VisitorAction VisitHeaderFooterEnd(HeaderFooter headerFooter)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[HeaderFooter end]");
        mVisitorIsInsideHeaderFooter = false;

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

    private bool mVisitorIsInsideHeaderFooter;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Ayrıca bakınız

* class [Run](../)
* ad alanı [Aspose.Words](../../run/)
* toplantı [Aspose.Words](../../../)


