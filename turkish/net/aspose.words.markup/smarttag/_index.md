---
title: SmartTag Class
linktitle: SmartTag
articleTitle: SmartTag
second_title: .NET için Aspose.Words
description: Resimler ve alanlar gibi satır içi öğelerin etrafındaki akıllı etiketleri belirleyerek belge düzenlemeyi geliştiren Aspose.Words.Markup.SmartTag sınıfını keşfedin.
type: docs
weight: 4740
url: /tr/net/aspose.words.markup/smarttag/
---
## SmartTag class

Bu öğe, bir paragraf içindeki bir veya daha fazla satır içi yapının (çalıştırmalar, resimler, alanlar, vb.) etrafında akıllı bir etiketin varlığını belirtir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yapılandırılmış Belge Etiketleri veya İçerik Denetimi](https://docs.aspose.com/words/net/working-with-content-control-sdt/) belgeleme makalesi.

```csharp
public class SmartTag : CompositeNode
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [SmartTag](smarttag/)(*[DocumentBase](../../aspose.words/documentbase/)*) | Yeni bir örneğini başlatır`SmartTag` sınıf. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün hemen alt düğümlerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [Element](../../aspose.words.markup/smarttag/element/) { get; set; } | Belge içindeki akıllı etiketin adını belirtir. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk çocuğunu alır. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Geri Döndürür`doğru` eğer bu düğümün herhangi bir alt düğümü varsa. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Geri Döndürür`doğru` çünkü bu düğümün alt düğümleri olabilir. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son çocuğunu alır. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümü hemen takip eden düğümü alır. |
| override [NodeType](../../aspose.words.markup/smarttag/nodetype/) { get; } | Geri DöndürürSmartTag . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün en yakın üst düğümünü alır. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Properties](../../aspose.words.markup/smarttag/properties/) { get; } | Akıllı etiket özelliklerinin bir koleksiyonu. |
| [Range](../../aspose.words/node/range/) { get; } | Bir[`Range`](../../aspose.words/range/)bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |
| [Uri](../../aspose.words.markup/smarttag/uri/) { get; set; } | Akıllı etiketin ad alanı URI'sini belirtir. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words.markup/smarttag/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Bir ziyaretçiyi kabul eder. |
| override [AcceptEnd](../../aspose.words.markup/smarttag/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Akıllı Etiketin sonunu ziyaret eden bir ziyaretçiyi kabul eder. |
| override [AcceptStart](../../aspose.words.markup/smarttag/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Akıllı Etiketin başlangıcını ziyaret eden bir ziyaretçiyi kabul eder. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Belirtilen düğümü bu düğüm için alt düğümler listesinin sonuna ekler. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Düğümleri gezmek ve okumak için kullanılabilen gezgini oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Belirtilenin ilk atasını alır[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Belirtilen nesne türünün ilk atasını alır. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Belirtilen türle eşleşen N'inci alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bu düğümün alt düğümleri üzerindeki her stil yinelemesi için destek sağlar. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Bu düğümün ve tüm alt düğümlerinin metnini alır. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Alt düğüm dizisindeki belirtilen alt düğümün dizinini döndürür. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | Belirtilen düğümü belirtilen referans düğümünden hemen sonra ekler. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | Belirtilen düğümü belirtilen referans düğümünden hemen önce ekler. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Ön sipariş ağacı geçiş algoritmasına göre bir sonraki düğümü alır. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Belirtilen düğümü bu düğüm için alt düğümler listesinin başına ekler. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini ana öğeden kaldırır. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Belirtilen alt düğümü kaldırır. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tümünü kaldırır`SmartTag` geçerli düğümün alt düğümleri. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | XPath ifadesiyle eşleşen düğümlerin bir listesini seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | İlkini seçer[`Node`](../../aspose.words/node/) XPath ifadesiyle eşleşen. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

## Notlar

Akıllı etiketler bir tür özel XML işaretlemesidir. Akıllı etiketler, bir belge içindeki bir çalıştırma veya çalıştırma kümesi için temel bir ad alanı/name sağlama yeteneği aracılığıyla, müşteri tarafından tanımlanan semantiğin belgeye gömülmesi için bir olanak sağlar.

`SmartTag` bir çocuğun çocuğu olabilir[`Paragraph`](../../aspose.words/paragraph/) or başka`SmartTag` düğüm.

Akıllı etiketin içinde bulunabilecek alt düğümlerin tam listesi 'den oluşur[`BookmarkStart`](../../aspose.words/bookmarkstart/) ,[`BookmarkEnd`](../../aspose.words/bookmarkend/) , [`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../aspose.words.fields/fieldend/) ,[`FormField`](../../aspose.words.fields/formfield/) , [`Comment`](../../aspose.words/comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) , [`Run`](../../aspose.words/run/) ,[`SpecialChar`](../../aspose.words/specialchar/) , [`Shape`](../../aspose.words.drawing/shape/) ,[`GroupShape`](../../aspose.words.drawing/groupshape/) , [`CommentRangeStart`](../../aspose.words/commentrangestart/) , [`CommentRangeEnd`](../../aspose.words/commentrangeend/) , `SmartTag`.

