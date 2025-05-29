---
title: BuildingBlockCollection Class
linktitle: BuildingBlockCollection
articleTitle: BuildingBlockCollection
second_title: .NET için Aspose.Words
description: Belge BuildingBlock nesnelerini verimli bir şekilde yönetmek ve iş akışınızı geliştirmek için güçlü bir araç olan Aspose.Words BuildingBlockCollection sınıfını keşfedin.
type: docs
weight: 340
url: /tr/net/aspose.words.buildingblocks/buildingblockcollection/
---
## BuildingBlockCollection class

Bir koleksiyon[`BuildingBlock`](../buildingblock/) belgedeki nesneler.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Aspose.Words Belge Nesne Modeli (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) belgeleme makalesi.

```csharp
public class BuildingBlockCollection : NodeCollection
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Koleksiyondaki düğüm sayısını alır. |
| [Item](../../aspose.words.buildingblocks/buildingblockcollection/item/) { get; } | Belirtilen dizindeki bir yapı bloğunu alır. (2 indexers) |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../../aspose.words/node/)*) | Koleksiyonun sonuna bir düğüm ekler. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Bu koleksiyondan ve belgeden tüm düğümleri kaldırır. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../../aspose.words/node/)*) | Bir düğümün koleksiyonda olup olmadığını belirler. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Düğüm koleksiyonu üzerinde basit bir "foreach" tarzı yineleme sağlar. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../../aspose.words/node/)*) | Belirtilen düğümün sıfır tabanlı dizinini döndürür. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../../aspose.words/node/)*) | Belirtilen dizinde koleksiyona bir düğüm ekler. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../../aspose.words/node/)*) | Düğümü koleksiyondan ve belgeden kaldırır. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Belirtilen dizindeki düğümü koleksiyondan ve belgeden kaldırır. |
| [ToArray](../../aspose.words.buildingblocks/buildingblockcollection/toarray/#toarray)() | Koleksiyondaki tüm yapı taşlarını yeni bir yapı taşı dizisine kopyalar. (2 methods) |

## Notlar

Bu sınıfın örneklerini doğrudan oluşturmazsınız. Yapı taşlarından oluşan koleksiyonuna erişmek için şunu kullanın:[`BuildingBlocks`](../glossarydocument/buildingblocks/) mülk.

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

* class [NodeCollection](../../aspose.words/nodecollection/)
* ad alanı [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* toplantı [Aspose.Words](../../)
