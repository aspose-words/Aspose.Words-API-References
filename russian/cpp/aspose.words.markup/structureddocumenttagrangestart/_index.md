---
title: "класс Aspose::Words::Markup::StructuredDocumentTagRangeStart"
linktitle: "StructuredDocumentTagRangeStart"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart class. Представляет начало диапазонного структурированного тега документа, который принимает содержимое из нескольких разделов. См. также StructuredDocumentTagRangeEnd. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 14000
url: /ru/cpp/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class


Представляет начало **ranged** структурированного тега документа, который принимает содержимое из нескольких разделов. См. также [StructuredDocumentTagRangeEnd](../structureddocumenttagrangeend/). Чтобы узнать больше, посетите статью документации [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class StructuredDocumentTagRangeStart : public Aspose::Words::Node,
                                        public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>,
                                        public Aspose::Words::Markup::IStructuredDocumentTag
```

## Методы

| Метод | Описание |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Принимает посетителя. |
| [AppendChild](./appendchild/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Добавляет указанный узел в конец диапазона stdContent. |
| [Clone](../../aspose.words/node/clone/)(bool) | Создаёт дубликат узла. |
| [get_Appearance](./get_appearance/)() override | Получает или задает внешний вид структурированного тега документа. |
| [get_Color](./get_color/)() override | Получает или задает цвет структурированного тега документа. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Указывает пользовательский идентификатор узла. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Возвращает документ, к которому принадлежит этот узел. |
| [get_Id](./get_id/)() override | Указывает уникальный только для чтения постоянный числовой Id для этого структурированного тега документа. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Возвращает **true**, если этот узел может содержать другие узлы. |
| [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() override | Указывает, следует ли интерпретировать содержимое этого структурированного тега документа как содержащие текст‑заполнитель (в отличие от обычного текста внутри тега). Если установлено в **true**, это состояние будет восстановлено (отображая текст‑заполнитель) при открытии документа. |
| [get_LastChild](./get_lastchild/)() | Получает последний дочерний элемент в диапазоне stdContent. |
| [get_Level](./get_level/)() const override | Получает уровень, на котором начинается диапазон этого структурированного тега документа в дереве документа. |
| [get_LockContentControl](./get_lockcontentcontrol/)() override | Когда установлено в **true**, это свойство запретит пользователю удалять этот структурированный тег документа. |
| [get_LockContents](./get_lockcontents/)() override | Когда установлено в **true**, это свойство запретит пользователю редактировать содержимое этого структурированного тега документа. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Возвращает узел, непосредственно следующий за этим узлом. |
| [get_NodeType](./get_nodetype/)() const override | Возвращает [StructuredDocumentTagRangeStart](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Возвращает непосредственного родителя этого узла. |
| [get_Placeholder](./get_placeholder/)() override | Получает [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/), содержащий текст‑заполнитель, который должен отображаться, когда содержимое выполнения этого структурированного тега документа пусто, соответствующий сопоставленный XML‑элемент пуст, как указано через элемент [XmlMapping](./get_xmlmapping/), или элемент [IsShowingPlaceholderText](./get_isshowingplaceholdertext/) имеет значение **true**. |
| [get_PlaceholderName](./get_placeholdername/)() override | Получает или задает имя [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/), содержащего текст-заполнитель. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Возвращает узел, непосредственно предшествующий этому узлу. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Возвращает объект [Range](../../aspose.words/range/), представляющий часть документа, содержащуюся в этом узле. |
| [get_RangeEnd](./get_rangeend/)() | Указывает конец диапазона, если [StructuredDocumentTag](../structureddocumenttag/) является диапазонным структурированным тегом документа. В противном случае возвращает **null**. |
| [get_SdtType](./get_sdttype/)() override | Получает тип этого структурированного тега документа. |
| [get_Tag](./get_tag/)() const override | Указывает тег, связанный с текущим узлом структурированного тега документа. Не может быть **null**. |
| [get_Title](./get_title/)() const override | Указывает удобочитаемое имя, связанное с этим структурированным тегом документа. Не может быть **null**. |
| [get_WordOpenXML](./get_wordopenxml/)() override | Получает строку, представляющую XML, содержащийся в узле, в формате [FlatOpc](../../aspose.words/saveformat/). |
| [get_WordOpenXMLMinimal](./get_wordopenxmlminimal/)() | Получает строку, представляющую XML, содержащийся в узле в формате [FlatOpc](../../aspose.words/saveformat/). В отличие от свойства [WordOpenXML](./get_wordopenxml/), этот метод генерирует упрощённый документ, исключающий любые части, не связанные с содержимым. |
| [get_XmlMapping](./get_xmlmapping/)() override | Получает объект, представляющий сопоставление диапазона этого структурированного тега документа с XML‑данными в пользовательской части XML текущего документа. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Возвращает первого предка указанного [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) override | Возвращает живую коллекцию дочерних узлов, соответствующих указанным типам. |
| [GetEnumerator](./getenumerator/)() override | Обеспечивает поддержку итерации в стиле foreach по дочерним узлам этого узла. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Получает текст этого узла и всех его дочерних узлов. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает следующий узел согласно алгоритму обхода дерева в порядке предобхода. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Вспомогательный метод, преобразующий значение перечисления типа узла в удобочитаемую строку. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Получает предыдущий узел согласно алгоритму обхода дерева в порядке предобхода. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя из родительского узла. |
| [RemoveAllChildren](./removeallchildren/)() | Удаляет все узлы между этим узлом начала диапазона и узлом конца диапазона. |
| [RemoveSelfOnly](./removeselfonly/)() override | Удаляет этот узел начала диапазона и соответствующие узлы конца диапазона структурированного тега документа, но сохраняет его содержимое в дереве документа. |
| [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) override | Сеттер для [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Appearance](./get_appearance/). |
| [set_Color](./set_color/)(System::Drawing::Color) override | Сеттер для [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Color](./get_color/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Сеттер для [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) override | Сеттер для [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/). |
| [set_LockContentControl](./set_lockcontentcontrol/)(bool) override | Сеттер для [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_LockContentControl](./get_lockcontentcontrol/). |
| [set_LockContents](./set_lockcontents/)(bool) override | Сеттер для [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_LockContents](./get_lockcontents/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PlaceholderName](./set_placeholdername/)(System::String) override | Сеттер для [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_PlaceholderName](./get_placeholdername/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Tag](./set_tag/)(System::String) override | Сеттер для [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Tag](./get_tag/). |
| [set_Title](./set_title/)(System::String) override | Сеттер для [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Title](./get_title/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](./settemplateweakptr/)(uint32_t) override |  |
| [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::Markup::SdtType) | Инициализирует новый экземпляр класса **Structured document tag range start**. |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| static [Type](./type/)() |  |

## Примеры



Показывает, как получить свойства многоразделных структурированных тегов документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");

auto rangeStartTag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, true)->idx_get(0));
auto rangeEndTag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeEnd>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeEnd, true)->idx_get(0));

std::cout << "StructuredDocumentTagRangeStart values:" << std::endl;
std::cout << System::String::Format(u"\t|Id: {0}", rangeStartTag->get_Id()) << std::endl;
std::cout << System::String::Format(u"\t|Title: {0}", rangeStartTag->get_Title()) << std::endl;
std::cout << System::String::Format(u"\t|PlaceholderName: {0}", rangeStartTag->get_PlaceholderName()) << std::endl;
std::cout << System::String::Format(u"\t|IsShowingPlaceholderText: {0}", rangeStartTag->get_IsShowingPlaceholderText()) << std::endl;
std::cout << System::String::Format(u"\t|LockContentControl: {0}", rangeStartTag->get_LockContentControl()) << std::endl;
std::cout << System::String::Format(u"\t|LockContents: {0}", rangeStartTag->get_LockContents()) << std::endl;
std::cout << System::String::Format(u"\t|Level: {0}", rangeStartTag->get_Level()) << std::endl;
std::cout << System::String::Format(u"\t|NodeType: {0}", rangeStartTag->get_NodeType()) << std::endl;
std::cout << System::String::Format(u"\t|RangeEnd: {0}", rangeStartTag->get_RangeEnd()) << std::endl;
std::cout << System::String::Format(u"\t|Color: {0}", rangeStartTag->get_Color().ToArgb()) << std::endl;
std::cout << System::String::Format(u"\t|SdtType: {0}", rangeStartTag->get_SdtType()) << std::endl;
std::cout << System::String::Format(u"\t|FlatOpcContent: {0}", rangeStartTag->get_WordOpenXML()) << std::endl;
std::cout << System::String::Format(u"\t|Tag: {0}\n", rangeStartTag->get_Tag()) << std::endl;

std::cout << "StructuredDocumentTagRangeEnd values:" << std::endl;
std::cout << System::String::Format(u"\t|Id: {0}", rangeEndTag->get_Id()) << std::endl;
std::cout << System::String::Format(u"\t|NodeType: {0}", rangeEndTag->get_NodeType()) << std::endl;
```

## См. также

* Class [Node](../../aspose.words/node/)
* Interface [IStructuredDocumentTag](../istructureddocumenttag/)
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
