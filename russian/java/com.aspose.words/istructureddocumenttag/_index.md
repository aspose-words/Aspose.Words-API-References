---
title: "IStructuredDocumentTag"
linktitle: "IStructuredDocumentTag"
second_title: "Aspose.Words для Java"
description: "Интерфейс для определения общих данных для StructuredDocumentTag и StructuredDocumentTagRangeStart в Java."
type: docs
weight: 785
url: /ru/java/com.aspose.words/istructureddocumenttag/
---
```
public interface IStructuredDocumentTag
```

Интерфейс для определения общих данных для [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) и [StructuredDocumentTagRangeStart](../../com.aspose.words/structureddocumenttagrangestart/).

 **Examples:** 

Показывает, как удалить структурированный тег документа, но сохраняет содержимое внутри.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");

 // This collection provides a unified interface for accessing ranged and non-ranged structured tags.
 StructuredDocumentTagCollection sdts = doc.getRange().getStructuredDocumentTags();
 Assert.assertEquals(5, sdts.getCount());

 // Here we can get child nodes from the common interface of ranged and non-ranged structured tags.
 for (IStructuredDocumentTag sdt : sdts)
     if (sdt.getChildNodes(NodeType.ANY, false).getCount() > 0)
         sdt.removeSelfOnly();

 sdts = doc.getRange().getStructuredDocumentTags();
 Assert.assertEquals(0, sdts.getCount());
 
```
## Методы

| Метод | Описание |
| --- | --- |
| [getAppearance()](#getAppearance) | Получает внешний вид структурированного тега документа. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean) |  |
| [getColor()](#getColor) | Получает цвет структурированного тега документа. |
| [getId()](#getId) | Указывает уникальный только для чтения постоянный числовой Id для этого **SDT**. |
| [getLevel()](#getLevel) | Получает уровень, на котором этот **SDT** находится в дереве документа. |
| [getLockContentControl()](#getLockContentControl) | Если установить в true, это свойство запретит пользователю удалять этот **SDT**. |
| [getLockContents()](#getLockContents) | Если установить в true, это свойство запретит пользователю изменять содержимое этого **SDT**. |
| [getNode()](#getNode) | Возвращает объект Node, реализующий этот интерфейс. |
| [getPlaceholder()](#getPlaceholder) | Получает [BuildingBlock](../../com.aspose.words/buildingblock/), содержащий текст-заполнитель, который должен отображаться, когда содержимое этого SDT пусто, соответствующий сопоставленный XML‑элемент пуст, как указано через элемент [getXmlMapping()](../../com.aspose.words/istructureddocumenttag/\#getXmlMapping) или элемент [isShowingPlaceholderText()](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText-boolean) установлен в true. |
| [getPlaceholderName()](#getPlaceholderName) | Получает или задает имя [BuildingBlock](../../com.aspose.words/buildingblock/), содержащего текст-заполнитель. |
| [getSdtType()](#getSdtType) | Получает тип этого **Structured document tag**. |
| [getTag()](#getTag) | Указывает тег, связанный с текущим узлом SDT. |
| [getTitle()](#getTitle) | Указывает удобочитаемое имя, связанное с этим **SDT**. |
| [getWordOpenXML()](#getWordOpenXML) | Получает строку, представляющую XML, содержащийся в узле, в формате [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC). |
| [getXmlMapping()](#getXmlMapping) | Получает объект, представляющий сопоставление этого структурированного тега документа с XML‑данными в пользовательской части XML текущего документа. |
| [isMultiSection()](#isMultiSection) | Возвращает true, если данный экземпляр является диапазонным (многоразделным) структурированным тегом документа. |
| [isShowingPlaceholderText()](#isShowingPlaceholderText) | Указывает, следует ли интерпретировать содержимое этого **SDT** как содержащий текст-заполнитель (в отличие от обычного текста внутри SDT). |
| [isShowingPlaceholderText(boolean value)](#isShowingPlaceholderText-boolean) | Указывает, следует ли интерпретировать содержимое этого **SDT** как содержащий текст-заполнитель (в отличие от обычного текста внутри SDT). |
| [removeSelfOnly()](#removeSelfOnly) | Удаляет только сам узел SDT, но сохраняет его содержимое внутри дерева документа. |
| [setAppearance(int value)](#setAppearance-int) | Устанавливает внешний вид структурированного тега документа. |
| [setColor(Color value)](#setColor-java.awt.Color) | Устанавливает цвет структурированного тега документа. |
| [setLockContentControl(boolean value)](#setLockContentControl-boolean) | Если установить в true, это свойство запретит пользователю удалять этот **SDT**. |
| [setLockContents(boolean value)](#setLockContents-boolean) | Если установить в true, это свойство запретит пользователю изменять содержимое этого **SDT**. |
| [setPlaceholderName(String value)](#setPlaceholderName-java.lang.String) | Получает или задает имя [BuildingBlock](../../com.aspose.words/buildingblock/), содержащего текст-заполнитель. |
| [setTag(String value)](#setTag-java.lang.String) | Указывает тег, связанный с текущим узлом SDT. |
| [setTitle(String value)](#setTitle-java.lang.String) | Указывает удобочитаемое имя, связанное с этим **SDT**. |
### getAppearance() {#getAppearance}
```
public abstract int getAppearance()
```


Получает внешний вид структурированного тега документа.

 **Examples:** 

Показывает, как отобразить тег вокруг содержимого.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");
 StructuredDocumentTagRangeStart tag = (StructuredDocumentTagRangeStart) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, true);

 if (tag.getAppearance() == SdtAppearance.HIDDEN)
     tag.setAppearance(SdtAppearance.TAGS);
 
```

