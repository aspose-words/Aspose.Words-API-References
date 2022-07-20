---
title: BuildingBlockBehavior
second_title: Справочник по API Aspose.Words для .NET
description: Определяет поведение которое должно применяться к содержимому стандартного блока при его вставке в основной документ.
type: docs
weight: 130
url: /ru/net/aspose.words.buildingblocks/buildingblockbehavior/
---
## BuildingBlockBehavior enumeration

Определяет поведение, которое должно применяться к содержимому стандартного блока при его вставке в основной документ.

```csharp
public enum BuildingBlockBehavior
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Content | `0` | Указывает, что стандартный блок должен быть вставлен как встроенное содержимое. |
| Paragraph | `1` | Указывает, что стандартный блок должен быть вставлен в отдельный абзац. |
| Page | `2` | Указывает, что стандартный блок должен быть добавлен на собственную страницу. |
| Default | `0` | То же, что иContent . |

### Примечания

Соответствует **ST_DocPartBehavior** введите OOXML.

### Примеры

Показывает, как добавить пользовательский стандартный блок в документ.

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

    // Мы можем получить доступ к только что созданному блоку из глоссария.
    BuildingBlock customBlock = glossaryDoc.GetBuildingBlock(BuildingBlockGallery.QuickParts,
        "My custom building blocks", "Custom Block");

    // Сам блок представляет собой раздел, содержащий текст.
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
        // Настройте стандартный блок как быструю часть и добавьте свойства, используемые Организатором стандартных блоков.
        block.Behavior = BuildingBlockBehavior.Paragraph;
        block.Category = "My custom building blocks";
        block.Description =
            "Using this block in the Quick Parts section of word will place its contents at the cursor.";
        block.Gallery = BuildingBlockGallery.QuickParts;

        // Добавляем раздел с текстом.
        // Вставка блока в документ добавит этот раздел с его дочерними узлами в этом месте.
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

* пространство имен [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
