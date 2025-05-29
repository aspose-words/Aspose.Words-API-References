---
title: GlossaryDocument Class
linktitle: GlossaryDocument
articleTitle: GlossaryDocument
second_title: .NET için Aspose.Words
description: Word belgelerinizde Otomatik Metin ve Yapı Taşlarını kusursuz bir şekilde yönetmenin anahtarı olan Aspose.Words.BuildingBlocks.GlossaryDocument sınıfını keşfedin.
type: docs
weight: 370
url: /tr/net/aspose.words.buildingblocks/glossarydocument/
---
## GlossaryDocument class

Word belgesi içindeki bir sözlük belgesinin kök öğesini temsil eder. Bir sözlük belgesi, Otomatik Metin, Otomatik Düzeltme girdileri ve Yapı Taşları için bir depolama alanıdır.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Aspose.Words Belge Nesne Modeli (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) belgeleme makalesi.

```csharp
public class GlossaryDocument : DocumentBase
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [GlossaryDocument](glossarydocument/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | Belgenin arka plan şeklini alır veya ayarlar.`hükümsüz` . |
| [BuildingBlocks](../../aspose.words.buildingblocks/glossarydocument/buildingblocks/) { get; } | Sözlük belgesindeki tüm yapı taşlarını temsil eden türlendirilmiş bir koleksiyon döndürür. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün hemen alt düğümlerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| override [Document](../../aspose.words/documentbase/document/) { get; } | Bu örneği alır. |
| [FirstBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/firstbuildingblock/) { get; } | Sözlük belgesindeki ilk yapı taşını alır. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk çocuğunu alır. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | Bu belgede kullanılan yazı tiplerinin özelliklerine erişim sağlar. |
| [FootnoteSeparators](../../aspose.words/documentbase/footnoteseparators/) { get; } | Belgede tanımlanan dipnot/sonnot ayırıcılarına erişim sağlar. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Geri Döndürür`doğru` eğer bu düğümün herhangi bir alt düğümü varsa. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Geri Döndürür`doğru` çünkü bu düğümün alt düğümleri olabilir. |
| [LastBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/lastbuildingblock/) { get; } | Sözlük belgesindeki son yapı taşını alır. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son çocuğunu alır. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | Belgede kullanılan liste biçimlendirmesine erişim sağlar. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümü hemen takip eden düğümü alır. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | Belgeye bir düğüm eklendiğinde veya kaldırıldığında çağrılır. |
| override [NodeType](../../aspose.words.buildingblocks/glossarydocument/nodetype/) { get; } | şunu döndürür:GlossaryDocument değer. |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | Belgenin sayfa rengini alır veya ayarlar. Bu özellik, daha basit bir sürümüdür[`BackgroundShape`](../../aspose.words/documentbase/backgroundshape/) . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün en yakın üst düğümünü alır. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir[`Range`](../../aspose.words/range/)bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | Harici kaynakların nasıl yükleneceğini kontrol etmenizi sağlar. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | Belgede tanımlanan stil koleksiyonunu döndürür. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | Çeşitli belge işleme prosedürleri sırasında, veri veya biçimlendirme sadakat kaybına neden olabilecek bir sorun algılandığında çağrılır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words.buildingblocks/glossarydocument/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Bir ziyaretçiyi kabul eder. |
| override [AcceptEnd](../../aspose.words.buildingblocks/glossarydocument/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Sözlük belgesinin sonunu ziyaret eden bir ziyaretçiyi kabul eder. |
| override [AcceptStart](../../aspose.words.buildingblocks/glossarydocument/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Sözlük belgesinin başlangıcını ziyaret eden bir ziyaretçiyi kabul eder. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Belirtilen düğümü bu düğüm için alt düğümler listesinin sonuna ekler. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Düğümleri gezmek ve okumak için kullanılabilen gezgini oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Belirtilenin ilk atasını alır[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Belirtilen nesne türünün ilk atasını alır. |
| [GetBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/getbuildingblock/)(*[BuildingBlockGallery](../buildingblockgallery/), string, string*) | Belirtilen galeri, kategori ve adı kullanarak bir yapı bloğu bulur. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Belirtilen türle eşleşen N'inci alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bu düğümün alt düğümleri üzerindeki her stil yinelemesi için destek sağlar. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Bu düğümün ve tüm alt düğümlerinin metnini alır. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../../aspose.words/node/), bool*) | Başka bir belgeden bir düğümü geçerli belgeye aktarır. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../../aspose.words/node/), bool, [ImportFormatMode](../../aspose.words/importformatmode/)*) | Biçimlendirmeyi kontrol etme seçeneğiyle başka bir belgeden geçerli belgeye bir düğüm aktarır. |
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

Bazı belgeler, genellikle şablonlar, Otomatik Metin, Otomatik Düzeltme girdileri ve/veya Yapı Taşları (ayrıca şu şekilde bilinir) içerebilir:sözlük belge girişleri ,belge parçaları veyayapı taşları).

Yapı taşlarına erişmek için bir belgeyi bir[`Document`](../../aspose.words/document/) nesnesi. Yapı taşları şu şekilde kullanılabilir:[`GlossaryDocument`](../../aspose.words/document/glossarydocument/) mülk.

`GlossaryDocument` herhangi bir sayıda içerebilir[`BuildingBlock`](../buildingblock/)nesneler. Her biri[`BuildingBlock`](../buildingblock/) bir belge parçasını temsil eder.

Karşılık gelir**sözlükBelge** Ve**docParçaları**OOXML'deki öğeler.

## Örnekler

Bir sözlük belgesindeki yapı taşlarına erişim yollarını gösterir.

```csharp
public void GlossaryDocument()
{
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();

    BuildingBlock child1 = new BuildingBlock(glossaryDoc) { Name = "Block 1" };
    glossaryDoc.AppendChild(child1);
    BuildingBlock child2 = new BuildingBlock(glossaryDoc) { Name = "Block 2" };
    glossaryDoc.AppendChild(child2);
    BuildingBlock child3 = new BuildingBlock(glossaryDoc) { Name = "Block 3" };
    glossaryDoc.AppendChild(child3);
    BuildingBlock child4 = new BuildingBlock(glossaryDoc) { Name = "Block 4" };
    glossaryDoc.AppendChild(child4);
    BuildingBlock child5 = new BuildingBlock(glossaryDoc) { Name = "Block 5" };
    glossaryDoc.AppendChild(child5);

    Assert.AreEqual(5, glossaryDoc.BuildingBlocks.Count);

    doc.GlossaryDocument = glossaryDoc;

    // Yapı taşlarına erişmenin çeşitli yolları vardır.
    // 1 - Koleksiyondaki ilk/son yapı taşlarını al:
    Assert.AreEqual("Block 1", glossaryDoc.FirstBuildingBlock.Name);
    Assert.AreEqual("Block 5", glossaryDoc.LastBuildingBlock.Name);

    // 2 - Dizin yoluyla bir yapı bloğunu al:
    Assert.AreEqual("Block 2", glossaryDoc.BuildingBlocks[1].Name);
    Assert.AreEqual("Block 3", glossaryDoc.BuildingBlocks.ToArray()[2].Name);

    // 3 - Bir galeriye, isme ve kategoriye uyan ilk yapı taşını al:
    Assert.AreEqual("Block 4", 
        glossaryDoc.GetBuildingBlock(BuildingBlockGallery.All, "(Empty Category)", "Block 4").Name);

    // Bunu özel bir ziyaretçi kullanarak yapacağız,
    // GlossaryDocument'taki her BuildingBlock'a benzersiz bir GUID verecek
    GlossaryDocVisitor visitor = new GlossaryDocVisitor();
    // Sözlük belgesinin başlangıcını/sonunu ziyaret edin.
    glossaryDoc.Accept(visitor);
    // Sözlük belgesinin yalnızca başlangıcını ziyaret edin.
    glossaryDoc.AcceptStart(visitor);
    // Sadece Sözlük belgesinin sonunu ziyaret edin.
    glossaryDoc.AcceptEnd(visitor);
    Console.WriteLine(visitor.GetText());

    // Microsoft Word'de yapı taşlarına "Ekle" -> "Hızlı Parçalar" -> "Yapı Taşları Düzenleyicisi" yoluyla erişebiliriz.
    doc.Save(ArtifactsDir + "BuildingBlocks.GlossaryDocument.dotx"); 
}

