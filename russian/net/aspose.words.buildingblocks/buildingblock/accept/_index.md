---
title: BuildingBlock.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words для .NET
description: Откройте для себя метод Accept от BuildingBlock, чтобы беспрепятственно вовлекать посетителей и улучшать пользовательский опыт. Раскройте весь потенциал вашего веб-сайта сегодня!
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

True, если все узлы были посещены; false, если[`DocumentVisitor`](../../../aspose.words/documentvisitor/) остановил операцию до посещения всех узлов.

## Примечания

Перечисляет этот узел и всех его потомков. Каждый узел вызывает соответствующий метод на[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

Более подробную информацию см. в шаблоне проектирования «Посетитель».

Звонки[`VisitBuildingBlockStart`](../../../aspose.words/documentvisitor/visitbuildingblockstart/) , затем вызывает [`Accept`](../../../aspose.words/node/accept/) для всех дочерних узлов этого строительного блока, затем вызывает [`VisitBuildingBlockEnd`](../../../aspose.words/documentvisitor/visitbuildingblockend/).

Примечание: узел строительного блока и его дочерние элементы не посещаются при выполнении посетителя a над[`Document`](../../../aspose.words/document/) . Если вы хотите выполнить Посетителя над строительным блоком a , вам нужно выполнить Посетителя над[`GlossaryDocument`](../../glossarydocument/) или вызов`Accept` .

## Примеры

Показывает, как добавить в документ пользовательский строительный блок.

```csharp
public void CreateAndInsert()
{
    // Документ глоссария документа хранит строительные блоки.
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();
    doc.GlossaryDocument = glossaryDoc;

    // Создайте строительный блок, дайте ему имя, а затем добавьте его в документ глоссария.
    BuildingBlock block = new BuildingBlock(glossaryDoc)
    {
        Name = "Custom Block"
    };

    glossaryDoc.AppendChild(block);

    // Все новые GUID-ы строительных блоков по умолчанию имеют одинаковое нулевое значение, и мы можем присвоить им новое уникальное значение.
    Assert.AreEqual("00000000-0000-0000-0000-000000000000", block.Guid.ToString());

    block.Guid = Guid.NewGuid();

    // Следующие свойства классифицируют строительные блоки
    // в меню Microsoft Word мы можем получить доступ через «Вставка» -> «Быстрые элементы» -> «Организатор строительных блоков».
    Assert.AreEqual("(Empty Category)", block.Category);
    Assert.AreEqual(BuildingBlockType.None, block.Type);
    Assert.AreEqual(BuildingBlockGallery.All, block.Gallery);
    Assert.AreEqual(BuildingBlockBehavior.Content, block.Behavior);

    // Прежде чем мы сможем добавить этот строительный блок в наш документ, нам нужно будет придать ему некоторое содержимое,
    // что мы сделаем с помощью посетителя документа. Этот посетитель также установит категорию, галерею и поведение.
    BuildingBlockVisitor visitor = new BuildingBlockVisitor(glossaryDoc);
    // Перейти к началу/концу BuildingBlock.
    block.Accept(visitor);

    // Мы можем получить доступ к блоку, который мы только что создали из документа глоссария.
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
/// Настраивает посещенный строительный блок для вставки в документ в качестве быстрой части и добавляет текст к его содержимому.
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

        // Добавить раздел с текстом.
        // Вставка блока в документ добавит этот раздел с его дочерними узлами в указанное место.
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
