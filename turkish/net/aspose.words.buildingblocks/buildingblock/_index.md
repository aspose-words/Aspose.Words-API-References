---
title: Class BuildingBlock
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.BuildingBlocks.BuildingBlock sınıf. Yapı Taşı Otomatik Metin veya Otomatik Düzelt girişi gibi bir sözlük belgesi girişini temsil eder.
type: docs
weight: 120
url: /tr/net/aspose.words.buildingblocks/buildingblock/
---
## BuildingBlock class

Yapı Taşı, Otomatik Metin veya Otomatik Düzelt girişi gibi bir sözlük belgesi girişini temsil eder.

```csharp
public class BuildingBlock : CompositeNode
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [BuildingBlock](buildingblock/)(GlossaryDocument) | Bu sınıfın yeni bir örneğini başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Behavior](../../aspose.words.buildingblocks/buildingblock/behavior/) { get; set; } | Yapı bloğunun içeriği ana belgeye eklendiğinde uygulanacak davranışı belirtir. |
| [Category](../../aspose.words.buildingblocks/buildingblock/category/) { get; set; } | Yapı taşı için ikinci düzey kategorizasyonu belirtir. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Bu düğümün tüm acil alt düğümlerini alır. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün acil alt öğelerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| [Description](../../aspose.words.buildingblocks/buildingblock/description/) { get; set; } | Bu yapı taşıyla ilişkili açıklamayı alır veya ayarlar. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk alt öğesini alır. |
| [FirstSection](../../aspose.words.buildingblocks/buildingblock/firstsection/) { get; } | Yapı taşındaki ilk bölümü alır. |
| [Gallery](../../aspose.words.buildingblocks/buildingblock/gallery/) { get; set; } | sınıflandırma veya kullanıcı arabirimi sıralama amaçları için yapı taşı için birinci düzey kategorizasyonu belirtir. |
| [Guid](../../aspose.words.buildingblocks/buildingblock/guid/) { get; set; } | Bu yapı taşını benzersiz şekilde tanımlayan bir tanımlayıcı (128 bit GUID) alır veya ayarlar. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Bu düğümün herhangi bir alt düğümü varsa doğru döndürür. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Bu düğümün alt düğümleri olabileceğinden true değerini döndürür. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son alt öğesini alır. |
| [LastSection](../../aspose.words.buildingblocks/buildingblock/lastsection/) { get; } | Yapı taşındaki son bölümü alır. |
| [Name](../../aspose.words.buildingblocks/buildingblock/name/) { get; set; } | Bu yapı taşının adını alır veya ayarlar. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümden hemen sonraki düğümü alır. |
| override [NodeType](../../aspose.words.buildingblocks/buildingblock/nodetype/) { get; } | BuildingBlock değer. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün hemen üst öğesini alır. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir döndürür **Menzil** belgenin bu düğümde bulunan bölümünü temsil eden nesne. |
| [Sections](../../aspose.words.buildingblocks/buildingblock/sections/) { get; } | Yapı taşındaki tüm bölümleri temsil eden bir koleksiyon döndürür. |
| [Type](../../aspose.words.buildingblocks/buildingblock/type/) { get; set; } | Yapı taşı türünü belirtir. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words.buildingblocks/buildingblock/accept/)(DocumentVisitor) | Bir ziyaretçiyi kabul eder. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin sonuna ekler. |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Sistem kullanımı için ayrılmıştır. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Belirtilenin ilk atasını alır[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Belirtilen nesne türünün ilk üst öğesini alır. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Belirtilen türle eşleşen N. alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Belirtilen türle eşleşen canlı bir alt düğüm koleksiyonu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bu düğümün alt düğümleri üzerinde her stil yinelemesi için destek sağlar. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Bu düğümün ve tüm alt öğelerinin metnini alır. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Alt düğüm dizisindeki belirtilen alt düğümün dizinini döndürür. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Belirtilen referans düğümünden hemen sonra belirtilen düğümü ekler. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Belirtilen düğümü, belirtilen referans düğümünden hemen önce ekler. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin başına ekler. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini üst öğeden kaldırır. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Belirtilen alt düğümü kaldırır. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tümünü kaldırır[`SmartTag`](../../aspose.words.markup/smarttag/) geçerli düğümün alt düğümleri. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | XPath ifadesiyle eşleşen düğümlerin listesini seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | XPath ifadesiyle eşleşen ilk Düğümü seçer. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

### Notlar

`BuildingBlock` sadece içerebilir[`Section`](../../aspose.words/section/) düğümler.

`BuildingBlock` sadece çocuğu olabilir[`GlossaryDocument`](../glossarydocument/).

Yeni yapı taşları oluşturabilir ve bunları bir sözlük belgesine ekleyebilirsiniz. Mevcut yapı taşlarını değiştirebilir veya silebilirsiniz. Belgeler arasında yapı taşlarını kopyalayabilir veya taşıyabilirsiniz. Bir yapı taşının içeriğini bir belgeye ekleyebilirsiniz.

karşılık gelir **docPart** , **docPartPr** ve **docPartVücut**OOXML'deki öğeler.

### Örnekler

Bir belgeye özel bir yapı taşının nasıl ekleneceğini gösterir.

```csharp
public void CreateAndInsert()
{
    // Bir belgenin sözlük belgesi, yapı taşlarını saklar.
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();
    doc.GlossaryDocument = glossaryDoc;

    // Bir yapı taşı oluşturun, adlandırın ve ardından onu sözlük belgesine ekleyin.
    BuildingBlock block = new BuildingBlock(glossaryDoc)
    {
        Name = "Custom Block"
    };

    glossaryDoc.AppendChild(block);

    // Tüm yeni yapı taşı GUID'leri varsayılan olarak aynı sıfır değerine sahiptir ve onlara yeni bir benzersiz değer verebiliriz.
    Assert.AreEqual("00000000-0000-0000-0000-000000000000", block.Guid.ToString());

    block.Guid = Guid.NewGuid();

    // Aşağıdaki özellikler yapı taşlarını sınıflandırır
    // menüde Microsoft Word'de "Ekle" -> "Hızlı Parçalar" -> "Yapı Taşları Organizatör".
    Assert.AreEqual("(Empty Category)", block.Category);
    Assert.AreEqual(BuildingBlockType.None, block.Type);
    Assert.AreEqual(BuildingBlockGallery.All, block.Gallery);
    Assert.AreEqual(BuildingBlockBehavior.Content, block.Behavior);

    // Bu yapı taşını belgemize eklemeden önce, ona bazı içerikler vermemiz gerekecek,
    // bunu bir belge ziyaretçisi kullanarak yapacağız. Bu ziyaretçi ayrıca bir kategori, galeri ve davranış belirleyecektir.
    BuildingBlockVisitor visitor = new BuildingBlockVisitor(glossaryDoc);
    block.Accept(visitor);

    // Az önce oluşturduğumuz bloğa sözlük belgesinden erişebiliriz.
    BuildingBlock customBlock = glossaryDoc.GetBuildingBlock(BuildingBlockGallery.QuickParts,
        "My custom building blocks", "Custom Block");

    // Bloğun kendisi metni içeren bir bölümdür.
    Assert.AreEqual($"Text inside {customBlock.Name}\f", customBlock.FirstSection.Body.FirstParagraph.GetText());
    Assert.AreEqual(customBlock.FirstSection, customBlock.LastSection);

    // Artık belgeye yeni bir bölüm olarak ekleyebiliriz.
    doc.AppendChild(doc.ImportNode(customBlock.FirstSection, true));

    // Microsoft Word'ün Building Blocks Organizer'ında da bulabilir ve manuel olarak yerleştirebiliriz.
    doc.Save(ArtifactsDir + "BuildingBlocks.CreateAndInsert.dotx");
}

/// <summary>
/// Belgeye hızlı bir parça olarak eklenecek ziyaret edilmiş bir yapı taşı kurar ve içeriğine metin ekler.
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
        // Yapı taşını hızlı bir parça olarak yapılandırın ve Yapı Taşları Düzenleyicisi tarafından kullanılan özellikleri ekleyin.
        block.Behavior = BuildingBlockBehavior.Paragraph;
        block.Category = "My custom building blocks";
        block.Description =
            "Using this block in the Quick Parts section of word will place its contents at the cursor.";
        block.Gallery = BuildingBlockGallery.QuickParts;

        // Metin içeren bir bölüm ekleyin.
        // Bloğun belgeye eklenmesi, bu bölümü konumdaki alt düğümleriyle birlikte ekler.
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


