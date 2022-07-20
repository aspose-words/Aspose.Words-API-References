---
title: BuildingBlockType
second_title: Aspose.Words for .NET API Referansı
description: Bir yapı taşı tipini belirtir. Tür Microsoft Word. yapı taşının görünürlüğünü ve davranışını etkileyebilir.
type: docs
weight: 160
url: /tr/net/aspose.words.buildingblocks/buildingblocktype/
---
## BuildingBlockType enumeration

Bir yapı taşı tipini belirtir. Tür, Microsoft Word. yapı taşının görünürlüğünü ve davranışını etkileyebilir.

```csharp
public enum BuildingBlockType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Yapı taşı için hiçbir tür bilgisi belirtilmedi. |
| AutomaticallyReplaceNameWithContent | `1` | Yapı taşının, adı bir uygulamaya girildiğinde belgeye otomatik olarak eklenmesine izin verir. |
| StructuredDocumentTagPlaceholderText | `2` | Yapı taşı, yapılandırılmış bir belge etiketi yer tutucu metnidir. |
| FormFieldHelpText | `3` | Yapı taşı, bir form alanı yardım metnidir. |
| Normal | `4` | Yapı taşı, normal (yani normal) bir sözlük belgesi girişidir. |
| AutoCorrect | `5` | Yapı taşı, yazım ve dil bilgisi araçlarıyla ilişkilidir. |
| AutoText | `6` | Yapı taşı bir Otomatik Metin girişidir. |
| All | `7` | Yapı taşı tüm türlerle ilişkilidir. |
| Default | `0` | Farklı kaydetNone . |

### Notlar

karşılık gelir **ST_DocPartType** OOXML'yi yazın.

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

* ad alanı [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