**Returns:**
int — Внешний вид структурированного тега документа. Возвращаемое значение является одной из констант [SdtAppearance](../../com.aspose.words/sdtappearance/).
### getChildNodes(int nodeType, boolean isDeep) {#getChildNodes-int-boolean}
```
public abstract NodeCollection getChildNodes(int nodeType, boolean isDeep)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| nodeType | int |  |
| isDeep | boolean |  |

**Returns:**
[NodeCollection](../../com.aspose.words/nodecollection/)
### getColor() {#getColor}
```
public abstract Color getColor()
```


Получает цвет структурированного тега документа.

 **Examples:** 

Показывает, как получить свойства многоразделных структурированных тегов документа.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Returns:**
java.awt.Color - Цвет структурированного тега документа.
### getId() {#getId}
```
public abstract int getId()
```


Указывает уникальный только для чтения постоянный числовой Id для этого **SDT**.

 **Examples:** 

Показывает, как получить свойства многоразделных структурированных тегов документа.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Returns:**
int — соответствующее значение  int .
### getLevel() {#getLevel}
```
public abstract int getLevel()
```


Получает уровень, на котором этот **SDT** находится в дереве документа.

 **Examples:** 

Показывает, как получить свойства многоразделных структурированных тегов документа.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Returns:**
int - Уровень, на котором происходит этот **SDT** в дереве документа. Возвращаемое значение является одной из констант [MarkupLevel](../../com.aspose.words/markuplevel/).
### getLockContentControl() {#getLockContentControl}
```
public abstract boolean getLockContentControl()
```


Если установить в true, это свойство запретит пользователю удалять этот **SDT**.

 **Examples:** 

Показывает, как применить ограничения редактирования к структурированным тегам документа.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a plain text structured document tag, which acts as a text box that prompts the user to fill it in.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the "LockContents" property to "true" to prohibit the user from editing this text box's contents.
 tag.setLockContents(true);
 builder.write("The contents of this structured document tag cannot be edited: ");
 builder.insertNode(tag);

 tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the "LockContentControl" property to "true" to prohibit the user from
 // deleting this structured document tag manually in Microsoft Word.
 tag.setLockContentControl(true);

 builder.insertParagraph();
 builder.write("This structured document tag cannot be deleted but its contents can be edited: ");
 builder.insertNode(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.Lock.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getLockContents() {#getLockContents}
```
public abstract boolean getLockContents()
```


Если установить в true, это свойство запретит пользователю изменять содержимое этого **SDT**.

 **Examples:** 

Показывает, как применить ограничения редактирования к структурированным тегам документа.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a plain text structured document tag, which acts as a text box that prompts the user to fill it in.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the "LockContents" property to "true" to prohibit the user from editing this text box's contents.
 tag.setLockContents(true);
 builder.write("The contents of this structured document tag cannot be edited: ");
 builder.insertNode(tag);

 tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the "LockContentControl" property to "true" to prohibit the user from
 // deleting this structured document tag manually in Microsoft Word.
 tag.setLockContentControl(true);

 builder.insertParagraph();
 builder.write("This structured document tag cannot be deleted but its contents can be edited: ");
 builder.insertNode(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.Lock.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getNode() {#getNode}
```
public abstract Node getNode()
```


Возвращает объект Node, реализующий этот интерфейс.

**Returns:**
[Node](../../com.aspose.words/node/) - Node object that implements this interface.
### getPlaceholder() {#getPlaceholder}
```
public abstract BuildingBlock getPlaceholder()
```


Получает [BuildingBlock](../../com.aspose.words/buildingblock/), содержащий текст-заполнитель, который должен отображаться, когда содержимое этого SDT пусто, соответствующий сопоставленный XML‑элемент пуст, как указано через элемент [getXmlMapping()](../../com.aspose.words/istructureddocumenttag/\#getXmlMapping) или элемент [isShowingPlaceholderText()](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText-boolean) установлен в true.

 **Remarks:** 

Может быть null, что означает, что заполнитель не применим к этому Sdt.

 **Examples:** 

Показывает, как использовать содержимое строительного блока в качестве пользовательского текста заполнителя для структурированного тега документа.

```

 Document doc = new Document();

 // Insert a plain text structured document tag of the "PlainText" type, which will function as a text box.
 // The contents that it will display by default are a "Click here to enter text." prompt.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // We can get the tag to display the contents of a building block instead of the default text.
 // First, add a building block with contents to the glossary document.
 GlossaryDocument glossaryDoc = doc.getGlossaryDocument();

 BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
 substituteBlock.setName("Custom Placeholder");
 substituteBlock.appendChild(new Section(glossaryDoc));
 substituteBlock.getFirstSection().appendChild(new Body(glossaryDoc));
 substituteBlock.getFirstSection().getBody().appendParagraph("Custom placeholder text.");

 glossaryDoc.appendChild(substituteBlock);

 // Then, use the structured document tag's "PlaceholderName" property to reference that building block by name.
 tag.setPlaceholderName("Custom Placeholder");

 // If "PlaceholderName" refers to an existing block in the parent document's glossary document,
 // we will be able to verify the building block via the "Placeholder" property.
 Assert.assertEquals(substituteBlock, tag.getPlaceholder());

 // Set the "IsShowingPlaceholderText" property to "true" to treat the
 // structured document tag's current contents as placeholder text.
 // This means that clicking on the text box in Microsoft Word will immediately highlight all the tag's contents.
 // Set the "IsShowingPlaceholderText" property to "false" to get the
 // structured document tag to treat its contents as text that a user has already entered.
 // Clicking on this text in Microsoft Word will place the blinking cursor at the clicked location.
 tag.isShowingPlaceholderText(isShowingPlaceholderText);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
 
