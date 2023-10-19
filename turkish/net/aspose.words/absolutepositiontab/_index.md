---
title: AbsolutePositionTab Class
linktitle: AbsolutePositionTab
articleTitle: AbsolutePositionTab
second_title: Aspose.Words for .NET
description: Aspose.Words.AbsolutePositionTab sınıf. Mutlak konum sekmesi bu WordprocessingML içeriğini görüntülerken geçerli metin satırındaki üzerindeki konumu ilerletmek için kullanılan bir karakterdir C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words/absolutepositiontab/
---
## AbsolutePositionTab class

Mutlak konum sekmesi, bu WordprocessingML içeriğini görüntülerken geçerli metin satırındaki üzerindeki konumu ilerletmek için kullanılan bir karakterdir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Aspose.Words Belge Nesne Modeli (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) dokümantasyon makalesi.

```csharp
public class AbsolutePositionTab : SpecialChar
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [Font](../../aspose.words/inline/font/) { get; } | Bu nesnenin yazı tipi formatlamasına erişim sağlar. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | İadeler`doğru` bu düğüm başka düğümler içeriyorsa. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Değişiklik izleme etkinken bu nesne Microsoft Word'de silinmişse true değerini döndürür. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Microsoft Word'de değişiklik izleme etkinken nesnenin biçimlendirmesi değiştirilmişse doğru değerini döndürür. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Bu nesne Microsoft Word'e değişiklik izleme etkinken eklenmişse doğru değerini döndürür. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | İadeler`doğru` değişiklik izleme etkinken bu nesne Microsoft Word'de taşındıysa (silindiyse). |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | İadeler`doğru` bu nesne Microsoft Word'de değişiklik izleme etkinken taşınmışsa (eklenmişse). |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümden hemen sonra gelen düğümü alır. |
| override [NodeType](../../aspose.words/specialchar/nodetype/) { get; } | İadelerSpecialChar . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün doğrudan ebeveynini alır. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Üst öğeyi alır[`Paragraph`](../paragraph/) bu düğümün. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir değeri döndürür[`Range`](../range/) Bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words/absolutepositiontab/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Ziyaretçi kabul eder. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Düğümün bir kopyasını oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Belirtilenin ilk atayı alır[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Belirtilen nesne türünün ilk atayı alır. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Bu düğümün temsil ettiği özel karakteri alır. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Ön sipariş ağaç geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini üst öğeden kaldırır. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Düğümün içeriğini belirtilen formatta bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

## Örnekler

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

* class [SpecialChar](../specialchar/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
