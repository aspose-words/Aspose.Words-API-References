---
title: BuildingBlock.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words для .NET
description: BuildingBlock Accept метод. Принимает посетителя на С#.
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

Истинно, если были посещены все узлы; ложь, если[`DocumentVisitor`](../../../aspose.words/documentvisitor/) остановил операцию перед посещением всех узлов.

## Примечания

Перечисляет этот узел и все его дочерние элементы. Каждый узел вызывает соответствующий метод[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

Дополнительные сведения см. в шаблоне проектирования «Посетитель».

Звонки[`VisitBuildingBlockStart`](../../../aspose.words/documentvisitor/visitbuildingblockstart/) , затем вызывает [`Accept`](../../../aspose.words/node/accept/) для всех дочерних узлов этого строительного блока, затем вызывает [`VisitBuildingBlockEnd`](../../../aspose.words/documentvisitor/visitbuildingblockend/).

Примечание. Узел стандартного блока и его дочерние элементы не посещаются, когда вы выполняете a Visitor через[`Document`](../../../aspose.words/document/) . Если вы хотите выполнить посетителя поверх строительного блока a , вам необходимо выполнить посетителя поверх[`GlossaryDocument`](../../glossarydocument/) or звонок`Accept` .

## Примеры

Показывает, как добавить в документ пользовательский стандартный блок.

```csharp
public void CreateAndInsert()
{
    // Глоссарий документа. В документе хранятся строительные блоки.
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();
    doc.GlossaryDocument = glossaryDoc;

    // Создайте строительный блок, назовите его, а затем добавьте в документ глоссария.
    BuildingBlock block = new BuildingBlock(glossaryDoc)
    {
        Name = "Custom Block"
    };

    glossaryDoc.AppendChild(block);

    // Все новые GUID строительных блоков по умолчанию имеют одинаковое нулевое значение, и мы можем присвоить им новое уникальное значение.
    Assert.AreEqual("00000000-0000-0000-0000-000000000000", block.Guid.ToString());

    block.Guid = Guid.NewGuid();

    // Следующие свойства классифицируют стандартные блоки
    // в меню, к которому мы можем получить доступ в Microsoft Word через «Вставка» -> «Быстрые детали» -> «Организатор строительных блоков».
    Assert.AreEqual("(Empty Category)", block.Category);
    Assert.AreEqual(BuildingBlockType.None, block.Type);
    Assert.AreEqual(BuildingBlockGallery.All, block.Gallery);
    Assert.AreEqual(BuildingBlockBehavior.Content, block.Behavior);

    // Прежде чем мы сможем добавить этот строительный блок в наш документ, нам нужно будет добавить в него некоторое содержимое,
    // что мы будем делать с помощью посетителя документа. Этот посетитель также установит категорию, галерею и поведение.
    BuildingBlockVisitor visitor = new BuildingBlockVisitor(glossaryDoc);
    block.Accept(visitor);

    // Мы можем получить доступ к только что созданному блоку из документа глоссария.
    BuildingBlock customBlock = glossaryDoc.GetBuildingBlock(BuildingBlockGallery.QuickParts,
        "My custom building blocks", "Custom Block");

    // Сам блок представляет собой раздел, содержащий текст.
    Assert.AreEqual($"Text inside {customBlock.Name}\f", customBlock.FirstSection.Body.FirstParagraph.GetText());
    Assert.AreEqual(customBlock.FirstSection, customBlock.LastSection);
    // Теперь мы можем вставить его в документ как новый раздел.
    doc.AppendChild(doc.ImportNode(customBlock.FirstSection, true));

    // Мы также можем найти его в органайзере строительных блоков Microsoft Word и разместить вручную.
    doc.Save(ArtifactsDir + "BuildingBlocks.CreateAndInsert.dotx");
}

/// <summary>
/// Устанавливает посещенный строительный блок для вставки в документ как быструю часть и добавляет текст к его содержимому.
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
        // Настройте строительный блок как быструю часть и добавьте свойства, используемые Организатором строительных блоков.
        block.Behavior = BuildingBlockBehavior.Paragraph;
        block.Category = "My custom building blocks";
        block.Description =
            "Using this block in the Quick Parts section of word will place its contents at the cursor.";
        block.Gallery = BuildingBlockGallery.QuickParts;

        // Добавляем раздел с текстом.
        // Вставка блока в документ добавит этот раздел с его дочерними узлами в указанном месте.
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

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [BuildingBlock](../)
* пространство имен [Aspose.Words.BuildingBlocks](../../../aspose.words.buildingblocks/)
* сборка [Aspose.Words](../../../)
