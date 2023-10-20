---
title: GlossaryDocument.GetBuildingBlock
linktitle: GetBuildingBlock
articleTitle: GetBuildingBlock
second_title: Aspose.Words for .NET
description: GlossaryDocument GetBuildingBlock yöntem. Belirtilen galeriyi kategoriyi ve adı kullanarak bir yapı taşı bulur C#'da.
type: docs
weight: 70
url: /tr/net/aspose.words.buildingblocks/glossarydocument/getbuildingblock/
---
## GlossaryDocument.GetBuildingBlock method

Belirtilen galeriyi, kategoriyi ve adı kullanarak bir yapı taşı bulur.

```csharp
public BuildingBlock GetBuildingBlock(BuildingBlockGallery gallery, string category, string name)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| gallery | BuildingBlockGallery | Galeri kriterleri. |
| category | String | Kategori kriterleri. Olabilir`hükümsüz`bu durumda karşılaştırma amacıyla kullanılmayacaktır. |
| name | String | Yapı taşı adı kriterleri. |

### Geri dönüş değeri

Eşleşen yapı taşı veya`hükümsüz` bir eşleşme bulunamazsa.

## Notlar

Bu, bu koleksiyondaki tüm yapı blokları üzerinde yinelenen ve belirtilen galeri, kategori ve adla eşleşen ilk yapı bloğunu döndüren kullanışlı bir yöntemdir.

Microsoft Word, yapı taşlarını galeriler halinde düzenler. galeriler , kullanılarak önceden tanımlanır.[`BuildingBlockGallery`](../../buildingblockgallery/) enum. Her galeride yapı taşları bir veya daha fazla kategori halinde düzenlenebilir. Kategori adı bir dizedir. Her yapı taşının bir adı vardır. Bir yapı bloğu adının benzersiz olacağı garanti edilmez.

## Örnekler

Bir sözlük belgesinde yapı taşlarına erişmenin yollarını gösterir.

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

    // 3 - Galeri, ad ve kategoriyle eşleşen ilk yapı taşını alın:
    Assert.AreEqual("Block 4", 
        glossaryDoc.GetBuildingBlock(BuildingBlockGallery.All, "(Empty Category)", "Block 4").Name);

    // Bunu özel bir ziyaretçi kullanarak yapacağız,
    // bu, GlossaryDocument'teki her BuildingBlock'a benzersiz bir GUID verecektir
    GlossaryDocVisitor visitor = new GlossaryDocVisitor();
    glossaryDoc.Accept(visitor);
    Console.WriteLine(visitor.GetText());

    // Microsoft Word'de yapı taşlarına "Ekle" --> aracılığıyla erişebiliriz. "Hızlı Parçalar" -> "Yapı Taşları Organizatörü".
    doc.Save(ArtifactsDir + "BuildingBlocks.GlossaryDocument.dotx"); 
}

/// <summary>
/// Ziyaret edilen bir sözlük belgesindeki her yapı taşına benzersiz bir GUID verir.
/// GUID yapı bloğu çiftlerini bir sözlükte saklar.
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

* class [BuildingBlock](../../buildingblock/)
* enum [BuildingBlockGallery](../../buildingblockgallery/)
* class [GlossaryDocument](../)
* ad alanı [Aspose.Words.BuildingBlocks](../../../aspose.words.buildingblocks/)
* toplantı [Aspose.Words](../../../)
