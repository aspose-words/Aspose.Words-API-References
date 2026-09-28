---
title: "Интерфейс Aspose::Words::Markup::IStructuredDocumentTag"
linktitle: "IStructuredDocumentTag"
second_title: "Справочник API Aspose.Words для C++"
description: "Интерфейс Aspose::Words::Markup::IStructuredDocumentTag. Интерфейс для определения общих данных для StructuredDocumentTag и StructuredDocumentTagRangeStart в C++."
type: docs
weight: 16000
url: /ru/cpp/aspose.words.markup/istructureddocumenttag/
---
## IStructuredDocumentTag interface


Интерфейс для определения общих данных для [StructuredDocumentTag](../structureddocumenttag/) и [StructuredDocumentTagRangeStart](../structureddocumenttagrangestart/).

```cpp
class IStructuredDocumentTag : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| virtual [get_Appearance](./get_appearance/)() | Получает или задает внешний вид структурированного тега документа. |
| virtual [get_Color](./get_color/)() | Получает или задает цвет структурированного тега документа. |
| virtual [get_Id](./get_id/)() | Указывает уникальный только для чтения постоянный числовой идентификатор для этого **SDT**. |
| virtual [get_IsMultiSection](./get_ismultisection/)() | Возвращает true, если данный экземпляр является диапазонным (многоразделным) структурированным тегом документа. |
| virtual [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() | Указывает, следует ли интерпретировать содержимое этого **SDT** как содержащие текст-заполнитель (в отличие от обычного текста внутри **SDT**). Если установлено в true, это состояние будет восстановлено (показ текста-заполнителя) при открытии документа. |
| virtual [get_Level](./get_level/)() const | Получает уровень, на котором этот **SDT** находится в дереве документа. |
| virtual [get_LockContentControl](./get_lockcontentcontrol/)() | Если установлено в true, это свойство запретит пользователю удалять этот **SDT**. |
| virtual [get_LockContents](./get_lockcontents/)() | Если установлено в true, это свойство запретит пользователю редактировать содержимое этого **SDT**. |
| virtual [get_Node](./get_node/)() | Возвращает объект [Node](../../aspose.words/node/), реализующий этот интерфейс. |
| virtual [get_Placeholder](./get_placeholder/)() | Получает [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/), содержащий текст-заполнитель, который должен отображаться, когда содержимое этого SDT пусто, соответствующий сопоставленный элемент XML пуст, как указано в элементе [XmlMapping](./get_xmlmapping/), или элемент [IsShowingPlaceholderText](./get_isshowingplaceholdertext/) имеет значение true. |
| virtual [get_PlaceholderName](./get_placeholdername/)() | Получает или задает имя [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/), содержащего текст-заполнитель. |
| virtual [get_SdtType](./get_sdttype/)() | Получает тип этого **Structured document tag**. |
| virtual [get_Tag](./get_tag/)() const | Указывает тег, связанный с текущим узлом SDT. Не может быть null. |
| virtual [get_Title](./get_title/)() const | Указывает удобочитаемое имя, связанное с этим **SDT**. Не может быть null. |
| virtual [get_WordOpenXML](./get_wordopenxml/)() | Получает строку, представляющую XML, содержащийся в узле, в формате [FlatOpc](../../aspose.words/saveformat/). |
| virtual [get_XmlMapping](./get_xmlmapping/)() | Получает объект, представляющий сопоставление этого структурированного тега документа с XML-данными в пользовательской части XML текущего документа. |
| virtual [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) | Возвращает живую коллекцию дочерних узлов, соответствующих указанным типам. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [RemoveSelfOnly](./removeselfonly/)() | Удаляет только этот узел SDT, но сохраняет его содержимое в дереве документа. |
| virtual [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) | Сеттер для [Aspose::Words::Markup::IStructuredDocumentTag::get_Appearance](./get_appearance/). |
| virtual [set_Color](./set_color/)(System::Drawing::Color) | Сеттер для [Aspose::Words::Markup::IStructuredDocumentTag::get_Color](./get_color/). |
| virtual [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) | Сеттер для [Aspose::Words::Markup::IStructuredDocumentTag::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/). |
| virtual [set_LockContentControl](./set_lockcontentcontrol/)(bool) | Сеттер для [Aspose::Words::Markup::IStructuredDocumentTag::get_LockContentControl](./get_lockcontentcontrol/). |
| virtual [set_LockContents](./set_lockcontents/)(bool) | Сеттер для [Aspose::Words::Markup::IStructuredDocumentTag::get_LockContents](./get_lockcontents/). |
| virtual [set_PlaceholderName](./set_placeholdername/)(System::String) | Сеттер для [Aspose::Words::Markup::IStructuredDocumentTag::get_PlaceholderName](./get_placeholdername/). |
| virtual [set_Tag](./set_tag/)(System::String) | Сеттер для [Aspose::Words::Markup::IStructuredDocumentTag::get_Tag](./get_tag/). |
| virtual [set_Title](./set_title/)(System::String) | Сеттер для [Aspose::Words::Markup::IStructuredDocumentTag::get_Title](./get_title/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как удалить структурированный тег документа, но сохраняет содержимое внутри.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// Эта коллекция предоставляет единый интерфейс для доступа к диапазонным и недиапазонным структурированным тегам.
System::SharedPtr<System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>> sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(5, sdts->LINQ_Count());

// Здесь мы можем получить дочерние узлы из общего интерфейса диапазонных и недиапазонных структурированных тегов.
for (auto&& sdt : System::IterateOver(sdts))
{
    if (sdt->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count() > 0)
    {
        sdt->RemoveSelfOnly();
    }
}

sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(0, sdts->LINQ_Count());
```

## См. также

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
