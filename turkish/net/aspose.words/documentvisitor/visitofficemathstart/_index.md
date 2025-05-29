---
title: DocumentVisitor.VisitOfficeMathStart
linktitle: VisitOfficeMathStart
articleTitle: VisitOfficeMathStart
second_title: .NET için Aspose.Words
description: Office Math nesne numaralandırmasını başlatmak için gerekli olan DocumentVisitor VisitOfficeMathStart yöntemini keşfedin. Kodlama verimliliğinizi bugün artırın!
type: docs
weight: 310
url: /tr/net/aspose.words/documentvisitor/visitofficemathstart/
---
## DocumentVisitor.VisitOfficeMathStart method

Bir Office Math nesnesinin numaralandırılması başladığında çağrılır.

```csharp
public virtual VisitorAction VisitOfficeMathStart(OfficeMath officeMath)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| officeMath | OfficeMath | Ziyaret edilen nesne. |

### Geri dönüş değeri

A[`VisitorAction`](../../visitoraction/) sayımın nasıl devam edeceğini belirten değer.

## Örnekler

Bir belgedeki her ofis matematik düğümünün düğüm yapısının nasıl yazdırılacağını gösterir.

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

    // Bir belge ziyaretçisini kabul etmek için bir bileşik düğüm aldığımızda, ziyaretçi kabul eden düğümü ziyaret eder,
    // ve sonra düğümün tüm çocuklarını derinlemesine bir şekilde dolaşır.
    // Ziyaretçi ziyaret edilen her düğümü okuyabilir ve değiştirebilir.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Bir düğümün alt düğümlerinin ikili olmayan ağacını dolaşır.
/// Karşılaşılan tüm OfficeMath düğümlerinin ve bunların alt öğelerinin bir dize biçiminde bir haritasını oluşturur.
/// </summary>
public class OfficeMathStructurePrinter : DocumentVisitor
{
    public OfficeMathStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideOfficeMath = false;
    }

    /// <summary>
    /// Ziyaretçinin topladığı belgenin düz metnini alır.
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
        if (mVisitorIsInsideOfficeMath) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir OfficeMath düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitOfficeMathStart(OfficeMath officeMath)
    {
        IndentAndAppendLine("[OfficeMath start] Math object type: " + officeMath.MathObjectType);
        mDocTraversalDepth++;
        mVisitorIsInsideOfficeMath = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Bir OfficeMath düğümünün tüm alt düğümleri ziyaret edildikten sonra çağrılır.
    /// </summary>
    public override VisitorAction VisitOfficeMathEnd(OfficeMath officeMath)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[OfficeMath end]");
        mVisitorIsInsideOfficeMath = false;

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

    private bool mVisitorIsInsideOfficeMath;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Ayrıca bakınız

* enum [VisitorAction](../../visitoraction/)
* class [OfficeMath](../../../aspose.words.math/officemath/)
* class [DocumentVisitor](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
