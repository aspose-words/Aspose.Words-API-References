---
title: DocumentVisitor.VisitBuildingBlockEnd
linktitle: VisitBuildingBlockEnd
articleTitle: VisitBuildingBlockEnd
second_title: Aspose.Words для .NET
description: Изучите метод DocumentVisitor VisitBuildingBlockEnd, который запускается в конце перечисления строительных блоков для эффективной обработки документов.
type: docs
weight: 60
url: /ru/net/aspose.words/documentvisitor/visitbuildingblockend/
---
## DocumentVisitor.VisitBuildingBlockEnd method

Вызывается, когда перечисление строительного блока завершено.

```csharp
public virtual VisitorAction VisitBuildingBlockEnd(BuildingBlock block)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| block | BuildingBlock | Посещаемый объект. |

### Возвращаемое значение

А[`VisitorAction`](../../visitoraction/) значение, указывающее, как продолжить перечисление.

## Примечания

Примечание: узел строительного блока и его дочерние элементы не посещаются при выполнении посетителя a над[`Document`](../../document/) . Если вы хотите выполнить Посетителя над строительным блоком a , вам нужно выполнить Посетителя над[`GlossaryDocument`](../../../aspose.words.buildingblocks/glossarydocument/) или вызов[`Accept`](../../../aspose.words.buildingblocks/buildingblock/accept/) .

## Примеры

Показывает способы доступа к строительным блокам в документе глоссария.

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

    // Существуют различные способы доступа к строительным блокам.
    // 1 — Получить первый/последний строительный блок в коллекции:
    Assert.AreEqual("Block 1", glossaryDoc.FirstBuildingBlock.Name);
    Assert.AreEqual("Block 5", glossaryDoc.LastBuildingBlock.Name);

    // 2 - Получить строительный блок по индексу:
    Assert.AreEqual("Block 2", glossaryDoc.BuildingBlocks[1].Name);
    Assert.AreEqual("Block 3", glossaryDoc.BuildingBlocks.ToArray()[2].Name);

    // 3 — Получить первый строительный блок, соответствующий галерее, названию и категории:
    Assert.AreEqual("Block 4", 
        glossaryDoc.GetBuildingBlock(BuildingBlockGallery.All, "(Empty Category)", "Block 4").Name);

    // Мы сделаем это с помощью пользовательского посетителя,
    // который присвоит каждому BuildingBlock в GlossaryDocument уникальный GUID
    GlossaryDocVisitor visitor = new GlossaryDocVisitor();
    // Перейти к началу/концу документа Глоссария.
    glossaryDoc.Accept(visitor);
    // Посетить только начало документа Глоссарий.
    glossaryDoc.AcceptStart(visitor);
    // Посетите только конец документа Глоссарий.
    glossaryDoc.AcceptEnd(visitor);
    Console.WriteLine(visitor.GetText());

    // В Microsoft Word мы можем получить доступ к строительным блокам через «Вставка» -> «Быстрые элементы» -> «Организатор строительных блоков».
    doc.Save(ArtifactsDir + "BuildingBlocks.GlossaryDocument.dotx"); 
}

/// <summary>
/// Присваивает каждому строительному блоку в посещенном документе глоссария уникальный GUID.
/// Сохраняет пары GUID-строительный блок в словаре.
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

* enum [VisitorAction](../../visitoraction/)
* class [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)
* class [DocumentVisitor](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
