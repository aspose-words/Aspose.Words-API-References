---
title: DocumentVisitor.VisitSmartTagEnd
linktitle: VisitSmartTagEnd
articleTitle: VisitSmartTagEnd
second_title: Aspose.Words for .NET
description: DocumentVisitor VisitSmartTagEnd yöntem. Akıllı etiketin numaralandırılması sona erdiğinde çağrılır C#'da.
type: docs
weight: 410
url: /tr/net/aspose.words/documentvisitor/visitsmarttagend/
---
## DocumentVisitor.VisitSmartTagEnd method

Akıllı etiketin numaralandırılması sona erdiğinde çağrılır.

```csharp
public virtual VisitorAction VisitSmartTagEnd(SmartTag smartTag)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| smartTag | SmartTag | Ziyaret edilen nesne. |

### Geri dönüş değeri

A[`VisitorAction`](../../visitoraction/) numaralandırmaya nasıl devam edileceğini belirten değer.

## Örnekler

Bir belgedeki her akıllı etiketin düğüm yapısının nasıl yazdırılacağını gösterir.

```csharp
public void SmartTagToText()
{
    Document doc = new Document(MyDir + "Smart tags.doc");
    SmartTagStructurePrinter visitor = new SmartTagStructurePrinter();

    // Bir belge ziyaretçisini kabul edecek bileşik bir düğüm aldığımızda, ziyaretçi kabul eden düğümü ziyaret eder,
    // ve ardından düğümün tüm alt öğelerini derinlik öncelikli bir şekilde geçer.
    // Ziyaretçi ziyaret edilen her düğümü okuyabilir ve değiştirebilir.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Bir düğümün ikili olmayan alt düğüm ağacını geçer.
/// Karşılaşılan tüm SmartTag düğümleri ve bunların alt öğelerinden oluşan bir dizi biçiminde bir harita oluşturur.
/// </summary>
public class SmartTagStructurePrinter : DocumentVisitor
{
    public SmartTagStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideSmartTag = false;
    }

    /// <summary>
    /// Ziyaretçinin biriktirdiği belgenin düz metnini alır.
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
        if (mVisitorIsInsideSmartTag) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir SmartTag düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitSmartTagStart(SmartTag smartTag)
    {
        IndentAndAppendLine("[SmartTag start] Name: " + smartTag.Element);
        mDocTraversalDepth++;
        mVisitorIsInsideSmartTag = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Bir SmartTag düğümünün tüm alt düğümleri ziyaret edildikten sonra çağrılır.
    /// </summary>
    public override VisitorAction VisitSmartTagEnd(SmartTag smartTag)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[SmartTag end]");
        mVisitorIsInsideSmartTag = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// StringBuilder'a bir satır ekleyin ve ziyaretçinin belge ağacında ne kadar derin olduğuna bağlı olarak onu girintileyin.
    /// </summary>
    /// <param adı="metin"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideSmartTag;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Ayrıca bakınız

* enum [VisitorAction](../../visitoraction/)
* class [SmartTag](../../../aspose.words.markup/smarttag/)
* class [DocumentVisitor](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