```

**Returns:**
[BuildingBlock](../../com.aspose.words/buildingblock/) - The [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [getXmlMapping()](../../com.aspose.words/istructureddocumenttag/\#getXmlMapping) element or the [isShowingPlaceholderText()](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText-boolean) element is true.
### getPlaceholderName() {#getPlaceholderName}
```
public abstract String getPlaceholderName()
```


Получает или задает имя [BuildingBlock](../../com.aspose.words/buildingblock/), содержащего текст-заполнитель.

**Returns:**
java.lang.String - Соответствующее значение java.lang.String.
### getSdtType() {#getSdtType}
```
public abstract int getSdtType()
```


Получает тип этого **Structured document tag**.

**Returns:**
int - Тип этого **Structured document tag**. Возвращаемое значение является одной из констант [SdtType](../../com.aspose.words/sdttype/).
### getTag() {#getTag}
```
public abstract String getTag()
```


Указывает тег, связанный с текущим узлом SDT. Не может быть null.

 **Examples:** 

Показывает, как создать структурированный тег документа в обычном текстовом поле и изменить его внешний вид.

```

 Document doc = new Document();

 // Create a structured document tag that will contain plain text.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the title and color of the frame that appears when you mouse over the structured document tag in Microsoft Word.
 tag.setTitle("My plain text");
 tag.setColor(Color.MAGENTA);

 // Set a tag for this structured document tag, which is obtainable
 // as an XML element named "tag", with the string below in its "@val" attribute.
 tag.setTag("MyPlainTextSDT");

 // Every structured document tag has a random unique ID.
 Assert.assertTrue(tag.getId() > 0);

 // Set the font for the text inside the structured document tag.
 tag.getContentsFont().setName("Arial");

 // Set the font for the text at the end of the structured document tag.
 // Any text that we type in the document body after moving out of the tag with arrow keys will use this font.
 tag.getEndCharacterFont().setName("Arial Black");

 // By default, this is false and pressing enter while inside a structured document tag does nothing.
 // When set to true, our structured document tag can have multiple lines.

 // Set the "Multiline" property to "false" to only allow the contents
 // of this structured document tag to span a single line.
 // Set the "Multiline" property to "true" to allow the tag to contain multiple lines of content.
 tag.setMultiline(true);

 // Set the "Appearance" property to "SdtAppearance.Tags" to show tags around content.
 // By default structured document tag shows as BoundingBox.
 tag.setAppearance(SdtAppearance.TAGS);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(tag);

 // Insert a clone of our structured document tag in a new paragraph.
 StructuredDocumentTag tagClone = (StructuredDocumentTag) tag.deepClone(true);
 builder.insertParagraph();
 builder.insertNode(tagClone);

 // Use the "RemoveSelfOnly" method to remove a structured document tag, while keeping its contents in the document.
 tagClone.removeSelfOnly();

 doc.save(getArtifactsDir() + "StructuredDocumentTag.PlainText.docx");
 
