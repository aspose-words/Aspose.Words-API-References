---
title: DocumentVisitor.VisitFieldStart
linktitle: VisitFieldStart
articleTitle: VisitFieldStart
second_title: Aspose.Words for .NET
description: DocumentVisitor VisitFieldStart yöntem. Belgede bir alan başlatıldığında çağrılır C#'da.
type: docs
weight: 200
url: /tr/net/aspose.words/documentvisitor/visitfieldstart/
---
## DocumentVisitor.VisitFieldStart method

Belgede bir alan başlatıldığında çağrılır.

```csharp
public virtual VisitorAction VisitFieldStart(FieldStart fieldStart)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fieldStart | FieldStart | Ziyaret edilen nesne. |

### Geri dönüş değeri

A[`VisitorAction`](../../visitoraction/) numaralandırmaya nasıl devam edileceğini belirten değer.

## Notlar

Word belgesindeki bir alan, alan kodu ve alan değerinden oluşur.

Örneğin sayfa numarasını görüntüleyen bir alan şu şekilde temsil edilebilir:

[FieldStart]PAGE[FieldSeparator]98[FieldEnd]

Alan ayırıcı, alan kodunu belgedeki alan değerinden ayırır. Bazı alanlarının yalnızca alan koduna sahip olduğunu ve alan ayırıcısı ve alan değeri içermediğini unutmayın.

Alanlar iç içe yerleştirilebilir.

## Örnekler

Bir belgedeki her alanın düğüm yapısının nasıl yazdırılacağını gösterir.

```csharp
public void FieldToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    FieldStructurePrinter visitor = new FieldStructurePrinter();

    // Bir belge ziyaretçisini kabul edecek bileşik bir düğüm aldığımızda, ziyaretçi kabul eden düğümü ziyaret eder,
    // ve ardından düğümün tüm alt öğelerini derinlik öncelikli bir şekilde geçer.
    // Ziyaretçi ziyaret edilen her düğümü okuyabilir ve değiştirebilir.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Bir düğümün ikili olmayan alt düğüm ağacını geçer.
/// Karşılaşılan tüm Alan düğümleri ve bunların alt öğelerinden oluşan bir dize biçiminde bir harita oluşturur.
/// </summary>
public class FieldStructurePrinter : DocumentVisitor
{
    public FieldStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideField = false;
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
        if (mVisitorIsInsideField) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir FieldStart düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        IndentAndAppendLine("[Field start] FieldType: " + fieldStart.FieldType);
        mDocTraversalDepth++;
        mVisitorIsInsideField = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede FieldEnd düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Field end]");
        mVisitorIsInsideField = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede FieldSeparator düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        IndentAndAppendLine("[FieldSeparator]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// StringBuilder'a bir satır ekleyin ve ziyaretçinin derinliğine bağlı olarak onu girintileyin
    /// alanın alt düğüm ağacına.
    /// </summary>
    /// <param adı="metin"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++)
        {
            mBuilder.Append("|  ");
        }

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideField;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### Ayrıca bakınız

* enum [VisitorAction](../../visitoraction/)
* class [FieldStart](../../../aspose.words.fields/fieldstart/)
* class [DocumentVisitor](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
