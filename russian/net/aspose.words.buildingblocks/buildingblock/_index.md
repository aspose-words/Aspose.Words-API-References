---
title: Class BuildingBlock
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.BuildingBlocks.BuildingBlock сорт. Представляет запись документа глоссария такую как стандартный блок автотекст или запись автозамены.
type: docs
weight: 120
url: /ru/net/aspose.words.buildingblocks/buildingblock/
---
## BuildingBlock class

Представляет запись документа глоссария, такую как стандартный блок, автотекст или запись автозамены.

```csharp
public class BuildingBlock : CompositeNode
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [BuildingBlock](buildingblock/)(GlossaryDocument) | Инициализирует новый экземпляр этого класса. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Behavior](../../aspose.words.buildingblocks/buildingblock/behavior/) { get; set; } | Определяет поведение, которое должно применяться, когда содержимое стандартного блока вставляется в основной документ. |
| [Category](../../aspose.words.buildingblocks/buildingblock/category/) { get; set; } | Задает категоризацию второго уровня для стандартного блока. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Получает все непосредственные дочерние узлы этого узла. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Получает количество непосредственных дочерних элементов этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает идентификатор пользовательского узла. |
| [Description](../../aspose.words.buildingblocks/buildingblock/description/) { get; set; } | Получает или задает описание, связанное с этим стандартным блоком. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, которому принадлежит этот узел. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Получает первого потомка узла. |
| [FirstSection](../../aspose.words.buildingblocks/buildingblock/firstsection/) { get; } | Получает первый раздел в стандартном блоке. |
| [Gallery](../../aspose.words.buildingblocks/buildingblock/gallery/) { get; set; } | Задает категоризацию первого уровня для стандартного блока в целях классификации или сортировки пользовательского интерфейса. |
| [Guid](../../aspose.words.buildingblocks/buildingblock/guid/) { get; set; } | Получает или задает идентификатор (128-битный GUID), однозначно идентифицирующий этот строительный блок. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Возвращает true, если у этого узла есть дочерние узлы. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Возвращает true, так как этот узел может иметь дочерние узлы. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Получает последний дочерний элемент узла. |
| [LastSection](../../aspose.words.buildingblocks/buildingblock/lastsection/) { get; } | Получает последний раздел в строительном блоке. |
| [Name](../../aspose.words.buildingblocks/buildingblock/name/) { get; set; } | Получает или задает имя этого стандартного блока. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за этим узлом. |
| override [NodeType](../../aspose.words.buildingblocks/buildingblock/nodetype/) { get; } | ВозвращаетBuildingBlock значение. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает **Диапазон** объект, представляющий часть документа, содержащегося в этом узле. |
| [Sections](../../aspose.words.buildingblocks/buildingblock/sections/) { get; } | Возвращает коллекцию, представляющую все разделы в стандартном блоке. |
| [Type](../../aspose.words.buildingblocks/buildingblock/type/) { get; set; } | Указывает тип стандартного блока. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words.buildingblocks/buildingblock/accept/)(DocumentVisitor) | Принимает посетителя. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Добавляет указанный узел в конец списка дочерних узлов для этого узла. |
| [Clone](../../aspose.words/node/clone/)(bool) | Создает дубликат узла. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Зарезервировано для системного использования. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Получает первого предка указанного[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Получает первого предка указанного типа объекта. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Возвращает N-й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Возвращает динамическую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Обеспечивает поддержку для каждой итерации стиля над дочерними узлами этого узла. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Получает текст этого узла и всех его дочерних элементов. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Вставляет указанный узел сразу после указанного ссылочного узла. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Вставляет указанный узел непосредственно перед указанным ссылочным узлом. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Добавляет указанный узел в начало списка дочерних узлов для этого узла. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя из родителя. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Удаляет указанный дочерний узел. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Удаляет все[`SmartTag`](../../aspose.words.markup/smarttag/) узлы-потомки текущего узла. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Выбирает список узлов, соответствующих выражению XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Выбирает первый узел, соответствующий выражению XPath. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

### Примечания

`BuildingBlock` может содержать только[`Section`](../../aspose.words/section/) узлы.

`BuildingBlock` может быть только ребенком[`GlossaryDocument`](../glossarydocument/).

Вы можете создавать новые стандартные блоки и вставлять их в глоссарий. Вы можете изменять или удалять существующие стандартные блоки. Вы можете копировать или перемещать стандартные блоки между документами. Вы можете вставить содержимое стандартного блока в документ.

Соответствует **docPart** , **docPartPr** а также **docPartBody**элементы в OOXML.

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

* class [CompositeNode](../../aspose.words/compositenode/)
* пространство имен [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* сборка [Aspose.Words](../../)


