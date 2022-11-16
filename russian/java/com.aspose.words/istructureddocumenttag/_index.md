---
title: IStructuredDocumentTag
second_title: Справочник по API Aspose.Words для Java
description: Интерфейс для определения общих данных для и .
type: docs
weight: 658
url: /ru/java/com.aspose.words/istructureddocumenttag/
---
```
public interface IStructuredDocumentTag
```

 Интерфейс для определения общих данных для[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) а также[StructuredDocumentTagRangeStart](../../com.aspose.words/structureddocumenttagrangestart).
## Методы

| Метод | Описание |
| --- | --- |
| [getColor()](#getColor--) | Получает цвет тега структурированного документа. |
| [getId()](#getId--) |  Указывает уникальный постоянный числовой идентификатор только для чтения для этого**SDT**. |
| [getLevel()](#getLevel--) |  Получает уровень, на котором это**SDT** происходит в дереве документов. |
| [getLockContentControl()](#getLockContentControl--) |  Если установлено значение true, это свойство запрещает пользователю удалять это**SDT**. |
| [getLockContents()](#getLockContents--) |  Если установлено значение true, это свойство запрещает пользователю редактировать содержимое этого**SDT**. |
| [getPlaceholder()](#getPlaceholder--) |  Получает[BuildingBlock](../../com.aspose.words/buildingblock)содержащий текст-заполнитель, который должен отображаться, когда содержимое этого запуска SDT пусто, связанный сопоставленный XML-элемент пуст, как указано в параметре[getXmlMapping()](../../com.aspose.words/istructureddocumenttag\#getXmlMapping--) элемент или[isShowingPlaceholderText()](../../com.aspose.words/istructureddocumenttag\#isShowingPlaceholderText--) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/istructureddocumenttag\#isShowingPlaceholderText-boolean-) элемент истинный. |
| [getPlaceholderName()](#getPlaceholderName--) |  Получает или задает имя[BuildingBlock](../../com.aspose.words/buildingblock) содержащий текст-заполнитель. |
| [getSdtType()](#getSdtType--) |  Получает тип этого**Structured document tag**. |
| [getTag()](#getTag--) | Задает тег, связанный с текущим узлом SDT. |
| [getTitle()](#getTitle--) |  Указывает понятное имя, связанное с этим**SDT**. |
| [getWordOpenXML()](#getWordOpenXML--) |  Получает строку, представляющую XML, содержащийся в узле в[SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC) формат. |
| [getXmlMapping()](#getXmlMapping--) | Получает объект, представляющий сопоставление этого тега структурированного документа с XML-данными в пользовательской XML-части текущего документа. |
| [isRanged()](#isRanged--) | Возвращает true, если этот экземпляр является ранжированным структурированным тегом документа. |
| [isShowingPlaceholderText()](#isShowingPlaceholderText--) |  Указывает, является ли содержимое этого**SDT** должен интерпретироваться как содержащий текст-заполнитель (в отличие от обычного текстового содержимого в SDT). |
| [isShowingPlaceholderText(boolean value)](#isShowingPlaceholderText-boolean-) |  Указывает, является ли содержимое этого**SDT** должен интерпретироваться как содержащий текст-заполнитель (в отличие от обычного текстового содержимого в SDT). |
| [setColor(Color value)](#setColor-java.awt.Color-) | Задает цвет тега структурированного документа. |
| [setLockContentControl(boolean value)](#setLockContentControl-boolean-) |  Если установлено значение true, это свойство запрещает пользователю удалять это**SDT**. |
| [setLockContents(boolean value)](#setLockContents-boolean-) |  Если установлено значение true, это свойство запрещает пользователю редактировать содержимое этого**SDT**. |
| [setPlaceholderName(String value)](#setPlaceholderName-java.lang.String-) |  Получает или задает имя[BuildingBlock](../../com.aspose.words/buildingblock) содержащий текст-заполнитель. |
| [setTag(String value)](#setTag-java.lang.String-) | Задает тег, связанный с текущим узлом SDT. |
| [setTitle(String value)](#setTitle-java.lang.String-) |  Указывает понятное имя, связанное с этим**SDT**. |
| [structuredDocumentTagNode()](#structuredDocumentTagNode--) | Возвращает объект Node, реализующий этот интерфейс. |
### getColor() {#getColor--}
```
public abstract Color getColor()
```


Получает цвет тега структурированного документа.

**Возвращает:**
java.awt.Color — цвет тега структурированного документа.
### getId() {#getId--}
```
public abstract int getId()
```


 Указывает уникальный постоянный числовой идентификатор только для чтения для этого**SDT**.

**Возвращает:**
int - соответствующее значение int.
### getLevel() {#getLevel--}
```
public abstract int getLevel()
```


 Получает уровень, на котором это**SDT** происходит в дереве документов.

**Возвращает:**
 int - Уровень, на котором это**SDT** происходит в дереве документов. Возвращаемое значение является одним из[MarkupLevel](../../com.aspose.words/markuplevel) константы.
### getLockContentControl() {#getLockContentControl--}
```
public abstract boolean getLockContentControl()
```


 Если установлено значение true, это свойство запрещает пользователю удалять это**SDT**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getLockContents() {#getLockContents--}
```
public abstract boolean getLockContents()
```


 Если установлено значение true, это свойство запрещает пользователю редактировать содержимое этого**SDT**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getPlaceholder() {#getPlaceholder--}
```
public abstract BuildingBlock getPlaceholder()
```


 Получает[BuildingBlock](../../com.aspose.words/buildingblock)содержащий текст-заполнитель, который должен отображаться, когда содержимое этого запуска SDT пусто, связанный сопоставленный XML-элемент пуст, как указано в параметре[getXmlMapping()](../../com.aspose.words/istructureddocumenttag\#getXmlMapping--) элемент или[isShowingPlaceholderText()](../../com.aspose.words/istructureddocumenttag\#isShowingPlaceholderText--) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/istructureddocumenttag\#isShowingPlaceholderText-boolean-) элемент истинный. Может быть нулевым, что означает, что заполнитель неприменим для этого Sdt.

**Возвращает:**
[BuildingBlock](../../com.aspose.words/buildingblock) -[BuildingBlock](../../com.aspose.words/buildingblock)содержащий текст-заполнитель, который должен отображаться, когда содержимое этого запуска SDT пусто, связанный сопоставленный XML-элемент пуст, как указано в параметре[getXmlMapping()](../../com.aspose.words/istructureddocumenttag\#getXmlMapping--) элемент или[isShowingPlaceholderText()](../../com.aspose.words/istructureddocumenttag\#isShowingPlaceholderText--) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/istructureddocumenttag\#isShowingPlaceholderText-boolean-) элемент истинный.
### getPlaceholderName() {#getPlaceholderName--}
```
public abstract String getPlaceholderName()
```


 Получает или задает имя[BuildingBlock](../../com.aspose.words/buildingblock) содержащий текст-заполнитель.

 BuildingBlock с этим названием[BuildingBlock.getName()](../../com.aspose.words/buildingblock\#getName--) / [BuildingBlock.setName(java.lang.String)](../../com.aspose.words/buildingblock\#setName-java.lang.String-) должен присутствовать в[Document.getGlossaryDocument()](../../com.aspose.words/document\#getGlossaryDocument--) / [Document.setGlossaryDocument(com.aspose.words.GlossaryDocument)](../../com.aspose.words/document\#setGlossaryDocument-com.aspose.words.GlossaryDocument-) в противном случае возникнет исключение java.lang.IllegalStateException.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getSdtType() {#getSdtType--}
```
public abstract int getSdtType()
```


 Получает тип этого**Structured document tag**.

**Возвращает:**
 int - Тип этого**Structured document tag** . Возвращаемое значение является одним из[SdtType](../../com.aspose.words/sdttype) константы.
### getTag() {#getTag--}
```
public abstract String getTag()
```


Задает тег, связанный с текущим узлом SDT. Не может быть нулевым.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getTitle() {#getTitle--}
```
public abstract String getTitle()
```


 Указывает понятное имя, связанное с этим**SDT**. Не может быть нулевым.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getWordOpenXML() {#getWordOpenXML--}
```
public abstract String getWordOpenXML()
```


 Получает строку, представляющую XML, содержащийся в узле в[SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC) формат.

**Возвращает:**
 java.lang.String — строка, представляющая XML, содержащийся в узле в[SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC) формат.
### getXmlMapping() {#getXmlMapping--}
```
public abstract XmlMapping getXmlMapping()
```


 Получает объект, представляющий сопоставление этого тега структурированного документа с XML-данными в пользовательской XML-части текущего документа. Вы можете использовать[XmlMapping.setMapping(com.aspose.words.CustomXmlPart, java.lang.String, java.lang.String)](../../com.aspose.words/xmlmapping\#setMapping-com.aspose.words.CustomXmlPart--java.lang.String--java.lang.String-) метод этого объекта для сопоставления тега структурированного документа с данными XML.

**Возвращает:**
[XmlMapping](../../com.aspose.words/xmlmapping) - Объект, представляющий сопоставление этого тега структурированного документа с данными XML в пользовательской части XML текущего документа.
### isRanged() {#isRanged--}
```
public abstract boolean isRanged()
```


Возвращает true, если этот экземпляр является ранжированным структурированным тегом документа.

**Возвращает:**
логический
### isShowingPlaceholderText() {#isShowingPlaceholderText--}
```
public abstract boolean isShowingPlaceholderText()
```


 Указывает, является ли содержимое этого**SDT** должен интерпретироваться как содержащий текст-заполнитель (в отличие от обычного текстового содержимого в SDT).

если установлено значение true, это состояние должно быть возобновлено (показывая текст-заполнитель) при открытии этого документа.

**Возвращает:**
boolean - соответствующее логическое значение.
### isShowingPlaceholderText(boolean value) {#isShowingPlaceholderText-boolean-}
```
public abstract void isShowingPlaceholderText(boolean value)
```


 Указывает, является ли содержимое этого**SDT** должен интерпретироваться как содержащий текст-заполнитель (в отличие от обычного текстового содержимого в SDT).

если установлено значение true, это состояние должно быть возобновлено (показывая текст-заполнитель) при открытии этого документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setColor(Color value) {#setColor-java.awt.Color-}
```
public abstract void setColor(Color value)
```


Задает цвет тега структурированного документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.Color | Цвет тега структурированного документа. |

### setLockContentControl(boolean value) {#setLockContentControl-boolean-}
```
public abstract void setLockContentControl(boolean value)
```


 Если установлено значение true, это свойство запрещает пользователю удалять это**SDT**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setLockContents(boolean value) {#setLockContents-boolean-}
```
public abstract void setLockContents(boolean value)
```


 Если установлено значение true, это свойство запрещает пользователю редактировать содержимое этого**SDT**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setPlaceholderName(String value) {#setPlaceholderName-java.lang.String-}
```
public abstract void setPlaceholderName(String value)
```


 Получает или задает имя[BuildingBlock](../../com.aspose.words/buildingblock) содержащий текст-заполнитель.

 BuildingBlock с этим названием[BuildingBlock.getName()](../../com.aspose.words/buildingblock\#getName--) / [BuildingBlock.setName(java.lang.String)](../../com.aspose.words/buildingblock\#setName-java.lang.String-) должен присутствовать в[Document.getGlossaryDocument()](../../com.aspose.words/document\#getGlossaryDocument--) / [Document.setGlossaryDocument(com.aspose.words.GlossaryDocument)](../../com.aspose.words/document\#setGlossaryDocument-com.aspose.words.GlossaryDocument-) в противном случае возникнет исключение java.lang.IllegalStateException.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setTag(String value) {#setTag-java.lang.String-}
```
public abstract void setTag(String value)
```


Задает тег, связанный с текущим узлом SDT. Не может быть нулевым.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setTitle(String value) {#setTitle-java.lang.String-}
```
public abstract void setTitle(String value)
```


 Указывает понятное имя, связанное с этим**SDT**. Не может быть нулевым.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### structuredDocumentTagNode() {#structuredDocumentTagNode--}
```
public abstract Node structuredDocumentTagNode()
```


Возвращает объект Node, реализующий этот интерфейс.

**Возвращает:**
[Node](../../com.aspose.words/node)