```

**Returns:**
java.lang.String - Соответствующее значение java.lang.String.
### getTitle() {#getTitle}
```
public abstract String getTitle()
```


Указывает дружественное имя, связанное с этим **SDT**. Не может быть null.

 **Examples:** 

Показывает, как получить структурированный тег документа.

```

 Document doc = new Document(getMyDir() + "Structured document tags by id.docx");

 // Get the structured document tag by Id.
 IStructuredDocumentTag sdt = doc.getRange().getStructuredDocumentTags().getById(1160505028);
 System.out.println(sdt.isMultiSection());
 System.out.println(sdt.getTitle());

 // Get the structured document tag or ranged tag by Title.
 sdt = doc.getRange().getStructuredDocumentTags().getByTitle("Alias4");
 System.out.println(sdt.getId());
 
```

**Returns:**
java.lang.String - Соответствующее значение java.lang.String.
### getWordOpenXML() {#getWordOpenXML}
```
public abstract String getWordOpenXML()
```


Получает строку, представляющую XML, содержащийся в узле, в формате [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC).

 **Examples:** 

Показывает, как получить XML, содержащийся в узле в формате FlatOpc.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");

 List tags = Arrays.stream(doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG, true).toArray())
         .filter(StructuredDocumentTag.class::isInstance)
         .map(StructuredDocumentTag.class::cast)
         .collect(Collectors.toList());

 Assert.assertTrue(tags.get(0).getWordOpenXML()
         .contains(
                 ""));
 
```

