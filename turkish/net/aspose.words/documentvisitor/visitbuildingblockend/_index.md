---
title: DocumentVisitor.VisitBuildingBlockEnd
linktitle: VisitBuildingBlockEnd
articleTitle: VisitBuildingBlockEnd
second_title: .NET için Aspose.Words
description: Verimli belge işleme için yapı bloğu numaralandırmasının sonunda tetiklenen DocumentVisitor VisitBuildingBlockEnd yöntemini keşfedin.
type: docs
weight: 60
url: /tr/net/aspose.words/documentvisitor/visitbuildingblockend/
---
## DocumentVisitor.VisitBuildingBlockEnd method

Bir yapı bloğunun numaralandırılması sona erdiğinde çağrılır.

```csharp
public virtual VisitorAction VisitBuildingBlockEnd(BuildingBlock block)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| block | BuildingBlock | Ziyaret edilen nesne. |

### Geri dönüş değeri

A[`VisitorAction`](../../visitoraction/) sayımın nasıl devam edeceğini belirten değer.

## Notlar

Not: Bir yapı bloğu düğümü ve onun alt düğümleri, bir a Visitor'ı bir[`Document`](../../document/) . Bir Visitor'ı a yapı bloğu üzerinde çalıştırmak istiyorsanız, Visitor'ı a yapı bloğu üzerinde çalıştırmanız gerekir.[`GlossaryDocument`](../../../aspose.words.buildingblocks/glossarydocument/) or çağrısı[`Accept`](../../../aspose.words.buildingblocks/buildingblock/accept/) .

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

* enum [VisitorAction](../../visitoraction/)
* class [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)
* class [DocumentVisitor](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
