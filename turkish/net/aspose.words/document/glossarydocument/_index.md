---
title: Document.GlossaryDocument
linktitle: GlossaryDocument
articleTitle: GlossaryDocument
second_title: Aspose.Words for .NET
description: Document GlossaryDocument mülk. Bu belge veya şablon içindeki sözlük belgesini alır veya ayarlar. Sözlük belgesi bir belgede tanımlanan Otomatik Metin Otomatik Düzeltme ve Yapı Taşı girişleri için bir depolama dir C#'da.
type: docs
weight: 170
url: /tr/net/aspose.words/document/glossarydocument/
---
## Document.GlossaryDocument property

Bu belge veya şablon içindeki sözlük belgesini alır veya ayarlar. Sözlük belgesi, bir belgede tanımlanan Otomatik Metin, Otomatik Düzeltme ve Yapı Taşı girişleri için bir depolama 'dir.

```csharp
public GlossaryDocument GlossaryDocument { get; set; }
```

## Notlar

Bu özellik şunu döndürür:`hükümsüz` belgenin sözlük belgesi yoksa.

a oluşturarak bir belgeye sözlük belgesi ekleyebilirsiniz.[`GlossaryDocument`](../../../aspose.words.buildingblocks/glossarydocument/) nesne ve bu özelliğe atama.

## Örnekler

Bir belgeye özel yapı taşının nasıl ekleneceğini gösterir.

```csharp
public void CreateAndInsert()
{
    // Bir belgenin sözlük belgesi yapı taşlarını saklar.
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
    // Microsoft Word'de "Ekle" yoluyla erişebileceğimiz menüde -> "Hızlı Parçalar" -> "Yapı Taşları Organizatörü".
    Assert.AreEqual("(Empty Category)", block.Category);
    Assert.AreEqual(BuildingBlockType.None, block.Type);
    Assert.AreEqual(BuildingBlockGallery.All, block.Gallery);
    Assert.AreEqual(BuildingBlockBehavior.Content, block.Behavior);

    // Bu yapı taşını belgemize eklemeden önce ona bazı içerikler vermemiz gerekecek,
    // bunu bir belge ziyaretçisi kullanarak yapacağız. Bu ziyaretçi ayrıca bir kategori, galeri ve davranış belirleyecektir.
    BuildingBlockVisitor visitor = new BuildingBlockVisitor(glossaryDoc);
    block.Accept(visitor);

    // Az önce oluşturduğumuz bloğa sözlük belgesinden ulaşabiliyoruz.
    BuildingBlock customBlock = glossaryDoc.GetBuildingBlock(BuildingBlockGallery.QuickParts,
        "My custom building blocks", "Custom Block");

    // Bloğun kendisi metni içeren bir bölümdür.
    Assert.AreEqual($"Text inside {customBlock.Name}\f", customBlock.FirstSection.Body.FirstParagraph.GetText());
    Assert.AreEqual(customBlock.FirstSection, customBlock.LastSection);
    // Artık belgeye yeni bir bölüm olarak ekleyebiliriz.
    doc.AppendChild(doc.ImportNode(customBlock.FirstSection, true));

    // Bunu Microsoft Word'ün Yapı Taşları Düzenleyicisinde de bulabilir ve manuel olarak yerleştirebiliriz.
    doc.Save(ArtifactsDir + "BuildingBlocks.CreateAndInsert.dotx");
}

/// <summary>
/// Belgeye hızlı bir parça olarak eklenecek ziyaret edilen bir yapı taşını ayarlar ve içeriğine metin ekler.
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
        // Yapı taşını hızlı parça olarak yapılandırın ve Yapı Taşları Düzenleyicisi tarafından kullanılan özellikleri ekleyin.
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

* class [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
