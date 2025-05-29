---
title: BuildingBlock Class
linktitle: BuildingBlock
articleTitle: BuildingBlock
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.BuildingBlocks.BuildingBlock для создания и управления записями глоссария, такими как AutoText и AutoCorrect, для повышения эффективности работы с документами.
type: docs
weight: 320
url: /ru/net/aspose.words.buildingblocks/buildingblock/
---
## BuildingBlock class

Представляет запись документа глоссария, такую как Building Block, AutoText или AutoCorrect.

Чтобы узнать больше, посетите[Объектная модель документа Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) документальная статья.

```csharp
public class BuildingBlock : CompositeNode
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [BuildingBlock](buildingblock/)(*[GlossaryDocument](../glossarydocument/)*) | Инициализирует новый экземпляр этого класса. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Behavior](../../aspose.words.buildingblocks/buildingblock/behavior/) { get; set; } | Указывает поведение, которое должно применяться при вставке содержимого строительного блока в основной документ. |
| [Category](../../aspose.words.buildingblocks/buildingblock/category/) { get; set; } | Указывает категоризацию второго уровня для строительного блока. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Получает количество непосредственных потомков этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает пользовательский идентификатор узла. |
| [Description](../../aspose.words.buildingblocks/buildingblock/description/) { get; set; } | Получает или задает описание, связанное с этим строительным блоком. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, к которому принадлежит этот узел. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Получает первый дочерний элемент узла. |
| [FirstSection](../../aspose.words.buildingblocks/buildingblock/firstsection/) { get; } | Получает первый раздел в строительном блоке. |
| [Gallery](../../aspose.words.buildingblocks/buildingblock/gallery/) { get; set; } | Указывает категоризацию первого уровня для строительного блока для целей классификации или сортировки пользовательского интерфейса. |
| [Guid](../../aspose.words.buildingblocks/buildingblock/guid/) { get; set; } | Получает или задает идентификатор (128-битный GUID), который уникально идентифицирует этот строительный блок. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Возврат`истинный` если у этого узла есть дочерние узлы. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Возврат`истинный` так как этот узел может иметь дочерние узлы. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Получает последний дочерний элемент узла. |
| [LastSection](../../aspose.words.buildingblocks/buildingblock/lastsection/) { get; } | Получает последний раздел в строительном блоке. |
| [Name](../../aspose.words.buildingblocks/buildingblock/name/) { get; set; } | Получает или задает имя этого строительного блока. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за данным узлом. |
| override [NodeType](../../aspose.words.buildingblocks/buildingblock/nodetype/) { get; } | ВозвращаетBuildingBlock значение. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий данному узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает[`Range`](../../aspose.words/range/)объект, представляющий часть документа, содержащуюся в этом узле. |
| [Sections](../../aspose.words.buildingblocks/buildingblock/sections/) { get; } | Возвращает коллекцию, которая представляет все разделы в строительном блоке. |
| [Type](../../aspose.words.buildingblocks/buildingblock/type/) { get; set; } | Указывает тип строительного блока. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words.buildingblocks/buildingblock/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Принимает посетителя. |
| override [AcceptEnd](../../aspose.words.buildingblocks/buildingblock/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Принимает посетителя для посещения конца BuildingBlock. |
| override [AcceptStart](../../aspose.words.buildingblocks/buildingblock/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Принимает посетителя для посещения начала BuildingBlock. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Добавляет указанный узел в конец списка дочерних узлов для данного узла. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Создает дубликат узла. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Создает навигатор, который можно использовать для перемещения и чтения узлов. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Получает первого предка указанного[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Получает первого предка указанного типа объекта. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Возвращает N-й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Обеспечивает поддержку для каждой итерации стиля по дочерним узлам этого узла. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Получает текст этого узла и всех его дочерних узлов. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | Вставляет указанный узел сразу после указанного ссылочного узла. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | Вставляет указанный узел непосредственно перед указанным ссылочным узлом. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Добавляет указанный узел в начало списка дочерних узлов для данного узла. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя из родителя. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Удаляет указанный дочерний узел. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Удаляет все[`SmartTag`](../../aspose.words.markup/smarttag/) узлы-потомки текущего узла. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Выбирает список узлов, соответствующих выражению XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Выбирает первый[`Node`](../../aspose.words/node/) что соответствует выражению XPath. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Экспортирует содержимое узла в строку указанного формата. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

## Примечания

`BuildingBlock` может содержать только[`Section`](../../aspose.words/section/) узлы.

`BuildingBlock` может быть только ребенком[`GlossaryDocument`](../glossarydocument/).

Вы можете создавать новые строительные блоки и вставлять их в документ глоссария. Вы можете изменять или удалять существующие строительные блоки. Вы можете копировать или перемещать строительные блоки между документами. Вы можете вставлять содержимое строительного блока в документ.

Соответствует**docЧасть** ,**docPartPr** и**docPartBody**элементы в OOXML.

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

* class [CompositeNode](../../aspose.words/compositenode/)
* пространство имен [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* сборка [Aspose.Words](../../)