**Returns:**
java.lang.String - Строка, представляющая XML, содержащийся в узле в формате [SaveFormat.FLAT\\_OPC](../../com.aspose.words/saveformat/\\#FLAT-OPC).
### getXmlMapping() {#getXmlMapping}
```
public abstract XmlMapping getXmlMapping()
```


Получает объект, представляющий сопоставление этого структурированного тега документа с XML‑данными в пользовательской части XML текущего документа.

 **Remarks:** 

Вы можете использовать метод [XmlMapping.setMapping(com.aspose.words.CustomXmlPart, java.lang.String, java.lang.String)](../../com.aspose.words/xmlmapping/\\#setMapping-com.aspose.words.CustomXmlPart--java.lang.String--java.lang.String) этого объекта для сопоставления структурированного тега документа с XML-данными.

 **Examples:** 

Показывает, как создать структурированный тег документа с пользовательскими XML-данными.

```

 Document doc = new Document();

 // Construct an XML part that contains data and add it to the document's collection.
 // If we enable the "Developer" tab in Microsoft Word,
 // we can find elements from this collection in the "XML Mapping Pane", along with a few default elements.
 String xmlPartId = UUID.randomUUID().toString();
 String xmlPartContent = "Hello, World!";
 CustomXmlPart xmlPart = doc.getCustomXmlParts().add(xmlPartId, xmlPartContent);

 Assert.assertEquals(xmlPart.getData(), xmlPartContent.getBytes());
 Assert.assertEquals(xmlPart.getId(), xmlPartId);

 // Below are two ways to refer to XML parts.
 // 1 -  By an index in the custom XML part collection:
 Assert.assertEquals(xmlPart, doc.getCustomXmlParts().get(0));

 // 2 -  By GUID:
 Assert.assertEquals(xmlPart, doc.getCustomXmlParts().getById(xmlPartId));

 // Add an XML schema association.
 xmlPart.getSchemas().add("http://www.w3.org/2001/XMLSchema");

 // Clone a part, and then insert it into the collection.
 CustomXmlPart xmlPartClone = xmlPart.deepClone();
 xmlPartClone.setId(UUID.randomUUID().toString());
 doc.getCustomXmlParts().add(xmlPartClone);

 Assert.assertEquals(doc.getCustomXmlParts().getCount(), 2);

 // Iterate through the collection and print the contents of each part.
 Iterator enumerator = doc.getCustomXmlParts().iterator();
 int index = 0;
 while (enumerator.hasNext()) {
     CustomXmlPart customXmlPart = enumerator.next();
     System.out.println(MessageFormat.format("XML part index {0}, ID: {1}", index, customXmlPart.getId()));
     System.out.println(MessageFormat.format("\tContent: {0}", customXmlPart.getData()));
     index++;
 }

 // Use the "RemoveAt" method to remove the cloned part by index.
 doc.getCustomXmlParts().removeAt(1);

 Assert.assertEquals(doc.getCustomXmlParts().getCount(), 1);

 // Clone the XML parts collection, and then use the "Clear" method to remove all its elements at once.
 CustomXmlPartCollection customXmlParts = doc.getCustomXmlParts().deepClone();
 customXmlParts.clear();

 // Create a structured document tag that will display our part's contents and insert it into the document body.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.BLOCK);
 tag.getXmlMapping().setMapping(xmlPart, "/root[1]/text[1]", "");

 doc.getFirstSection().getBody().appendChild(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.CustomXml.docx");
 
```

**Returns:**
[XmlMapping](../../com.aspose.words/xmlmapping/) - An object that represents the mapping of this structured document tag to XML data in a custom XML part of the current document.
### isMultiSection() {#isMultiSection}
```
public abstract boolean isMultiSection()
```


Возвращает true, если данный экземпляр является диапазонным (многоразделным) структурированным тегом документа.

 **Examples:** 

Показывает, как получить структурированный тег документа.

```

 Document doc = new Document(getMyDir() + "Structured document tags by id.docx");

 // Get the structured document tag by Id.
 IStructuredDocumentTag sdt = doc.getRange().getStructuredDocumentTags().getById(1160505028);
 System.out.println(sdt.isMultiSection());
 System.out.println(sdt.getTitle());

 // Get the structured document tag or ranged tag by Title.
 sdt = doc.getRange().getStructuredDocumentTags().getByTitle("Alias4");
 System.out.println(sdt.getId());
 
```

**Returns:**
boolean - True, если этот экземпляр является диапазонным (многоразделным) структурированным тегом документа.
### isShowingPlaceholderText() {#isShowingPlaceholderText}
```
public abstract boolean isShowingPlaceholderText()
```


Указывает, следует ли интерпретировать содержимое этого **SDT** как содержащий текст-заполнитель (в отличие от обычного текста внутри SDT).

если установлено в true, это состояние будет возобновлено (показывая текст заполнителя) при открытии этого документа.

 **Examples:** 

Показывает, как использовать содержимое строительного блока в качестве пользовательского текста заполнителя для структурированного тега документа.

```

 Document doc = new Document();

 // Insert a plain text structured document tag of the "PlainText" type, which will function as a text box.
 // The contents that it will display by default are a "Click here to enter text." prompt.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // We can get the tag to display the contents of a building block instead of the default text.
 // First, add a building block with contents to the glossary document.
 GlossaryDocument glossaryDoc = doc.getGlossaryDocument();

 BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
 substituteBlock.setName("Custom Placeholder");
 substituteBlock.appendChild(new Section(glossaryDoc));
 substituteBlock.getFirstSection().appendChild(new Body(glossaryDoc));
 substituteBlock.getFirstSection().getBody().appendParagraph("Custom placeholder text.");

 glossaryDoc.appendChild(substituteBlock);

 // Then, use the structured document tag's "PlaceholderName" property to reference that building block by name.
 tag.setPlaceholderName("Custom Placeholder");

 // If "PlaceholderName" refers to an existing block in the parent document's glossary document,
 // we will be able to verify the building block via the "Placeholder" property.
 Assert.assertEquals(substituteBlock, tag.getPlaceholder());

 // Set the "IsShowingPlaceholderText" property to "true" to treat the
 // structured document tag's current contents as placeholder text.
 // This means that clicking on the text box in Microsoft Word will immediately highlight all the tag's contents.
 // Set the "IsShowingPlaceholderText" property to "false" to get the
 // structured document tag to treat its contents as text that a user has already entered.
 // Clicking on this text in Microsoft Word will place the blinking cursor at the clicked location.
 tag.isShowingPlaceholderText(isShowingPlaceholderText);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### isShowingPlaceholderText(boolean value) {#isShowingPlaceholderText-boolean}
```
public abstract void isShowingPlaceholderText(boolean value)
```


Указывает, следует ли интерпретировать содержимое этого **SDT** как содержащий текст-заполнитель (в отличие от обычного текста внутри SDT).

если установлено в true, это состояние будет возобновлено (показывая текст заполнителя) при открытии этого документа.

 **Examples:** 

Показывает, как использовать содержимое строительного блока в качестве пользовательского текста заполнителя для структурированного тега документа.

```

 Document doc = new Document();

 // Insert a plain text structured document tag of the "PlainText" type, which will function as a text box.
 // The contents that it will display by default are a "Click here to enter text." prompt.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // We can get the tag to display the contents of a building block instead of the default text.
 // First, add a building block with contents to the glossary document.
 GlossaryDocument glossaryDoc = doc.getGlossaryDocument();

 BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
 substituteBlock.setName("Custom Placeholder");
 substituteBlock.appendChild(new Section(glossaryDoc));
 substituteBlock.getFirstSection().appendChild(new Body(glossaryDoc));
 substituteBlock.getFirstSection().getBody().appendParagraph("Custom placeholder text.");

 glossaryDoc.appendChild(substituteBlock);

 // Then, use the structured document tag's "PlaceholderName" property to reference that building block by name.
 tag.setPlaceholderName("Custom Placeholder");

 // If "PlaceholderName" refers to an existing block in the parent document's glossary document,
 // we will be able to verify the building block via the "Placeholder" property.
 Assert.assertEquals(substituteBlock, tag.getPlaceholder());

 // Set the "IsShowingPlaceholderText" property to "true" to treat the
 // structured document tag's current contents as placeholder text.
 // This means that clicking on the text box in Microsoft Word will immediately highlight all the tag's contents.
 // Set the "IsShowingPlaceholderText" property to "false" to get the
 // structured document tag to treat its contents as text that a user has already entered.
 // Clicking on this text in Microsoft Word will place the blinking cursor at the clicked location.
 tag.isShowingPlaceholderText(isShowingPlaceholderText);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### removeSelfOnly() {#removeSelfOnly}
```
public abstract void removeSelfOnly()
```


Удаляет только сам узел SDT, но сохраняет его содержимое внутри дерева документа.

 **Examples:** 

Показывает, как удалить структурированный тег документа, но сохраняет содержимое внутри.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");

 // This collection provides a unified interface for accessing ranged and non-ranged structured tags.
 StructuredDocumentTagCollection sdts = doc.getRange().getStructuredDocumentTags();
 Assert.assertEquals(5, sdts.getCount());

 // Here we can get child nodes from the common interface of ranged and non-ranged structured tags.
 for (IStructuredDocumentTag sdt : sdts)
     if (sdt.getChildNodes(NodeType.ANY, false).getCount() > 0)
         sdt.removeSelfOnly();

 sdts = doc.getRange().getStructuredDocumentTags();
 Assert.assertEquals(0, sdts.getCount());
 
```

### setAppearance(int value) {#setAppearance-int}
```
public abstract void setAppearance(int value)
```


Устанавливает внешний вид структурированного тега документа.

 **Examples:** 

Показывает, как отобразить тег вокруг содержимого.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");
 StructuredDocumentTagRangeStart tag = (StructuredDocumentTagRangeStart) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, true);

 if (tag.getAppearance() == SdtAppearance.HIDDEN)
     tag.setAppearance(SdtAppearance.TAGS);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Внешний вид структурированного тега документа. Значение должно быть одной из констант [SdtAppearance](../../com.aspose.words/sdtappearance/). |

### setColor(Color value) {#setColor-java.awt.Color}
```
public abstract void setColor(Color value)
```


Устанавливает цвет структурированного тега документа.

 **Examples:** 

Показывает, как получить свойства многоразделных структурированных тегов документа.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.awt.Color | Цвет структурированного тега документа. |

### setLockContentControl(boolean value) {#setLockContentControl-boolean}
```
public abstract void setLockContentControl(boolean value)
```


Если установить в true, это свойство запретит пользователю удалять этот **SDT**.

 **Examples:** 

Показывает, как применить ограничения редактирования к структурированным тегам документа.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a plain text structured document tag, which acts as a text box that prompts the user to fill it in.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the "LockContents" property to "true" to prohibit the user from editing this text box's contents.
 tag.setLockContents(true);
 builder.write("The contents of this structured document tag cannot be edited: ");
 builder.insertNode(tag);

 tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the "LockContentControl" property to "true" to prohibit the user from
 // deleting this structured document tag manually in Microsoft Word.
 tag.setLockContentControl(true);

 builder.insertParagraph();
 builder.write("This structured document tag cannot be deleted but its contents can be edited: ");
 builder.insertNode(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.Lock.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setLockContents(boolean value) {#setLockContents-boolean}
```
public abstract void setLockContents(boolean value)
```


Если установить в true, это свойство запретит пользователю изменять содержимое этого **SDT**.

 **Examples:** 

Показывает, как применить ограничения редактирования к структурированным тегам документа.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a plain text structured document tag, which acts as a text box that prompts the user to fill it in.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the "LockContents" property to "true" to prohibit the user from editing this text box's contents.
 tag.setLockContents(true);
 builder.write("The contents of this structured document tag cannot be edited: ");
 builder.insertNode(tag);

 tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the "LockContentControl" property to "true" to prohibit the user from
 // deleting this structured document tag manually in Microsoft Word.
 tag.setLockContentControl(true);

 builder.insertParagraph();
 builder.write("This structured document tag cannot be deleted but its contents can be edited: ");
 builder.insertNode(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.Lock.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setPlaceholderName(String value) {#setPlaceholderName-java.lang.String}
```
public abstract void setPlaceholderName(String value)
```


Получает или задает имя [BuildingBlock](../../com.aspose.words/buildingblock/), содержащего текст-заполнитель.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Соответствующее значение java.lang.String. |

### setTag(String value) {#setTag-java.lang.String}
```
public abstract void setTag(String value)
```


Указывает тег, связанный с текущим узлом SDT. Не может быть null.

 **Examples:** 

Показывает, как создать структурированный тег документа в обычном текстовом поле и изменить его внешний вид.

```

 Document doc = new Document();

 // Create a structured document tag that will contain plain text.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.INLINE);

 // Set the title and color of the frame that appears when you mouse over the structured document tag in Microsoft Word.
 tag.setTitle("My plain text");
 tag.setColor(Color.MAGENTA);

 // Set a tag for this structured document tag, which is obtainable
 // as an XML element named "tag", with the string below in its "@val" attribute.
 tag.setTag("MyPlainTextSDT");

 // Every structured document tag has a random unique ID.
 Assert.assertTrue(tag.getId() > 0);

 // Set the font for the text inside the structured document tag.
 tag.getContentsFont().setName("Arial");

 // Set the font for the text at the end of the structured document tag.
 // Any text that we type in the document body after moving out of the tag with arrow keys will use this font.
 tag.getEndCharacterFont().setName("Arial Black");

 // By default, this is false and pressing enter while inside a structured document tag does nothing.
 // When set to true, our structured document tag can have multiple lines.

 // Set the "Multiline" property to "false" to only allow the contents
 // of this structured document tag to span a single line.
 // Set the "Multiline" property to "true" to allow the tag to contain multiple lines of content.
 tag.setMultiline(true);

 // Set the "Appearance" property to "SdtAppearance.Tags" to show tags around content.
 // By default structured document tag shows as BoundingBox.
 tag.setAppearance(SdtAppearance.TAGS);

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(tag);

 // Insert a clone of our structured document tag in a new paragraph.
 StructuredDocumentTag tagClone = (StructuredDocumentTag) tag.deepClone(true);
 builder.insertParagraph();
 builder.insertNode(tagClone);

 // Use the "RemoveSelfOnly" method to remove a structured document tag, while keeping its contents in the document.
 tagClone.removeSelfOnly();

 doc.save(getArtifactsDir() + "StructuredDocumentTag.PlainText.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Соответствующее значение java.lang.String. |

### setTitle(String value) {#setTitle-java.lang.String}
```
public abstract void setTitle(String value)
```


Указывает дружественное имя, связанное с этим **SDT**. Не может быть null.

 **Examples:** 

Показывает, как получить структурированный тег документа.

```

 Document doc = new Document(getMyDir() + "Structured document tags by id.docx");

 // Get the structured document tag by Id.
 IStructuredDocumentTag sdt = doc.getRange().getStructuredDocumentTags().getById(1160505028);
 System.out.println(sdt.isMultiSection());
 System.out.println(sdt.getTitle());

 // Get the structured document tag or ranged tag by Title.
 sdt = doc.getRange().getStructuredDocumentTags().getByTitle("Alias4");
 System.out.println(sdt.getId());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Соответствующее значение java.lang.String. |

