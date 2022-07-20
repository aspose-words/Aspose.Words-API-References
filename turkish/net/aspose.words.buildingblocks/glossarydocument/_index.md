---
title: GlossaryDocument
second_title: Aspose.Words for .NET API Referansı
description: Bir Word belgesi içindeki bir sözlük belgesinin kök öğesini temsil eder. Sözlük belgesi Otomatik Metin Otomatik Düzelt girdileri ve Yapı Taşları için bir depolama alanıdır.
type: docs
weight: 170
url: /tr/net/aspose.words.buildingblocks/glossarydocument/
---
## GlossaryDocument class

Bir Word belgesi içindeki bir sözlük belgesinin kök öğesini temsil eder. Sözlük belgesi, Otomatik Metin, Otomatik Düzelt girdileri ve Yapı Taşları için bir depolama alanıdır.

```csharp
public class GlossaryDocument : DocumentBase
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [GlossaryDocument](glossarydocument)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape) { get; set; } | Belgenin arka plan şeklini alır veya ayarlar. null. olabilir |
| [BuildingBlocks](../../aspose.words.buildingblocks/glossarydocument/buildingblocks) { get; } | Sözlük belgesindeki tüm yapı taşlarını temsil eden yazılı bir koleksiyon döndürür. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Bu düğümün tüm acil alt düğümlerini alır. |
| [Count](../../aspose.words/compositenode/count) { get; } | Bu düğümün acil alt öğelerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| override [Document](../../aspose.words/documentbase/document) { get; } |  |
| [FirstBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/firstbuildingblock) { get; } | Sözlük belgesindeki ilk yapı taşını alır. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Düğümün ilk alt öğesini alır. |
| [FontInfos](../../aspose.words/documentbase/fontinfos) { get; } | Bu belgede kullanılan yazı tiplerinin özelliklerine erişim sağlar. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Bu düğümün herhangi bir alt düğümü varsa doğru döndürür. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Bu düğümün alt düğümleri olabileceğinden true değerini döndürür. |
| [LastBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/lastbuildingblock) { get; } | Sözlük belgesindeki son yapı taşını alır. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Düğümün son alt öğesini alır. |
| [Lists](../../aspose.words/documentbase/lists) { get; } | Belgede kullanılan liste formatına erişim sağlar. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Bu düğümden hemen sonraki düğümü alır. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback) { get; set; } | Belgeye bir düğüm eklendiğinde veya kaldırıldığında çağrılır. |
| override [NodeType](../../aspose.words.buildingblocks/glossarydocument/nodetype) { get; } | GlossaryDocument değer. |
| [PageColor](../../aspose.words/documentbase/pagecolor) { get; set; } | Belgenin sayfa rengini alır veya ayarlar. Bu özellik, aşağıdakilerin daha basit bir sürümüdür:[`BackgroundShape`](../../aspose.words/documentbase/backgroundshape) . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Bu düğümün hemen üst öğesini alır. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range) { get; } | Bir döndürür **Menzil** belgenin bu düğümde bulunan bölümünü temsil eden nesne. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback) { get; set; } | Harici kaynakların nasıl yüklendiğini kontrol etmeye izin verir. |
| [Styles](../../aspose.words/documentbase/styles) { get; } | Belgede tanımlanan stillerin bir koleksiyonunu döndürür. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback) { get; set; } | Verilerde veya biçimlendirme aslına uygunluk kaybına neden olabilecek bir sorun algılandığında çeşitli belge işleme prosedürleri sırasında çağrılır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words.buildingblocks/glossarydocument/accept)(DocumentVisitor) | Bir ziyaretçiyi kabul eder. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin sonuna ekler. |
| [Clone](../../aspose.words/node/clone)(bool) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Sistem kullanımı için ayrılmıştır. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Belirtilenin ilk atasını alır[`NodeType`](../../aspose.words/nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Belirtilen nesne türünün ilk üst öğesini alır. |
| [GetBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/getbuildingblock)(BuildingBlockGallery, string, string) | Belirtilen galeri, kategori ve adı kullanarak bir yapı taşı bulur. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Belirtilen türle eşleşen N. alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Belirtilen türle eşleşen canlı bir alt düğüm koleksiyonu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Bu düğümün alt düğümleri üzerinde her stil yinelemesi için destek sağlar. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Bu düğümün ve tüm alt öğelerinin metnini alır. |
| [ImportNode](../../aspose.words/documentbase/importnode)(Node, bool) | Bir düğümü başka bir belgeden geçerli belgeye aktarır. |
| [ImportNode](../../aspose.words/documentbase/importnode)(Node, bool, ImportFormatMode) | Biçimlendirmeyi kontrol etme seçeneği ile bir düğümü başka bir belgeden geçerli belgeye aktarır. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Alt düğüm dizisindeki belirtilen alt düğümün dizinini döndürür. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Belirtilen referans düğümünden hemen sonra belirtilen düğümü ekler. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Belirtilen düğümü, belirtilen referans düğümünden hemen önce ekler. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin başına ekler. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove)() | Kendini üst öğeden kaldırır. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Belirtilen alt düğümü kaldırır. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Tümünü kaldırır[`SmartTag`](../../aspose.words.markup/smarttag) geçerli düğümün alt düğümleri. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | XPath ifadesiyle eşleşen düğümlerin listesini seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | XPath ifadesiyle eşleşen ilk Düğümü seçer. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

### Notlar

Bazı belgeler, genellikle şablonlar, Otomatik Metin, Otomatik Düzeltme girdileri ve/veya Yapı Taşları (olarak da bilinir) içerebilir.sözlük belge girişleri ,belge parçaları veyayapı taşları).

Yapı taşlarına erişmek için bir belgeyi bir[`Document`](../../aspose.words/document) nesne. Yapı taşları,[`GlossaryDocument`](../../aspose.words/document/glossarydocument) Emlak.

[`GlossaryDocument`](../glossarydocument) herhangi bir sayıda içerebilir[`BuildingBlock`](../buildingblock) nesneler. Her biri[`BuildingBlock`](../buildingblock) bir belge bölümünü temsil eder.

karşılık gelir **sözlükBelge** ve **docParts**OOXML'deki öğeler.

### Örnekler

Sözlük belgesindeki yapı taşlarına erişmenin yollarını gösterir.

```csharp
public void GlossaryDocument()
{
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();

    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 1" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 2" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 3" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 4" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 5" });

    Assert.AreEqual(5, glossaryDoc.BuildingBlocks.Count);

    doc.GlossaryDocument = glossaryDoc;

    // Yapı taşlarına erişmenin çeşitli yolları vardır.
    // 1 - Koleksiyondaki ilk/son yapı taşlarını alın:
    Assert.AreEqual("Block 1", glossaryDoc.FirstBuildingBlock.Name);
    Assert.AreEqual("Block 5", glossaryDoc.LastBuildingBlock.Name);

    // 2 - Dizine göre bir yapı taşı alın:
    Assert.AreEqual("Block 2", glossaryDoc.BuildingBlocks[1].Name);
    Assert.AreEqual("Block 3", glossaryDoc.BuildingBlocks.ToArray()[2].Name);

    // 3 - Bir galeri, ad ve kategoriyle eşleşen ilk yapı taşını alın:
    Assert.AreEqual("Block 4", 
        glossaryDoc.GetBuildingBlock(BuildingBlockGallery.All, "(Empty Category)", "Block 4").Name);

    // Bunu özel bir ziyaretçi kullanarak yapacağız,
    // GlossaryDocument'taki her BuildingBlock'a benzersiz bir GUID verecek
    GlossaryDocVisitor visitor = new GlossaryDocVisitor();
    glossaryDoc.Accept(visitor);

    Console.WriteLine(visitor.GetText());

    // Microsoft Word'de yapı taşlarına "Ekle" -> "Hızlı Parçalar" -> "Yapı Taşları Organizatör".
    doc.Save(ArtifactsDir + "BuildingBlocks.GlossaryDocument.dotx"); 
}

/// <summary>
/// Ziyaret edilen bir sözlük belgesindeki her yapı taşına benzersiz bir GUID verir.
/// GUID yapı taşı çiftlerini bir sözlükte saklar.
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

* class [DocumentBase](../../aspose.words/documentbase)
* ad alanı [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
