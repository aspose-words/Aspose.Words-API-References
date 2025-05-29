---
title: BuildingBlock Class
linktitle: BuildingBlock
articleTitle: BuildingBlock
second_title: .NET için Aspose.Words
description: Gelişmiş belge verimliliği için Otomatik Metin ve Otomatik Düzeltme gibi sözlük girişleri oluşturmak ve yönetmek amacıyla Aspose.Words.BuildingBlocks.BuildingBlock sınıfını keşfedin.
type: docs
weight: 320
url: /tr/net/aspose.words.buildingblocks/buildingblock/
---
## BuildingBlock class

Bir Yapı Bloğu, Otomatik Metin veya Otomatik Düzeltme girişi gibi bir sözlük belge girişini temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Aspose.Words Belge Nesne Modeli (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) belgeleme makalesi.

```csharp
public class BuildingBlock : CompositeNode
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [BuildingBlock](buildingblock/)(*[GlossaryDocument](../glossarydocument/)*) | Bu sınıfın yeni bir örneğini başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Behavior](../../aspose.words.buildingblocks/buildingblock/behavior/) { get; set; } | Yapı bloğunun içeriği ana belgeye eklendiğinde uygulanacak davranışı belirtir. |
| [Category](../../aspose.words.buildingblocks/buildingblock/category/) { get; set; } | Yapı bloğu için ikinci düzey kategorizasyonu belirtir. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün hemen alt düğümlerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| [Description](../../aspose.words.buildingblocks/buildingblock/description/) { get; set; } | Bu yapı bloğuyla ilişkili açıklamayı alır veya ayarlar. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk çocuğunu alır. |
| [FirstSection](../../aspose.words.buildingblocks/buildingblock/firstsection/) { get; } | Yapı bloğundaki ilk bölümü alır. |
| [Gallery](../../aspose.words.buildingblocks/buildingblock/gallery/) { get; set; } | sınıflandırması veya kullanıcı arayüzü sıralaması amaçları doğrultusunda yapı taşı için birinci düzey kategorizasyonu belirtir. |
| [Guid](../../aspose.words.buildingblocks/buildingblock/guid/) { get; set; } | Bu yapı taşını benzersiz bir şekilde tanımlayan bir tanımlayıcı (128 bitlik bir GUID) alır veya ayarlar. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Geri Döndürür`doğru` eğer bu düğümün herhangi bir alt düğümü varsa. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Geri Döndürür`doğru` çünkü bu düğümün alt düğümleri olabilir. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son çocuğunu alır. |
| [LastSection](../../aspose.words.buildingblocks/buildingblock/lastsection/) { get; } | Yapı bloğundaki son bölümü alır. |
| [Name](../../aspose.words.buildingblocks/buildingblock/name/) { get; set; } | Bu yapı bloğunun adını alır veya ayarlar. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümü hemen takip eden düğümü alır. |
| override [NodeType](../../aspose.words.buildingblocks/buildingblock/nodetype/) { get; } | şunu döndürür:BuildingBlock değer. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün en yakın üst düğümünü alır. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir[`Range`](../../aspose.words/range/)bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |
| [Sections](../../aspose.words.buildingblocks/buildingblock/sections/) { get; } | Yapı bloğundaki tüm bölümleri temsil eden bir koleksiyon döndürür. |
| [Type](../../aspose.words.buildingblocks/buildingblock/type/) { get; set; } | Yapı bloğu türünü belirtir. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words.buildingblocks/buildingblock/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Bir ziyaretçiyi kabul eder. |
| override [AcceptEnd](../../aspose.words.buildingblocks/buildingblock/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | BuildingBlock'un sonunu ziyaret eden bir ziyaretçiyi kabul eder. |
| override [AcceptStart](../../aspose.words.buildingblocks/buildingblock/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | BuildingBlock'un başlangıcını ziyaret eden bir ziyaretçiyi kabul eder. |
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
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tümünü kaldırır[`SmartTag`](../../aspose.words.markup/smarttag/) geçerli düğümün alt düğümleri. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | XPath ifadesiyle eşleşen düğümlerin bir listesini seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | İlkini seçer[`Node`](../../aspose.words/node/) XPath ifadesiyle eşleşen. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

## Notlar

`BuildingBlock` sadece içerebilir[`Section`](../../aspose.words/section/) düğümler.

`BuildingBlock` sadece bir çocuk olabilir[`GlossaryDocument`](../glossarydocument/).

Yeni yapı taşları oluşturabilir ve bunları bir sözlük belgesine ekleyebilirsiniz. Mevcut yapı taşlarını değiştirebilir veya silebilirsiniz. Yapı taşlarını belgeler arasında kopyalayabilir veya taşıyabilirsiniz. Bir yapı taşının içeriğini bir belgeye ekleyebilirsiniz.

Karşılık gelir**docPart** ,**docPartPr** Ve**docPartGövde**OOXML'deki öğeler.

## Örnekler

Bir belgeye özel yapı taşının nasıl ekleneceğini gösterir.

```csharp
public void CreateAndInsert()
{
    // Bir belgenin sözlük belgesi yapı taşlarını depolar.
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();
    doc.GlossaryDocument = glossaryDoc;

    // Bir yapı taşı oluşturun, ona bir isim verin ve ardından sözlük belgesine ekleyin.
    BuildingBlock block = new BuildingBlock(glossaryDoc)
    {
        Name = "Custom Block"
    };

    glossaryDoc.AppendChild(block);

    // Tüm yeni yapı taşı GUID'leri varsayılan olarak aynı sıfır değerine sahiptir ve bunlara yeni ve benzersiz bir değer verebiliriz.
    Assert.AreEqual("00000000-0000-0000-0000-000000000000", block.Guid.ToString());

    block.Guid = Guid.NewGuid();

    // Aşağıdaki özellikler yapı taşlarını kategorilere ayırır
    // Microsoft Word'de "Ekle" -> "Hızlı Parçalar" -> "Yapı Blokları Düzenleyicisi" yoluyla ulaşabileceğimiz menüde.
    Assert.AreEqual("(Empty Category)", block.Category);
    Assert.AreEqual(BuildingBlockType.None, block.Type);
    Assert.AreEqual(BuildingBlockGallery.All, block.Gallery);
    Assert.AreEqual(BuildingBlockBehavior.Content, block.Behavior);

    // Bu yapı taşını belgemize eklemeden önce, ona bazı içerikler vermemiz gerekecek,
    // bunu bir belge ziyaretçisi kullanarak yapacağız. Bu ziyaretçi ayrıca bir kategori, galeri ve davranış belirleyecek.
    BuildingBlockVisitor visitor = new BuildingBlockVisitor(glossaryDoc);
    // BuildingBlock'un başlangıcını/sonunu ziyaret edin.
    block.Accept(visitor);

    // Az önce oluşturduğumuz bloğa sözlük belgesinden erişebiliriz.
    BuildingBlock customBlock = glossaryDoc.GetBuildingBlock(BuildingBlockGallery.QuickParts,
        "My custom building blocks", "Custom Block");

    // Blok, metnin yer aldığı bölümdür.
    Assert.AreEqual($"Text inside {customBlock.Name}\f", customBlock.FirstSection.Body.FirstParagraph.GetText());
    Assert.AreEqual(customBlock.FirstSection, customBlock.LastSection);
    // Şimdi bunu yeni bir bölüm olarak belgeye ekleyebiliriz.
    doc.AppendChild(doc.ImportNode(customBlock.FirstSection, true));

    // Bunu Microsoft Word'ün Building Blocks Organizer'ında da bulabilir ve elle yerleştirebiliriz.
    doc.Save(ArtifactsDir + "BuildingBlocks.CreateAndInsert.dotx");
}

