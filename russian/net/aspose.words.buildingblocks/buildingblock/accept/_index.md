---
title: Accept
second_title: Справочник по API Aspose.Words для .NET
description: Принимает посетителя.
type: docs
weight: 130
url: /ru/net/aspose.words.buildingblocks/buildingblock/accept/
---
## BuildingBlock.Accept method

Принимает посетителя.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| visitor | DocumentVisitor | Посетитель, который посетит узлы. |

### Возвращаемое значение

Истинно, если были посещены все узлы; false, если DocumentVisitor остановил операцию перед посещением всех узлов.

### Примечания

Перечисляет этот узел и все его дочерние элементы. Каждый узел вызывает соответствующий метод в DocumentVisitor.

Для получения дополнительной информации см. шаблон проектирования Посетитель.

Вызовы[`VisitBuildingBlockStart`](../../../aspose.words/documentvisitor/visitbuildingblockstart), затем вызывает [`Accept`](../../../aspose.words/node/accept)для всех дочерних узлов этого строительного блока, затем вызывает [`VisitBuildingBlockEnd`](../../../aspose.words/documentvisitor/visitbuildingblockend).

Примечание. Узел стандартного блока и его дочерние элементы не посещено, когда вы выполняете Посетитель поверх[`Document`](../../../aspose.words/document). Если вы хотите выполнить посетителя над строительным блоком , вам нужно выполнить посетителя над[`GlossaryDocument`](../../glossarydocument)или call`Accept`.

### Примеры

Показывает, как добавить в документ пользовательский стандартный блок.

```csharp
public void CreateAndInsert()
{
     // Глоссарий документа хранит строительные блоки.
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();
    doc.GlossaryDocument = glossaryDoc;

     // Создайте стандартный блок, назовите его, а затем добавьте в глоссарий.
    BuildingBlock block = new BuildingBlock(glossaryDoc)
    {
        Name = "Custom Block"
    };

    glossaryDoc.AppendChild(block);

     // Все новые GUID строительных блоков по умолчанию имеют одно и то же нулевое значение, и мы можем присвоить им новое уникальное значение.
    Assert.AreEqual("00000000-0000-0000-0000-000000000000", block.Guid.ToString());

    block.Guid = Guid.NewGuid();

     // Следующие свойства классифицируют строительные блоки
     // в меню мы можем получить доступ в Microsoft Word через «Вставить» -> "Быстрые детали" -> «Организатор строительных блоков».
    Assert.AreEqual("(Empty Category)", block.Category);
    Assert.AreEqual(BuildingBlockType.None, block.Type);
    Assert.AreEqual(BuildingBlockGallery.All, block.Gallery);
    Assert.AreEqual(BuildingBlockBehavior.Content, block.Behavior);

     // Прежде чем мы сможем добавить этот строительный блок в наш документ, нам нужно дать ему некоторое содержимое, 
     // что мы и сделаем с помощью посетителя документа. Этот посетитель также установит категорию, галерею и поведение.
    BuildingBlockVisitor visitor = new BuildingBlockVisitor(glossaryDoc);
    block.Accept(visitor);

    // Мы можем получить доступ к только что созданному блоку из глоссария document.
    BuildingBlock customBlock = glossaryDoc.GetBuildingBlock(BuildingBlockGallery.QuickParts,
        "My custom building blocks", "Custom Block");

     // Сам блок представляет собой секцию, содержащую текст.
    Assert.AreEqual($"Text inside {customBlock.Name}\f", customBlock.FirstSection.Body.FirstParagraph.GetText());
    Assert.AreEqual(customBlock.FirstSection, customBlock.LastSection);

     // Теперь мы можем вставить его в документ как новый раздел.
    doc.AppendChild(doc.ImportNode(customBlock.FirstSection, true));

     // Мы также можем найти его в Организаторе строительных блоков Microsoft Word и разместить вручную.
    doc.Save(ArtifactsDir + "BuildingBlocks.CreateAndInsert.dotx");
}

/// <summary>
 /// Настраивает посещенный стандартный блок для вставки в документ в качестве быстрой части и добавляет текст к его содержимому.
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
         // Настройте стандартный блок как быструю часть и добавьте свойства, используемые Организатором строительных блоков.
        block.Behavior = BuildingBlockBehavior.Paragraph;
        block.Category = "My custom building blocks";
        block.Description =
            "Using this block in the Quick Parts section of word will place its contents at the cursor.";
        block.Gallery = BuildingBlockGallery.QuickParts;

         // Добавляем раздел с текстом.
         // Вставка блока в документ добавит этот раздел с его дочерними узлами в местоположении.
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

### Смотрите также

* class [DocumentVisitor](../../../aspose.words/documentvisitor)
* class [BuildingBlock](../../buildingblock)
* пространство имен [Aspose.Words.BuildingBlocks](../../buildingblock)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
