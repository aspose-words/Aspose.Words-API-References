---
title: OfficeMath.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words for .NET
description: OfficeMath Accept yöntem. Ziyaretçi kabul eder C#'da.
type: docs
weight: 60
url: /tr/net/aspose.words.math/officemath/accept/
---
## OfficeMath.Accept method

Ziyaretçi kabul eder.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| visitor | DocumentVisitor | Düğümleri ziyaret edecek ziyaretçi. |

### Geri dönüş değeri

Tüm düğümler ziyaret edilmişse doğrudur; yanlış ise[`DocumentVisitor`](../../../aspose.words/documentvisitor/) tüm düğümleri ziyaret etmeden işlemi durdurdu.

## Notlar

Bu düğümü ve tüm alt öğelerini numaralandırır. Her düğüm kendisine karşılık gelen bir yöntemi çağırır.[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

Daha fazla bilgi için Ziyaretçi tasarım desenine bakın.

Çağrılar[`VisitOfficeMathStart`](../../../aspose.words/documentvisitor/visitofficemathstart/) , ardından arar[`Accept`](../../../aspose.words/node/accept/) Office Math'ın all alt düğümleri ve çağrıları için[`VisitOfficeMathEnd`](../../../aspose.words/documentvisitor/visitofficemathend/) sonunda.

## Örnekler

Bir belgedeki her ofis matematik düğümünün düğüm yapısının nasıl yazdırılacağını gösterir.

```csharp
public void OfficeMathToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

    // Bir belge ziyaretçisini kabul edecek bileşik bir düğüm aldığımızda, ziyaretçi kabul eden düğümü ziyaret eder,
    // ve ardından düğümün tüm alt öğelerini derinlik öncelikli bir şekilde geçer.
    // Ziyaretçi ziyaret edilen her düğümü okuyabilir ve değiştirebilir.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Bir düğümün ikili olmayan alt düğüm ağacını geçer.
/// Karşılaşılan tüm OfficeMath düğümleri ve bunların alt öğelerinden oluşan bir dize biçiminde bir harita oluşturur.
/// </summary>
public class OfficeMathStructurePrinter : DocumentVisitor
{
    public OfficeMathStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideOfficeMath = false;
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
    /// StringBuilder'a bir satır ekleyin ve ziyaretçinin belge ağacında ne kadar derin olduğuna bağlı olarak onu girintileyin.
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

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [OfficeMath](../)
* ad alanı [Aspose.Words.Math](../../../aspose.words.math/)
* toplantı [Aspose.Words](../../../)