/// <summary>
/// Ziyaret edilen bir yapı bloğunun belgeye hızlı bir parça olarak eklenmesini ayarlar ve içeriğine metin ekler.
/// </summary>
public class BuildingBlockVisitor : DocumentVisitor
{
    public BuildingBlockVisitor(GlossaryDocument ownerGlossaryDoc)
    {
        mBuilder = new StringBuilder();
        mGlossaryDoc = ownerGlossaryDoc;
    }

    public override VisitorAction VisitBuildingBlockStart(BuildingBlock block)
    {
        // Yapı bloğunu hızlı bir parça olarak yapılandırın ve Yapı Blokları Düzenleyicisi tarafından kullanılan özellikleri ekleyin.
        block.Behavior = BuildingBlockBehavior.Paragraph;
        block.Category = "My custom building blocks";
        block.Description =
            "Using this block in the Quick Parts section of word will place its contents at the cursor.";
        block.Gallery = BuildingBlockGallery.QuickParts;

        // Metin içeren bir bölüm ekleyin.
        // Bloğun belgeye eklenmesi, bu bölümü alt düğümleriyle birlikte konuma ekleyecektir.
        Section section = new Section(mGlossaryDoc);
        block.AppendChild(section);
        block.FirstSection.EnsureMinimum();

        Run run = new Run(mGlossaryDoc, "Text inside " + block.Name);
        block.FirstSection.Body.FirstParagraph.AppendChild(run);

        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBuildingBlockEnd(BuildingBlock block)
    {
        mBuilder.Append("Visited " + block.Name + "\r\n");
        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
    private readonly GlossaryDocument mGlossaryDoc;
}
```

### Ayrıca bakınız

* class [CompositeNode](../../aspose.words/compositenode/)
* ad alanı [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* toplantı [Aspose.Words](../../)
