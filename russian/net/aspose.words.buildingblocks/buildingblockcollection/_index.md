---
title: BuildingBlockCollection Class
linktitle: BuildingBlockCollection
articleTitle: BuildingBlockCollection
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words BuildingBlockCollection — мощный инструмент для эффективного управления объектами BuildingBlock документа и улучшения рабочего процесса.
type: docs
weight: 340
url: /ru/net/aspose.words.buildingblocks/buildingblockcollection/
---
## BuildingBlockCollection class

Коллекция[`BuildingBlock`](../buildingblock/) объекты в документе.

Чтобы узнать больше, посетите[Объектная модель документа Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) документальная статья.

```csharp
public class BuildingBlockCollection : NodeCollection
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Получает количество узлов в коллекции. |
| [Item](../../aspose.words.buildingblocks/buildingblockcollection/item/) { get; } | Извлекает строительный блок по указанному индексу. (2 indexers) |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../../aspose.words/node/)*) | Добавляет узел в конец коллекции. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Удаляет все узлы из этой коллекции и из документа. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../../aspose.words/node/)*) | Определяет, находится ли узел в коллекции. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Обеспечивает простую итерацию в стиле «foreach» по коллекции узлов. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../../aspose.words/node/)*) | Возвращает индекс указанного узла, отсчитываемый от нуля. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../../aspose.words/node/)*) | Вставляет узел в коллекцию по указанному индексу. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../../aspose.words/node/)*) | Удаляет узел из коллекции и из документа. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Удаляет узел с указанным индексом из коллекции и из документа. |
| [ToArray](../../aspose.words.buildingblocks/buildingblockcollection/toarray/#toarray)() | Копирует все строительные блоки из коллекции в новый массив строительных блоков. (2 methods) |

## Примечания

Вы не создаете экземпляры этого класса напрямую. Чтобы получить доступ к коллекции строительных блоков, используйте[`BuildingBlocks`](../glossarydocument/buildingblocks/) свойство.

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

* class [NodeCollection](../../aspose.words/nodecollection/)
* пространство имен [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* сборка [Aspose.Words](../../)
