---
title: Enum BuildingBlockType
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.BuildingBlocks.BuildingBlockType перечисление. Указывает тип стандартного блока. Тип может повлиять на видимость и поведение стандартного блока в Microsoft Word. .
type: docs
weight: 170
url: /ru/net/aspose.words.buildingblocks/buildingblocktype/
---
## BuildingBlockType enumeration

Указывает тип стандартного блока. Тип может повлиять на видимость и поведение стандартного блока в Microsoft Word. .

```csharp
public enum BuildingBlockType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Для стандартного блока не указана информация о типе. |
| AutomaticallyReplaceNameWithContent | `1` | Позволяет автоматически вставлять стандартный блок в документ всякий раз, когда его имя вводится в приложение. |
| StructuredDocumentTagPlaceholderText | `2` | Строительный блок представляет собой текст-заполнитель тега структурированного документа. |
| FormFieldHelpText | `3` | Строительный блок представляет собой текст справки по полю формы. |
| Normal | `4` | Строительный блок представляет собой обычную (т. е. обычную) запись документа глоссария. |
| AutoCorrect | `5` | Строительный блок связан с инструментами орфографии и грамматики. |
| AutoText | `6` | Строительным блоком является запись автотекста. |
| All | `7` | Строительный блок связан со всеми типами. |
| Default | `0` | Сохранить какNone . |

### Примечания

Соответствует **ST_DocPartType** введите OOXML.

### Примеры

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

* пространство имен [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* сборка [Aspose.Words](../../)


