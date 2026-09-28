---
title: "Класс Aspose::Words::Markup::StructuredDocumentTag"
linktitle: "StructuredDocumentTag"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Markup::StructuredDocumentTag. Представляет структурированный тег документа (SDT или элемент управления содержимым) в документе. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words.markup/structureddocumenttag/
---
## StructuredDocumentTag class


Представляет структурный тег документа (SDT или элемент управления содержимым) в документе. Чтобы узнать больше, посетите статью документации [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class StructuredDocumentTag : public Aspose::Words::CompositeNode,
                              public Aspose::Words::Markup::IMarkupNode,
                              public Aspose::Words::Revisions::ITrackableNode,
                              public Aspose::Words::IRunAttrSource,
                              public Aspose::Words::Markup::IStructuredDocumentTag
```

## Методы

| Метод | Описание |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя для посещения конца [StructuredDocumentTag](./). |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя для посещения начала [StructuredDocumentTag](./). |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clear](./clear/)() | Очищает содержимое этого структурированного тега документа и отображает заполнитель, если он определён. |
| [Clone](../../aspose.words/node/clone/)(bool) | Создаёт дубликат узла. |
| [get_Appearance](./get_appearance/)() override | Получает/устанавливает внешний вид структурированного тега документа. |
| [get_BuildingBlockCategory](./get_buildingblockcategory/)() | Указывает категорию строительного блока для этого узла **SDT**. Не может быть **null**. |
| [get_BuildingBlockGallery](./get_buildingblockgallery/)() | Указывает тип строительного блока для этого **SDT**. Не может быть **null**. |
| [get_CalendarType](./get_calendartype/)() | Указывает тип календаря для этого **SDT**. По умолчанию — [Default](../sdtcalendartype/) |
| [get_Checked](./get_checked/)() | Получает/устанавливает текущее состояние флажка **SDT**. Значение по умолчанию для этого свойства — **false**. |
| [get_Color](./get_color/)() override | Получает или задает цвет структурированного тега документа. |
| [get_ContentsFont](./get_contentsfont/)() | [Font](../../aspose.words/font/) форматирование, которое будет применено к тексту, введённому в **SDT**. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Возвращает количество непосредственных дочерних элементов этого узла. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Указывает пользовательский идентификатор узла. |
| [get_DateDisplayFormat](./get_datedisplayformat/)() | Строка, представляющая формат, в котором отображаются даты. |
| [get_DateDisplayLocale](./get_datedisplaylocale/)() | Позволяет установить/получить языковой формат даты, отображаемой в этом **SDT**. |
| [get_DateStorageFormat](./get_datestorageformat/)() | Получает/устанавливает формат, в котором дата для датового **SDT** хранится, когда **SDT** привязан к узлу XML в хранилище данных документа. Значение по умолчанию — [DateTime](../sdtdatestorageformat/) |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Возвращает документ, к которому принадлежит этот узел. |
| [get_EndCharacterFont](./get_endcharacterfont/)() | [Font](../../aspose.words/font/) форматирование, которое будет применено к последнему символу текста, введённому в **SDT**. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Возвращает первого дочернего узла. |
| [get_FullDate](./get_fulldate/)() | Указывает полную дату и время, последним введённые в этот **SDT**. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Возвращает **true**, если у этого узла есть дочерние узлы. |
| [get_Id](./get_id/)() override | Указывает уникальный только для чтения постоянный числовой идентификатор для этого **SDT**. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Возвращает **true**, поскольку этот узел может иметь дочерние узлы. |
| [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() override | Указывает, следует ли интерпретировать содержимое этого **SDT** как содержащие текст-заполнитель (в отличие от обычного текста внутри **SDT**). Если установлено в **true**, это состояние будет восстановлено (показ текста-заполнителя) при открытии документа. |
| [get_IsTemporary](./get_istemporary/)() const | Указывает, следует ли удалять этот **SDT** из документа WordProcessingML при изменении его содержимого. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Возвращает последнего дочернего узла. |
| [get_Level](./get_level/)() const override | Получает уровень, на котором этот **SDT** находится в дереве документа. |
| [get_ListItems](./get_listitems/)() | Получает [SdtListItemCollection](../sdtlistitemcollection/), связанный с этим **SDT**. |
| [get_LockContentControl](./get_lockcontentcontrol/)() override | Если установлено в **true**, это свойство запретит пользователю удалять этот **SDT**. |
| [get_LockContents](./get_lockcontents/)() override | Если установлено в **true**, это свойство запретит пользователю редактировать содержимое этого **SDT**. |
| [get_Multiline](./get_multiline/)() | Указывает, позволяет ли этот **SDT** несколько строк текста. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Возвращает узел, непосредственно следующий за этим узлом. |
| [get_NodeType](./get_nodetype/)() const override | Возвращает [StructuredDocumentTag](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Возвращает непосредственного родителя этого узла. |
| [get_Placeholder](./get_placeholder/)() override | Получает [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/), содержащий текст-заполнитель, который должен отображаться, когда содержимое выполнения этого SDT пусто, соответствующий сопоставленный элемент XML пуст, как указано через элемент [XmlMapping](./get_xmlmapping/), или элемент [IsShowingPlaceholderText](./get_isshowingplaceholdertext/) имеет значение **true**. |
| [get_PlaceholderName](./get_placeholdername/)() override | Получает или задает имя [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/), содержащего текст-заполнитель. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Возвращает узел, непосредственно предшествующий этому узлу. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Возвращает объект [Range](../../aspose.words/range/), представляющий часть документа, содержащуюся в этом узле. |
| [get_SdtType](./get_sdttype/)() override | Получает тип этого **Structured document tag**. |
| [get_Style](./get_style/)() | Получает или задает [Style](../../aspose.words/style/) структурного тега документа. |
| [get_StyleName](./get_stylename/)() | Получает или задает имя стиля, применяемого к структурному тегу документа. |
| [get_Tag](./get_tag/)() const override | Указывает тег, связанный с текущим узлом SDT. Не может быть **null**. |
| [get_Title](./get_title/)() const override | Указывает удобочитаемое имя, связанное с этим **SDT**. Не может быть **null**. |
| [get_WordOpenXML](./get_wordopenxml/)() override | Получает строку, представляющую XML, содержащийся в узле, в формате [FlatOpc](../../aspose.words/saveformat/). |
| [get_WordOpenXMLMinimal](./get_wordopenxmlminimal/)() | Получает строку, представляющую XML, содержащийся в узле в формате [FlatOpc](../../aspose.words/saveformat/). В отличие от свойства [WordOpenXML](./get_wordopenxml/), этот метод генерирует упрощённый документ, исключающий любые части, не связанные с содержимым. |
| [get_XmlMapping](./get_xmlmapping/)() override | Получает объект, представляющий сопоставление этого структурированного тега документа с XML-данными в пользовательской части XML текущего документа. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Возвращает первого предка указанного [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Возвращает N‑й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) override | Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Обеспечивает поддержку итерации в стиле foreach по дочерним узлам этого узла. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Получает текст этого узла и всех его дочерних узлов. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает следующий узел согласно алгоритму обхода дерева в порядке предобхода. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Вспомогательный метод, преобразующий значение перечисления типа узла в удобочитаемую строку. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает предыдущий узел согласно алгоритму обхода дерева в порядке предобхода. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя из родительского узла. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSelfOnly](./removeselfonly/)() override | Удаляет только этот узел SDT, но сохраняет его содержимое в дереве документа. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Удаляет все дочерние узлы [SmartTag](../smarttag/) текущего узла. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Выбирает список узлов, соответствующих XPath-выражению. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Выбирает первый [Node](../../aspose.words/node/), соответствующий XPath-выражению. |
| [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) override | Сеттер для [Aspose::Words::Markup::StructuredDocumentTag::get_Appearance](./get_appearance/). |
| [set_BuildingBlockCategory](./set_buildingblockcategory/)(const System::String\&) | Сеттер для [Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockCategory](./get_buildingblockcategory/). |
| [set_BuildingBlockGallery](./set_buildingblockgallery/)(const System::String\&) | Сеттер для [Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery](./get_buildingblockgallery/). |
| [set_CalendarType](./set_calendartype/)(Aspose::Words::Markup::SdtCalendarType) | Сеттер для [Aspose::Words::Markup::StructuredDocumentTag::get_CalendarType](./get_calendartype/). |
| [set_Checked](./set_checked/)(bool) | Сеттер для [Aspose::Words::Markup::StructuredDocumentTag::get_Checked](./get_checked/). |
| [set_Color](./set_color/)(System::Drawing::Color) override | Сеттер для [Aspose::Words::Markup::StructuredDocumentTag::get_Color](./get_color/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Сеттер для [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_DateDisplayFormat](./set_datedisplayformat/)(const System::String\&) | Сеттер для [Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayFormat](./get_datedisplayformat/). |
| [set_DateDisplayLocale](./set_datedisplaylocale/)(int32_t) | Сеттер для [Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayLocale](./get_datedisplaylocale/). |
| [set_DateStorageFormat](./set_datestorageformat/)(Aspose::Words::Markup::SdtDateStorageFormat) | Сеттер для [Aspose::Words::Markup::StructuredDocumentTag::get_DateStorageFormat](./get_datestorageformat/). |
| [set_FullDate](./set_fulldate/)(System::DateTime) | Сеттер для [Aspose::Words::Markup::StructuredDocumentTag::get_FullDate](./get_fulldate/). |
| [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) override | Сеттер для [Aspose::Words::Markup::StructuredDocumentTag::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/). |
| [set_IsTemporary](./set_istemporary/)(bool) | Сеттер для [Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary](./get_istemporary/). |
| [set_LockContentControl](./set_lockcontentcontrol/)(bool) override | Сеттер для [Aspose::Words::Markup::StructuredDocumentTag::get_LockContentControl](./get_lockcontentcontrol/). |
| [set_LockContents](./set_lockcontents/)(bool) override | Сеттер для [Aspose::Words::Markup::StructuredDocumentTag::get_LockContents](./get_lockcontents/). |
| [set_Multiline](./set_multiline/)(bool) | Сеттер для [Aspose::Words::Markup::StructuredDocumentTag::get_Multiline](./get_multiline/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PlaceholderName](./set_placeholdername/)(System::String) override | Сеттер для [Aspose::Words::Markup::StructuredDocumentTag::get_PlaceholderName](./get_placeholdername/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Сеттер для [Aspose::Words::Markup::StructuredDocumentTag::get_Style](./get_style/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | Сеттер для [Aspose::Words::Markup::StructuredDocumentTag::get_StyleName](./get_stylename/). |
| [set_Tag](./set_tag/)(System::String) override | Сеттер для [Aspose::Words::Markup::StructuredDocumentTag::get_Tag](./get_tag/). |
| [set_Title](./set_title/)(System::String) override | Сеттер для [Aspose::Words::Markup::StructuredDocumentTag::get_Title](./get_title/). |
| [SetCheckedSymbol](./setcheckedsymbol/)(int32_t, const System::String\&) | Устанавливает символ, используемый для представления отмеченного состояния элемента управления checkbox. |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [SetUncheckedSymbol](./setuncheckedsymbol/)(int32_t, const System::String\&) | Устанавливает символ, используемый для представления неотмеченного состояния элемента управления checkbox. |
| [StructuredDocumentTag](./structureddocumenttag/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::Markup::SdtType, Aspose::Words::Markup::MarkupLevel) | Инициализирует новый экземпляр класса **Structured document tag**. |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| static [Type](./type/)() |  |
## Примечания


Теги структурированных документов (SDT) позволяют внедрять определяемую пользователем семантику, а также их поведение и внешний вид в документ.

В этой версии Aspose.Words предоставляет ряд публичных методов и свойств для управления поведением и содержимым [StructuredDocumentTag](./). Сопоставление узлов SDT с пользовательскими пакетами XML в документе может быть выполнено с использованием свойства [XmlMapping](./get_xmlmapping/).

[StructuredDocumentTag](./) can occur in a document in the following places:

* Block-level - Among paragraphs and tables, as a child of a [Body](../../aspose.words/body/), [HeaderFooter](../../aspose.words/headerfooter/), [Comment](../../aspose.words/comment/), [Footnote](../../aspose.words.notes/footnote/) or a [Shape](../../aspose.words.drawing/shape/) node.
* Row-level - Among rows in a table, as a child of a [Table](../../aspose.words.tables/table/) node.
* Cell-level - Among cells in a table row, as a child of a [Row](../../aspose.words.tables/row/) node.
* Inline-level - Among inline content inside, as a child of a [Paragraph](../../aspose.words/paragraph/).
* Nested inside another [StructuredDocumentTag](./).



## Примеры



Показывает, как работать со стилями для элементов управления содержимым.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ниже представлены два способа применения стиля из документа к structured document tag.
// 1 -  Применить объект стиля из коллекции стилей документа:
System::SharedPtr<Aspose::Words::Style> quoteStyle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Quote);
auto sdtPlainText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  Ссылка на стиль в документе по имени:
auto sdtRichText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RichText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtRichText->set_StyleName(u"Quote");

builder->InsertNode(sdtPlainText);
builder->InsertNode(sdtRichText);

ASSERT_EQ(Aspose::Words::NodeType::StructuredDocumentTag, sdtPlainText->get_NodeType());

System::SharedPtr<Aspose::Words::NodeCollection> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true);

for (auto&& node : System::IterateOver(tags))
{
    auto sdt = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(node);

    std::cout << sdt->get_WordOpenXMLMinimal() << std::endl;

    ASSERT_EQ(Aspose::Words::StyleIdentifier::Quote, sdt->get_Style()->get_StyleIdentifier());
    ASSERT_EQ(u"Quote", sdt->get_StyleName());
}
```

## См. также

* Class [CompositeNode](../../aspose.words/compositenode/)
* Interface [IStructuredDocumentTag](../istructureddocumenttag/)
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
