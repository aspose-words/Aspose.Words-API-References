---
title: BuildingBlockGallery Enum
linktitle: BuildingBlockGallery
articleTitle: BuildingBlockGallery
second_title: .NET için Aspose.Words
description: Verimli belge yönetimi ve organizasyonu için önceden tanımlanmış galerilere yönelik rehberiniz olan Aspose.Words BuildingBlockGallery enum'u keşfedin. İş akışınızı bugün geliştirin!
type: docs
weight: 350
url: /tr/net/aspose.words.buildingblocks/buildingblockgallery/
---
## BuildingBlockGallery enumeration

Bir yapı bloğunun sınıflandırıldığı önceden tanımlanmış galeriyi belirtir.

```csharp
public enum BuildingBlockGallery
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| All | `0` | Bu sözlük belge girişinin tüm olası galeri sınıflandırma değerleriyle ilişkilendirileceğini belirtir. |
| AutoText | `1` |  |
| Bibliography | `2` |  |
| CoverPage | `3` |  |
| CustomAutoText | `4` |  |
| CustomBibliography | `5` |  |
| CustomCoverPage | `6` |  |
| CustomEquations | `7` |  |
| CustomFooters | `8` |  |
| CustomHeaders | `9` |  |
| Custom1 | `10` |  |
| Custom2 | `11` |  |
| Custom3 | `12` |  |
| Custom4 | `13` |  |
| Custom5 | `14` |  |
| CustomPageNumber | `15` |  |
| CustomPageNumberAtBottom | `16` |  |
| CustomPageNumberAtMargin | `17` |  |
| CustomPageNumberAtTop | `18` |  |
| CustomQuickParts | `19` |  |
| CustomTableOfContents | `20` |  |
| CustomTables | `21` |  |
| CustomTextBox | `22` |  |
| CustomWatermarks | `23` |  |
| NoGallery | `24` |  |
| QuickParts | `25` |  |
| Equations | `26` |  |
| Footers | `27` |  |
| Headers | `28` |  |
| PageNumber | `29` |  |
| PageNumberAtBottom | `30` |  |
| PageNumberAtMargin | `31` |  |
| PageNumberAtTop | `32` |  |
| StructuredDocumentTagPlaceholderText | `33` |  |
| TableOfContents | `34` |  |
| Tables | `35` |  |
| TextBox | `36` |  |
| Watermarks | `37` |  |
| Default | `0` | AynısıAll . |

## Notlar

Karşılık gelir**ST_DocPartGallery** OOXML yazın.

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

* ad alanı [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* toplantı [Aspose.Words](../../)
