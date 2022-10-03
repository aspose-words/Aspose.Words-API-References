---
title: GetBuildingBlock
second_title: Справочник по API Aspose.Words для .NET
description: Находит стандартный блок используя указанную галерею категорию и имя.
type: docs
weight: 70
url: /ru/net/aspose.words.buildingblocks/glossarydocument/getbuildingblock/
---
## GlossaryDocument.GetBuildingBlock method

Находит стандартный блок, используя указанную галерею, категорию и имя.

```csharp
public BuildingBlock GetBuildingBlock(BuildingBlockGallery gallery, string category, string name)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| gallery | BuildingBlockGallery | Критерии галереи. |
| category | String | Критерии категории. Может быть нулевым, и в этом случае он не будет использоваться для сравнения. |
| name | String | Критерии имени стандартного блока. |

### Возвращаемое значение

Соответствующий стандартный блок или нуль, если совпадение не найдено.

### Примечания

Это удобный метод, который выполняет итерацию по всем стандартным блокам в этой коллекции и возвращает первый стандартный блок, который соответствует указанной коллекции, категории и имени.

Microsoft Word организует стандартные блоки в галереи. Галереи предопределены с помощью[`BuildingBlockGallery`](../../buildingblockgallery/) enum. В каждой галерее стандартные блоки могут быть организованы в одну или несколько категорий. Имя категории представляет собой строку. Каждый строительный блок имеет имя. Уникальность имени Building block не гарантируется.

### Примеры

Показывает способы доступа к стандартным блокам в документе глоссария.

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

    // Существуют различные способы доступа к строительным блокам.
    // 1 - Получить первый/последний строительные блоки в коллекции:
    Assert.AreEqual("Block 1", glossaryDoc.FirstBuildingBlock.Name);
    Assert.AreEqual("Block 5", glossaryDoc.LastBuildingBlock.Name);

    // 2 - Получить строительный блок по индексу:
    Assert.AreEqual("Block 2", glossaryDoc.BuildingBlocks[1].Name);
    Assert.AreEqual("Block 3", glossaryDoc.BuildingBlocks.ToArray()[2].Name);

    // 3 — Получить первый стандартный блок, соответствующий галерее, названию и категории:
    Assert.AreEqual("Block 4", 
        glossaryDoc.GetBuildingBlock(BuildingBlockGallery.All, "(Empty Category)", "Block 4").Name);

    // Мы сделаем это с помощью пользовательского посетителя,
    // что даст каждому BuildingBlock в GlossaryDocument уникальный GUID
    GlossaryDocVisitor visitor = new GlossaryDocVisitor();
    glossaryDoc.Accept(visitor);

    Console.WriteLine(visitor.GetText());

    // В Microsoft Word мы можем получить доступ к строительным блокам через «Вставить» -> "Быстрые детали" -> «Организатор строительных блоков».
    doc.Save(ArtifactsDir + "BuildingBlocks.GlossaryDocument.dotx"); 
}

/// <summary>
/// Присваивает каждому строительному блоку в посещенном документе глоссария уникальный идентификатор GUID.
/// Сохраняет пары блоков GUID в словаре.
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

### Смотрите также

* class [BuildingBlock](../../buildingblock/)
* enum [BuildingBlockGallery](../../buildingblockgallery/)
* class [GlossaryDocument](../)
* пространство имен [Aspose.Words.BuildingBlocks](../../glossarydocument/)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