## Örnekler

Akıllı etiketlerin nasıl oluşturulacağını gösterir.

```csharp
public void Create()
{
    Document doc = new Document();

    // Microsoft Word'de bir belgede görünen akıllı etiket, metnin bir kısmını bir tür veri olarak tanır,
    // isim, tarih veya adres gibi bir bilgiyi alıp mor noktalı alt çizgi gösteren bir köprü metnine dönüştürür.
    SmartTag smartTag = new SmartTag(doc);

    // Akıllı etiketler, tanınan metinlerini bütünüyle içeren bileşik düğümlerdir.
    // Bu akıllı etikete içerikleri manuel olarak ekleyin.
    smartTag.AppendChild(new Run(doc, "May 29, 2019"));

    // Microsoft Word yukarıdaki içeriği bir tarih olarak tanıyabilir.
    // Akıllı etiketler, içerdikleri veri türünü yansıtmak için "Element" özelliğini kullanır.
    smartTag.Element = "date";

    // Bazı akıllı etiket türleri içeriklerini daha sonra özel XML özelliklerine işler.
    smartTag.Properties.Add(new CustomXmlProperty("Day", string.Empty, "29"));
    smartTag.Properties.Add(new CustomXmlProperty("Month", string.Empty, "5"));
    smartTag.Properties.Add(new CustomXmlProperty("Year", string.Empty, "2019"));

    // Akıllı etiketin URI'sini varsayılan değere ayarlayın.
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a date. "));

    // Bir hisse senedi için başka bir akıllı etiket oluşturun.
    smartTag = new SmartTag(doc);
    smartTag.Element = "stockticker";
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    smartTag.AppendChild(new Run(doc, "MSFT"));

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a stock ticker."));

    // Belge ziyaretçisini kullanarak belgemizdeki tüm akıllı etiketleri yazdır.
    doc.Accept(new SmartTagPrinter());

    // Microsoft Word'ün eski sürümleri akıllı etiketleri destekler.
    doc.Save(ArtifactsDir + "SmartTag.Create.doc");

    // Bir belgeden tüm akıllı etiketleri kaldırmak için "RemoveSmartTags" yöntemini kullanın.
    Assert.AreEqual(2, doc.GetChildNodes(NodeType.SmartTag, true).Count);

    doc.RemoveSmartTags();

    Assert.AreEqual(0, doc.GetChildNodes(NodeType.SmartTag, true).Count);
}

/// <summary>
/// Ziyaret edilen akıllı etiketleri ve içeriklerini yazdırır.
/// </summary>
private class SmartTagPrinter : DocumentVisitor
{
    /// <summary>
    /// Belgede bir SmartTag düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitSmartTagStart(SmartTag smartTag)
    {
        Console.WriteLine($"Smart tag type: {smartTag.Element}");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Bir SmartTag düğümünün ziyareti sona erdiğinde çağrılır.
    /// </summary>
    public override VisitorAction VisitSmartTagEnd(SmartTag smartTag)
    {
        Console.WriteLine($"\tContents: \"{smartTag.ToString(SaveFormat.Text)}\"");

        if (smartTag.Properties.Count == 0)
        {
            Console.WriteLine("\tContains no properties");
        }
        else
        {
            Console.Write("\tProperties: ");
            string[] properties = new string[smartTag.Properties.Count];
            int index = 0;

            foreach (CustomXmlProperty cxp in smartTag.Properties)
                properties[index++] = $"\"{cxp.Name}\" = \"{cxp.Value}\"";

            Console.WriteLine(string.Join(", ", properties));
        }

        return VisitorAction.Continue;
    }
}
```

### Ayrıca bakınız

* class [CompositeNode](../../aspose.words/compositenode/)
* ad alanı [Aspose.Words.Markup](../../aspose.words.markup/)
* toplantı [Aspose.Words](../../)
