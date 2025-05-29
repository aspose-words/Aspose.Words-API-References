---
title: StructuredDocumentTag Class
linktitle: StructuredDocumentTag
articleTitle: StructuredDocumentTag
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Markup.StructuredDocumentTag для эффективного управления содержимым в документах. Улучшите управление документами с помощью функций SDT!
type: docs
weight: 4750
url: /ru/net/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class

Представляет структурированный тег документа (SDT или элемент управления содержимым) в документе.

Чтобы узнать больше, посетите[Структурированные теги документов или контроль содержимого](https://docs.aspose.com/words/net/working-with-content-control-sdt/) документальная статья.

```csharp
public class StructuredDocumentTag : CompositeNode, IStructuredDocumentTag
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [StructuredDocumentTag](structureddocumenttag/)(*[DocumentBase](../../aspose.words/documentbase/), [SdtType](../sdttype/), [MarkupLevel](../markuplevel/)*) | Инициализирует новый экземпляр**Структурированный тег документа** класс. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Appearance](../../aspose.words.markup/structureddocumenttag/appearance/) { get; set; } | Получает/задает внешний вид структурированного тега документа. |
| [BuildingBlockCategory](../../aspose.words.markup/structureddocumenttag/buildingblockcategory/) { get; set; } | Указывает категорию строительного блока для этого**СДТ** node. Не может быть`нулевой` . |
| [BuildingBlockGallery](../../aspose.words.markup/structureddocumenttag/buildingblockgallery/) { get; set; } | Указывает тип строительного блока для этого**СДТ** . Не может быть`нулевой` . |
| [CalendarType](../../aspose.words.markup/structureddocumenttag/calendartype/) { get; set; } | Указывает тип календаря для этого**СДТ** . По умолчаниюDefault |
| [Checked](../../aspose.words.markup/structureddocumenttag/checked/) { get; set; } | Получает/устанавливает текущее состояние флажка**СДТ** . Значение по умолчанию для этого свойства:`ЛОЖЬ` . |
| [Color](../../aspose.words.markup/structureddocumenttag/color/) { get; set; } | Получает или задает цвет структурированного тега документа. |
| [ContentsFont](../../aspose.words.markup/structureddocumenttag/contentsfont/) { get; } | Форматирование шрифта, которое будет применено к тексту, введенному в**СДТ** . |
| [Count](../../aspose.words/compositenode/count/) { get; } | Получает количество непосредственных потомков этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает пользовательский идентификатор узла. |
| [DateDisplayFormat](../../aspose.words.markup/structureddocumenttag/datedisplayformat/) { get; set; } | Строка, представляющая формат отображения дат. |
| [DateDisplayLocale](../../aspose.words.markup/structureddocumenttag/datedisplaylocale/) { get; set; } | Позволяет установить/получить формат языка для даты, отображаемой в этом**СДТ** . |
| [DateStorageFormat](../../aspose.words.markup/structureddocumenttag/datestorageformat/) { get; set; } | Возвращает/устанавливает формат, в котором хранится дата для SDT при**СДТ** привязан к узлу XML в хранилище данных документа. Значение по умолчанию:DateTime |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, к которому принадлежит этот узел. |
| [EndCharacterFont](../../aspose.words.markup/structureddocumenttag/endcharacterfont/) { get; } | Форматирование шрифта, которое будет применено к последнему символу текста, введенного в**СДТ** . |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Получает первый дочерний элемент узла. |
| [FullDate](../../aspose.words.markup/structureddocumenttag/fulldate/) { get; set; } | Указывает полную дату и время последнего ввода в этот**СДТ** . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Возврат`истинный` если у этого узла есть дочерние узлы. |
| [Id](../../aspose.words.markup/structureddocumenttag/id/) { get; } | Указывает уникальный постоянный числовой идентификатор, доступный только для чтения, для этого**СДТ**. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Возврат`истинный` так как этот узел может иметь дочерние узлы. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttag/isshowingplaceholdertext/) { get; set; } | Указывает, является ли содержимое этого**СДТ** должно интерпретироваться как содержащее заполнитель text (в отличие от обычного текстового содержимого в SDT). |
| [IsTemporary](../../aspose.words.markup/structureddocumenttag/istemporary/) { get; set; } | Указывает, является ли это**СДТ** должны быть удалены из документа WordProcessingML при изменении его содержимого . |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Получает последний дочерний элемент узла. |
| [Level](../../aspose.words.markup/structureddocumenttag/level/) { get; } | Получает уровень, на котором это**СДТ** встречается в дереве документа. |
| [ListItems](../../aspose.words.markup/structureddocumenttag/listitems/) { get; } | Получает[`SdtListItemCollection`](../sdtlistitemcollection/) связанный с этим**СДТ** . |
| [LockContentControl](../../aspose.words.markup/structureddocumenttag/lockcontentcontrol/) { get; set; } | При установке на`истинный` , это свойство запретит пользователю удалять это**СДТ** . |
| [LockContents](../../aspose.words.markup/structureddocumenttag/lockcontents/) { get; set; } | При установке на`истинный` , это свойство запретит пользователю редактировать содержимое этого**СДТ** . |
| [Multiline](../../aspose.words.markup/structureddocumenttag/multiline/) { get; set; } | Указывает, является ли это**СДТ** позволяет вводить несколько строк текста. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за данным узлом. |
| override [NodeType](../../aspose.words.markup/structureddocumenttag/nodetype/) { get; } | ВозвратStructuredDocumentTag . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [Placeholder](../../aspose.words.markup/structureddocumenttag/placeholder/) { get; } | Получает[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) содержащий текст-заполнитель, который должен отображаться, когда содержимое этого запуска SDT пусто, связанный сопоставленный элемент XML пуст, как указано через[`XmlMapping`](./xmlmapping/) element или[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) элемент - это`истинный` . |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttag/placeholdername/) { get; set; } | Получает или задает имя[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) содержащий текст-заполнитель. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий данному узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает[`Range`](../../aspose.words/range/)объект, представляющий часть документа, содержащуюся в этом узле. |
| [SdtType](../../aspose.words.markup/structureddocumenttag/sdttype/) { get; } | Получает тип этого**Структурированный тег документа** . |
| [Style](../../aspose.words.markup/structureddocumenttag/style/) { get; set; } | Возвращает или задает стиль тега структурированного документа. |
| [StyleName](../../aspose.words.markup/structureddocumenttag/stylename/) { get; set; } | Возвращает или задает имя стиля, примененного к структурированному тегу документа. |
| [Tag](../../aspose.words.markup/structureddocumenttag/tag/) { get; set; } | Указывает тег, связанный с текущим узлом SDT. Не может быть`нулевой` . |
| [Title](../../aspose.words.markup/structureddocumenttag/title/) { get; set; } | Указывает понятное имя, связанное с этим**СДТ** . Не может быть`нулевой` . |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttag/wordopenxml/) { get; } | Получает строку, представляющую XML, содержащийся в узле вFlatOpc формат. |
| [WordOpenXMLMinimal](../../aspose.words.markup/structureddocumenttag/wordopenxmlminimal/) { get; } | Получает строку, представляющую XML, содержащийся в узле вFlatOpc формат. В отличие от[`WordOpenXML`](./wordopenxml/) свойство, этот метод генерирует урезанный документ, который исключает любые части, не связанные с содержимым. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttag/xmlmapping/) { get; } | Получает объект, представляющий сопоставление этого структурированного тега документа с XML-данными в пользовательской XML-части текущего документа. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttag/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Принимает посетителя. |
| override [AcceptEnd](../../aspose.words.markup/structureddocumenttag/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Принимает посетителя для посещения конца StructuredDocumentTag. |
| override [AcceptStart](../../aspose.words.markup/structureddocumenttag/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Принимает посетителя для посещения начала StructuredDocumentTag. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Добавляет указанный узел в конец списка дочерних узлов для данного узла. |
| [Clear](../../aspose.words.markup/structureddocumenttag/clear/)() | Очищает содержимое этого структурированного тега документа и отображает заполнитель, если он определен. |
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
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttag/removeselfonly/)() | Удаляет только сам узел SDT, но сохраняет его содержимое внутри дерева документа. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Удаляет все[`SmartTag`](../smarttag/) узлы-потомки текущего узла. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Выбирает список узлов, соответствующих выражению XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Выбирает первый[`Node`](../../aspose.words/node/) что соответствует выражению XPath. |
| [SetCheckedSymbol](../../aspose.words.markup/structureddocumenttag/setcheckedsymbol/)(*int, string*) | Устанавливает символ, используемый для представления отмеченного состояния элемента управления содержимым флажка. |
| [SetUncheckedSymbol](../../aspose.words.markup/structureddocumenttag/setuncheckedsymbol/)(*int, string*) | Устанавливает символ, используемый для представления неотмеченного состояния элемента управления содержимым флажка. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Экспортирует содержимое узла в строку указанного формата. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

## Примечания

Структурированные теги документов (SDT) позволяют встраивать в документ определяемую пользователем семантику, а также поведение и внешний вид its .

В этой версии Aspose.Words предоставляет ряд открытых методов и свойств для управления поведением и содержимым`StructuredDocumentTag` . Сопоставление узлов SDT с пользовательскими пакетами XML в документе можно выполнить с помощью using [`XmlMapping`](./xmlmapping/) свойство.

`StructuredDocumentTag` может встречаться в документе в следующих местах:

* Уровень блока — среди абзацев и таблиц, как дочерний элемент[`Body`](../../aspose.words/body/) ,[`HeaderFooter`](../../aspose.words/headerfooter/) , [`Comment`](../../aspose.words/comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) или[`Shape`](../../aspose.words.drawing/shape/) узел.
* Уровень строки — среди строк в таблице, как дочерний элемент[`Table`](../../aspose.words.tables/table/) узел.
* Уровень ячеек — среди ячеек в строке таблицы, как дочерний элемент[`Row`](../../aspose.words.tables/row/) узел.
* Встроенный уровень - Среди встроенного содержимого внутри, как дочерний элемент[`Paragraph`](../../aspose.words/paragraph/).
* Вложенный внутрь другого`StructuredDocumentTag`.

## Примеры

Показывает, как работать со стилями для элементов управления содержимым.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены два способа применения стиля из документа к структурированному тегу документа.
// 1 — Применить объект стиля из коллекции стилей документа:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Ссылка на стиль в документе по имени:
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Console.WriteLine(sdt.WordOpenXMLMinimal);

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### Смотрите также

* class [CompositeNode](../../aspose.words/compositenode/)
* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* пространство имен [Aspose.Words.Markup](../../aspose.words.markup/)
* сборка [Aspose.Words](../../)