/// <summary>
/// Ziyaret edilen sözlük belgesindeki her yapı bloğuna benzersiz bir GUID verir.
/// GUID yapı taşı çiftlerini bir sözlükte depolar.
/// </summary>
public class GlossaryDocVisitor : DocumentVisitor
{
    public GlossaryDocVisitor()
    {
        mBlocksByGuid = new Dictionary<Guid, BuildingBlock>();
        mBuilder = new StringBuilder();
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    public Dictionary<Guid, BuildingBlock> GetDictionary()
    {
        return mBlocksByGuid;
    }

    public override VisitorAction VisitGlossaryDocumentStart(GlossaryDocument glossary)
    {
        mBuilder.AppendLine("Glossary document found!");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitGlossaryDocumentEnd(GlossaryDocument glossary)
    {
        mBuilder.AppendLine("Reached end of glossary!");
        mBuilder.AppendLine("BuildingBlocks found: " + mBlocksByGuid.Count);
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBuildingBlockStart(BuildingBlock block)
    {
        block.Guid = Guid.NewGuid();
        mBlocksByGuid.Add(block.Guid, block);
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBuildingBlockEnd(BuildingBlock block)
    {
        mBuilder.AppendLine("\tVisited block \"" + block.Name + "\"");
        mBuilder.AppendLine("\t Type: " + block.Type);
        mBuilder.AppendLine("\t Gallery: " + block.Gallery);
        mBuilder.AppendLine("\t Behavior: " + block.Behavior);
        mBuilder.AppendLine("\t Description: " + block.Description);

        return VisitorAction.Continue;
    }

    private readonly Dictionary<Guid, BuildingBlock> mBlocksByGuid;
    private readonly StringBuilder mBuilder;
}
```

### Ayrıca bakınız

* class [DocumentBase](../../aspose.words/documentbase/)
* ad alanı [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* toplantı [Aspose.Words](../../)
