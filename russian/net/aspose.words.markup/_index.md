---
title: Aspose.Words.Markup
linktitle: Aspose.Words.Markup
articleTitle: Aspose.Words.Markup
second_title: Aspose.Words для .NET
description: Откройте для себя пространство имен Aspose.Words.Markup, включающее настраиваемые классы для смарт-тегов, XML и элементов управления содержимым, которые помогут вам улучшить управление документами.
type: docs
weight: 180
url: /ru/net/aspose.words.markup/
---
The**Aspose.Words.Markup** Пространство имен содержит классы, которые представляют определяемую пользователем семантику в документе: смарт-теги, пользовательский XML и структурированные теги документа (элементы управления содержимым).

## Классы

| Учебный класс | Описание |
| --- | --- |
| [CustomPart](./custompart/) | Представляет собой пользовательскую часть (произвольное содержимое), которая не определена стандартом ISO/IEC 29500. |
| [CustomPartCollection](./custompartcollection/) | Представляет собой коллекцию[`CustomPart`](../aspose.words.markup/custompart/) объекты. |
| [CustomXmlPart](./customxmlpart/) | Представляет часть хранилища пользовательских XML-данных (пользовательские XML-данные в пакете). |
| [CustomXmlPartCollection](./customxmlpartcollection/) | Представляет коллекцию пользовательских XML-частей. Элементы[`CustomXmlPart`](../aspose.words.markup/customxmlpart/) объекты. |
| [CustomXmlProperty](./customxmlproperty/) | Представляет один пользовательский атрибут XML или свойство смарт-тега. |
| [CustomXmlPropertyCollection](./customxmlpropertycollection/) | Представляет коллекцию пользовательских атрибутов XML или свойств смарт-тегов. |
| [CustomXmlSchemaCollection](./customxmlschemacollection/) | Коллекция строк, представляющих схемы XML, связанные с пользовательской частью XML. |
| [SdtListItem](./sdtlistitem/) | Этот элемент определяет один элемент списка в родительскомComboBox илиDropDownList структурированный документ тег. |
| [SdtListItemCollection](./sdtlistitemcollection/) | Предоставляет доступ к[`SdtListItem`](../aspose.words.markup/sdtlistitem/) элементы структурированного документа тег. |
| [SmartTag](./smarttag/) | Этот элемент определяет наличие смарт-тега вокруг одной или нескольких встроенных структур (выступов, изображений, полей и т. д.) внутри абзаца. |
| [StructuredDocumentTag](./structureddocumenttag/) | Представляет структурированный тег документа (SDT или элемент управления содержимым) в документе. |
| [StructuredDocumentTagCollection](./structureddocumenttagcollection/) | Коллекция[`IStructuredDocumentTag`](../aspose.words.markup/istructureddocumenttag/) экземпляры, представляющие структурированные теги документа в указанном диапазоне. |
| [StructuredDocumentTagRangeEnd](./structureddocumenttagrangeend/) | Представляет собой конец**дальний** структурированный тег документа, который принимает многосекционный контент. См. также[`StructuredDocumentTagRangeStart`](../aspose.words.markup/structureddocumenttagrangestart/) узел. |
| [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/) | Представляет начало**дальний** структурированный тег документа, который принимает многосекционный контент. См. также[`StructuredDocumentTagRangeEnd`](../aspose.words.markup/structureddocumenttagrangeend/) . |
| [XmlMapping](./xmlmapping/) | Указывает информацию, которая используется для установления сопоставления между структурированным тегом документа parent и элементом XML, хранящимся в пользовательской части данных XML в документе. |
## Интерфейсы

| Интерфейс | Описание |
| --- | --- |
| [IStructuredDocumentTag](./istructureddocumenttag/) | Интерфейс для определения общих данных для[`StructuredDocumentTag`](../aspose.words.markup/structureddocumenttag/) и[`StructuredDocumentTagRangeStart`](../aspose.words.markup/structureddocumenttagrangestart/) . |
## перечисление

| перечисление | Описание |
| --- | --- |
| [MarkupLevel](./markuplevel/) | Указывает уровень в дереве документа, где находится конкретный[`StructuredDocumentTag`](../aspose.words.markup/structureddocumenttag/) может произойти. |
| [SdtAppearance](./sdtappearance/) | Задает внешний вид структурированного тега документа. |
| [SdtCalendarType](./sdtcalendartype/) | Указывает возможные типы календарей, которые можно использовать для указания[`CalendarType`](../aspose.words.markup/structureddocumenttag/calendartype/) в документе Office Open XML. |
| [SdtDateStorageFormat](./sdtdatestorageformat/) | Указывает, как дата для SDT даты сохраняется/извлекается, когда SDT привязан к узлу XML в хранилище данных документа. |
| [SdtType](./sdttype/) | Указывает тип узла структурированного тега документа (SDT). |
