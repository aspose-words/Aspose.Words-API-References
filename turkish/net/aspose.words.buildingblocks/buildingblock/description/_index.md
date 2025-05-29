---
title: BuildingBlock.Description
linktitle: Description
articleTitle: Description
second_title: .NET için Aspose.Words
description: BuildingBlock açıklamanızı zahmetsizce yönetin. Projelerinizde gelişmiş organizasyon ve netlik için açıklamaları kolayca ayarlayın veya güncelleyin.
type: docs
weight: 40
url: /tr/net/aspose.words.buildingblocks/buildingblock/description/
---
## BuildingBlock.Description property

Bu yapı bloğuyla ilişkili açıklamayı alır veya ayarlar.

```csharp
public string Description { get; set; }
```

## Notlar

Açıklama herhangi bir dize içeriğini, genellikle ek bilgileri içerebilir.

Olamaz`hükümsüz`, ancak boş bir dize de olabilir.

Karşılık gelir**docPartPr.açıklaması** OOXML'deki öğe.

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

* class [BuildingBlock](../)
* ad alanı [Aspose.Words.BuildingBlocks](../../../aspose.words.buildingblocks/)
* toplantı [Aspose.Words](../../../)
