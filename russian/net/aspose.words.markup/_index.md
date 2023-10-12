---
title: Aspose.Words.Markup
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Markup Пространство имен содержит классы которые представляют определяемую пользователем семантику в документе смарттеги настраиваемый XML и теги структурированного документа элементы управления содержимым.
type: docs
weight: 160
url: /ru/net/aspose.words.markup/
---
**Aspose.Words.Markup** Пространство имен содержит классы, которые представляют определяемую пользователем семантику в документе: смарт-теги, настраиваемый XML и теги структурированного документа (элементы управления содержимым).

## Классы

| Учебный класс | Описание |
| --- | --- |
| [CustomPart](./custompart/) | Представляет пользовательскую часть (произвольное содержимое), которая не определена стандартом ISO/IEC 29500. |
| [CustomPartCollection](./custompartcollection/) | Представляет коллекцию[`CustomPart`](../aspose.words.markup/custompart/) объекты. |
| [CustomXmlPart](./customxmlpart/) | Представляет пользовательскую часть хранилища данных XML (пользовательские данные XML в пакете). |
| [CustomXmlPartCollection](./customxmlpartcollection/) | Представляет коллекцию пользовательских частей XML. Предметы[`CustomXmlPart`](../aspose.words.markup/customxmlpart/) объекты. |
| [CustomXmlProperty](./customxmlproperty/) | Представляет один пользовательский атрибут XML или свойство смарт-тега. |
| [CustomXmlPropertyCollection](./customxmlpropertycollection/) | Представляет коллекцию пользовательских атрибутов XML или свойств смарт-тегов. |
| [CustomXmlSchemaCollection](./customxmlschemacollection/) | Коллекция строк, представляющих схемы XML, связанные с пользовательской частью XML. |
| [SdtListItem](./sdtlistitem/) | Этот элемент определяет один элемент списка в родительском списке.ComboBox илиDropDownList тег структурированного документа. |
| [SdtListItemCollection](./sdtlistitemcollection/) | Обеспечивает доступ к[`SdtListItem`](../aspose.words.markup/sdtlistitem/) элементы тега структурированного документа. |
| [SmartTag](./smarttag/) | Этот элемент определяет наличие смарт-тега вокруг одной или нескольких встроенных структур (прогонов, изображений, полей и т. д.) внутри абзаца. |
| [StructuredDocumentTag](./structureddocumenttag/) | Представляет структурированный тег документа (SDT или элемент управления содержимым) в документе. |
| [StructuredDocumentTagCollection](./structureddocumenttagcollection/) | Коллекция[`IStructuredDocumentTag`](../aspose.words.markup/istructureddocumenttag/) экземпляры, представляющие теги структурированного документа в указанном диапазоне. |
| [StructuredDocumentTagRangeEnd](./structureddocumenttagrangeend/) | Обозначает конец **дальнего боя** тег структурированного документа, который принимает содержимое из нескольких разделов. См. также[`StructuredDocumentTagRangeStart`](../aspose.words.markup/structureddocumenttagrangestart/) узел. |
| [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/) | Обозначает начало **дальнего боя** тег структурированного документа, который принимает содержимое из нескольких разделов. См. также[`StructuredDocumentTagRangeEnd`](../aspose.words.markup/structureddocumenttagrangeend/) . |
| [XmlMapping](./xmlmapping/) | Указывает информацию, которая используется для установления сопоставления между тегом структурированного документа Parent и элементом XML, хранящимся в пользовательской части данных XML в документе. |
## Интерфейсы

| Интерфейс | Описание |
| --- | --- |
| [IStructuredDocumentTag](./istructureddocumenttag/) | Интерфейс для определения общих данных для[`StructuredDocumentTag`](../aspose.words.markup/structureddocumenttag/) и[`StructuredDocumentTagRangeStart`](../aspose.words.markup/structureddocumenttagrangestart/) . |
## перечисление

| перечисление | Описание |
| --- | --- |
| [MarkupLevel](./markuplevel/) | Указывает уровень в дереве документа, на котором конкретный[`StructuredDocumentTag`](../aspose.words.markup/structureddocumenttag/) может произойти. |
| [SdtAppearance](./sdtappearance/) | Определяет внешний вид тега структурированного документа. |
| [SdtCalendarType](./sdtcalendartype/) | Указывает возможные типы календарей, которые можно использовать для указания[`CalendarType`](../aspose.words.markup/structureddocumenttag/calendartype/) в документе Office Open XML. |
| [SdtDateStorageFormat](./sdtdatestorageformat/) | Указывает, как дата для SDT даты сохраняется/извлекается, когда SDT привязан к узлу XML в хранилище данных документа. |
| [SdtType](./sdttype/) | Указывает тип узла тега структурированного документа (SDT). |


