---
title: StructuredDocumentTag
second_title: Справочник по API Aspose.Words для .NET
description: Представляет тег структурированного документа SDT или элемент управления содержимым в документе.
type: docs
weight: 3770
url: /ru/net/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class

Представляет тег структурированного документа (SDT или элемент управления содержимым) в документе.

```csharp
public class StructuredDocumentTag : CompositeNode, IStructuredDocumentTag
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [StructuredDocumentTag](structureddocumenttag)(DocumentBase, SdtType, MarkupLevel) | Инициализирует новый экземпляр тега структурированного документа класса. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Appearance](../../aspose.words.markup/structureddocumenttag/appearance) { get; set; } | Получает/задает внешний вид тега структурированного документа. |
| [BuildingBlockCategory](../../aspose.words.markup/structureddocumenttag/buildingblockcategory) { get; set; } | Указывает категорию стандартного блока для этого узла **SDT** . Не может быть нулевым. |
| [BuildingBlockGallery](../../aspose.words.markup/structureddocumenttag/buildingblockgallery) { get; set; } | Указывает тип строительного блока для этого **SDT** . Не может быть нулевым. |
| [CalendarType](../../aspose.words.markup/structureddocumenttag/calendartype) { get; set; } | Указывает тип календаря для этого **SDT** . По умолчанию:Default |
| [Checked](../../aspose.words.markup/structureddocumenttag/checked) { get; set; } | Получает/устанавливает текущее состояние флажка **SDT** . Значение по умолчанию для этого свойства — false. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Получает все непосредственные дочерние узлы данного узла. |
| [Color](../../aspose.words.markup/structureddocumenttag/color) { get; set; } | Получает или задает цвет тега структурированного документа. |
| [ContentsFont](../../aspose.words.markup/structureddocumenttag/contentsfont) { get; } | Форматирование шрифта, которое будет применяться к тексту, введенному в **SDT** . |
| [Count](../../aspose.words/compositenode/count) { get; } | Получает количество непосредственных потомков этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Указывает идентификатор пользовательского узла. |
| [DateDisplayFormat](../../aspose.words.markup/structureddocumenttag/datedisplayformat) { get; set; } | Строка, представляющая формат, в котором отображаются даты. Не может быть нулевым.  Даты для английского языка (США):"мм/дд/гггг" |
| [DateDisplayLocale](../../aspose.words.markup/structureddocumenttag/datedisplaylocale) { get; set; } | Позволяет установить/получить языковой формат для даты, отображаемой в этом **SDT** . |
| [DateStorageFormat](../../aspose.words.markup/structureddocumenttag/datestorageformat) { get; set; } | Получает/задает формат, в котором дата для SDT даты хранится, когда привязывается **SDT** в узел XML в хранилище данных документа. Значение по умолчанию:DateTime |
| virtual [Document](../../aspose.words/node/document) { get; } | Получает документ, которому принадлежит данный узел. |
| [EndCharacterFont](../../aspose.words.markup/structureddocumenttag/endcharacterfont) { get; } | Форматирование шрифта, которое будет применено к последнему символу текста, введенного в **SDT** . |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Получает первый потомок узла. |
| [FullDate](../../aspose.words.markup/structureddocumenttag/fulldate) { get; set; } | Указывает полную дату и время, введенные в последний раз в этом **SDT** . |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Возвращает true, если у этого узла есть дочерние узлы. |
| [Id](../../aspose.words.markup/structureddocumenttag/id) { get; } | Указывает уникальный постоянный числовой идентификатор только для чтения для этого **SDT** . |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Возвращает true, так как этот узел может иметь дочерние узлы. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttag/isshowingplaceholdertext) { get; set; } | Указывает, должно ли содержимое этого **SDT** интерпретироваться как содержать замещающий текст (в отличие от обычного текстового содержимого в SDT). |
| [IsTemporary](../../aspose.words.markup/structureddocumenttag/istemporary) { get; set; } | Указывает, будет ли этот **SDT** удаляться из документа WordProcessingML, когда его содержимое изменены. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Получает последний потомок узла. |
| [Level](../../aspose.words.markup/structureddocumenttag/level) { get; } | Получает уровень, на котором это **SDT** встречается в дереве документа. |
| [ListItems](../../aspose.words.markup/structureddocumenttag/listitems) { get; } | Получает[`SdtListItemCollection`](../sdtlistitemcollection)связанный с этим **SDT** . |
| [LockContentControl](../../aspose.words.markup/structureddocumenttag/lockcontentcontrol) { get; set; } | Если установлено значение true, это свойство запрещает пользователю удалять это **SDT** . |
| [LockContents](../../aspose.words.markup/structureddocumenttag/lockcontents) { get; set; } | Если установлено значение true, это свойство запрещает пользователю редактировать содержимое этого **SDT** . |
| [Multiline](../../aspose.words.markup/structureddocumenttag/multiline) { get; set; } | Указывает, допускает ли это **SDT** несколько строк текста. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Получает узел, следующий сразу за этим узлом. |
| override [NodeType](../../aspose.words.markup/structureddocumenttag/nodetype) { get; } | Возвращает **NodeType.StructuredDocumentTag** . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Получает непосредственного родителя этого узла. |
| [Placeholder](../../aspose.words.markup/structureddocumenttag/placeholder) { get; } | Получает[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock)содержащий текст-заполнитель, который должен отображаться, когда содержимое этого запуска SDT пусто ассоциированный отображаемый XML-элемент пуст, как указано с помощью[`XmlMapping`](./xmlmapping)element или:::R5 Элемент:P:Aspose.Words.Markup.StructuredDocumentTag.IsShowingPlaceholderText:::имеет значение true. |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttag/placeholdername) { get; set; } | Получает или задает имя элемента[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock), содержащего замещающий текст. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [Range](../../aspose.words/node/range) { get; } | Возвращает объект **Range** , представляющий часть документа, содержащуюся в этом узле. |
| [SdtType](../../aspose.words.markup/structureddocumenttag/sdttype) { get; } | Получает тип этого **Тег структурированного документа** . |
| [Style](../../aspose.words.markup/structureddocumenttag/style) { get; set; } | Получает или задает стиль тега структурированного документа. |
| [StyleName](../../aspose.words.markup/structureddocumenttag/stylename) { get; set; } | Получает или задает имя стиля, примененного к тегу структурированного документа. |
| [Tag](../../aspose.words.markup/structureddocumenttag/tag) { get; set; } | Задает тег, связанный с текущим узлом SDT. Не может быть нулевым. |
| [Title](../../aspose.words.markup/structureddocumenttag/title) { get; set; } | Указывает понятное имя, связанное с этим **SDT** . Не может быть нулевым. |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttag/wordopenxml) { get; } | Получает строку, представляющую XML, содержащийся в узле, в форматеFlatOpc. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttag/xmlmapping) { get; } | Получает объект, представляющий сопоставление этого тега структурированного документа с данными XML в пользовательской части XML текущего документа. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttag/accept)(DocumentVisitor) | Принимает посетителя. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Добавляет указанный узел в конец списка дочерних узлов для этого узла. |
| [Clear](../../aspose.words.markup/structureddocumenttag/clear)() | Очищает содержимое этого тега структурированного документа и отображает заполнитель, если он определен. |
| [Clone](../../aspose.words/node/clone)(bool) | Создает дубликат узла. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Зарезервировано для системного использования. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Получает первого предка указанного[`NodeType`](../../aspose.words/nodetype). |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Получает первого предка указанного типа объекта. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Возвращает N-й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Возвращает динамическую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Обеспечивает поддержку для каждой итерации стиля над дочерними узлами этого узла. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Получает текст этого узла и всех его потомков. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Вставляет указанный узел сразу после указанного опорного узла. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Вставляет указанный узел непосредственно перед указанным ссылочным узлом. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Добавляет указанный узел в начало списка дочерних узлов для этого узла. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [Remove](../../aspose.words/node/remove)() | Удаляет себя из родителя. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Удаляет указанный дочерний узел. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttag/removeselfonly)() | Удаляет только сам этот узел SDT, но сохраняет его содержимое внутри дерева документа. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Удаляет все[`SmartTag`](../smarttag)узлы-потомки текущего узла. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Выбирает список узлов, соответствующих выражению XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Выбирает первый узел, соответствующий выражению XPath. |
| [SetCheckedSymbol](../../aspose.words.markup/structureddocumenttag/setcheckedsymbol)(int, string) | Устанавливает символ, используемый для представления отмеченного состояния элемента управления содержимым флажка. |
| [SetUncheckedSymbol](../../aspose.words.markup/structureddocumenttag/setuncheckedsymbol)(int, string) | Устанавливает символ, используемый для представления неотмеченного состояния элемента управления содержимым флажка. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

### Примечания

Теги структурированных документов (SDT) позволяют встраивать определяемую пользователем семантику, а также ее поведение и внешний вид в документе.

В этой версии Aspose.Words предоставляет ряд общедоступных методов и свойств для управления поведением и содержимым[`StructuredDocumentTag`](../structureddocumenttag). Сопоставление узлов SDT с пользовательскими пакетами XML в документе можно выполнить с помощью [`XmlMapping`](./xmlmapping)имущество.

[`StructuredDocumentTag`](../structureddocumenttag)может встречаться в документе в следующих местах:

* Уровень блока - среди абзацев и таблиц, как дочерний элемент[`Body`](../../aspose.words/body),[`HeaderFooter`](../../aspose.words/headerfooter), [`Comment`](../../aspose.words/comment),[`Footnote`](../../aspose.words.notes/footnote)или узел[`Shape`](../../aspose.words.drawing/shape).
* Уровень строки - Среди строк в таблице, как дочерний элемент узла[`Table`](../../aspose.words.tables/table).
* Уровень ячейки - Среди ячеек в строке таблицы, как дочерний узел[`Row`](../../aspose.words.tables/row).
* Встроенный уровень — среди встроенного содержимого внутри, как дочерний элемент[`Paragraph`](../../aspose.words/paragraph).
* Вложен в другой[`StructuredDocumentTag`](../structureddocumenttag).

### Примеры

Показывает, как работать со стилями для элементов управления содержимым.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены два способа применения стиля из документа к тегу структурированного документа.
// 1 - Применить объект стиля из коллекции стилей документа:
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

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

### Смотрите также

* class [CompositeNode](../../aspose.words/compositenode)
* interface [IStructuredDocumentTag](../istructureddocumenttag)
* namespace [Aspose.Words.Markup](../../aspose.words.markup)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
