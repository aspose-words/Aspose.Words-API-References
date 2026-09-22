---
title: "IStructuredDocumentTag"
linktitle: "IStructuredDocumentTag"
second_title: "Aspose.Words لـ Java"
description: "واجهة لتحديد بيانات مشتركة لـ StructuredDocumentTag و StructuredDocumentTagRangeStart في Java."
type: docs
weight: 785
url: /ar/java/com.aspose.words/istructureddocumenttag/
---
```
public interface IStructuredDocumentTag
```

واجهة لتحديد بيانات مشتركة لـ [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) و [StructuredDocumentTagRangeStart](../../com.aspose.words/structureddocumenttagrangestart/).

 **Examples:** 

يوضح كيفية إزالة علامة المستند المهيكلة، مع الحفاظ على المحتوى داخلها.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getAppearance()](#getAppearance) | يحصل على مظهر علامة المستند المهيكلة. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean) |  |
| [getColor()](#getColor) | يحصل على لون علامة المستند المهيكلة. |
| [getId()](#getId) | يحدد معرفًا رقميًا فريدًا للقراءة فقط ومستمر لهذا **SDT**. |
| [getLevel()](#getLevel) | يحصل على المستوى الذي يظهر فيه هذا **SDT** في شجرة المستند. |
| [getLockContentControl()](#getLockContentControl) | عند تعيينه إلى true، سيمنع هذا الخصائص المستخدم من حذف هذا **SDT**. |
| [getLockContents()](#getLockContents) | عند تعيينه إلى true، سيمنع هذا الخصائص المستخدم من تعديل محتويات هذا **SDT**. |
| [getNode()](#getNode) | يعيد كائن Node الذي يطبق هذه الواجهة. |
| [getPlaceholder()](#getPlaceholder) | يحصل على الـ [BuildingBlock](../../com.aspose.words/buildingblock/) الذي يحتوي على نص العنصر النائب الذي يجب عرضه عندما تكون محتويات تشغيل الـ SDT فارغة، أو عندما يكون عنصر XML المرتبط فارغًا كما هو محدد عبر عنصر [getXmlMapping()](../../com.aspose.words/istructureddocumenttag/\#getXmlMapping) أو عندما يكون عنصر [isShowingPlaceholderText()](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText-boolean) صحيح. |
| [getPlaceholderName()](#getPlaceholderName) | يحصل أو يحدد اسم الـ [BuildingBlock](../../com.aspose.words/buildingblock/) الذي يحتوي على نص العنصر النائب. |
| [getSdtType()](#getSdtType) | يحصل على نوع هذه **Structured document tag**. |
| [getTag()](#getTag) | يحدد علامة مرتبطة بعقدة الـ SDT الحالية. |
| [getTitle()](#getTitle) | يحدد الاسم الودي المرتبط بهذا **SDT**. |
| [getWordOpenXML()](#getWordOpenXML) | يحصل على سلسلة تمثل XML الموجود داخل العقدة بتنسيق [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC). |
| [getXmlMapping()](#getXmlMapping) | يحصل على كائن يمثل ربط هذه علامة المستند المهيكلة ببيانات XML في جزء XML مخصص للمستند الحالي. |
| [isMultiSection()](#isMultiSection) | يعيد true إذا كانت هذه الحالة علامة مستند مهيكلة ذات نطاق (متعددة الأقسام). |
| [isShowingPlaceholderText()](#isShowingPlaceholderText) | يحدد ما إذا كان محتوى هذا **SDT** يجب تفسيره كاحتواء نص عنصر نائب (بدلاً من محتويات نصية عادية داخل الـ SDT). |
| [isShowingPlaceholderText(boolean value)](#isShowingPlaceholderText-boolean) | يحدد ما إذا كان محتوى هذا **SDT** يجب تفسيره كاحتواء نص عنصر نائب (بدلاً من محتويات نصية عادية داخل الـ SDT). |
| [removeSelfOnly()](#removeSelfOnly) | يزيل عقدة الـ SDT هذه فقط، مع الحفاظ على محتواها داخل شجرة المستند. |
| [setAppearance(int value)](#setAppearance-int) | يضبط مظهر علامة المستند المهيكلة. |
| [setColor(Color value)](#setColor-java.awt.Color) | يضبط لون علامة المستند المهيكلة. |
| [setLockContentControl(boolean value)](#setLockContentControl-boolean) | عند تعيينه إلى true، سيمنع هذا الخصائص المستخدم من حذف هذا **SDT**. |
| [setLockContents(boolean value)](#setLockContents-boolean) | عند تعيينه إلى true، سيمنع هذا الخصائص المستخدم من تعديل محتويات هذا **SDT**. |
| [setPlaceholderName(String value)](#setPlaceholderName-java.lang.String) | يحصل أو يحدد اسم الـ [BuildingBlock](../../com.aspose.words/buildingblock/) الذي يحتوي على نص العنصر النائب. |
| [setTag(String value)](#setTag-java.lang.String) | يحدد علامة مرتبطة بعقدة الـ SDT الحالية. |
| [setTitle(String value)](#setTitle-java.lang.String) | يحدد الاسم الودي المرتبط بهذا **SDT**. |
### getAppearance() {#getAppearance}
```
public abstract int getAppearance()
```


يحصل على مظهر علامة المستند المهيكلة.

 **Examples:** 

يوضح كيفية إظهار العلامة حول المحتوى.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");
 StructuredDocumentTagRangeStart tag = (StructuredDocumentTagRangeStart) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, true);

 if (tag.getAppearance() == SdtAppearance.HIDDEN)
     tag.setAppearance(SdtAppearance.TAGS);
 
```

**Returns:**
int - مظهر علامة المستند المهيكلة. القيمة المعادة هي واحدة من ثوابت [SdtAppearance](../../com.aspose.words/sdtappearance/).
### getChildNodes(int nodeType, boolean isDeep) {#getChildNodes-int-boolean}
```
public abstract NodeCollection getChildNodes(int nodeType, boolean isDeep)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| nodeType | int |  |
| isDeep | boolean |  |

**Returns:**
[NodeCollection](../../com.aspose.words/nodecollection/)
### getColor() {#getColor}
```
public abstract Color getColor()
```


يحصل على لون علامة المستند المهيكلة.

 **Examples:** 

يوضح كيفية الحصول على خصائص علامات المستند المهيكلة متعددة الأقسام.

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
java.awt.Color - لون علامة المستند المهيكلة.
### getId() {#getId}
```
public abstract int getId()
```


يحدد معرفًا رقميًا فريدًا للقراءة فقط ومستمر لهذا **SDT**.

 **Examples:** 

يوضح كيفية الحصول على خصائص علامات المستند المهيكلة متعددة الأقسام.

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
int - القيمة المقابلة  int .
### getLevel() {#getLevel}
```
public abstract int getLevel()
```


يحصل على المستوى الذي يظهر فيه هذا **SDT** في شجرة المستند.

 **Examples:** 

يوضح كيفية الحصول على خصائص علامات المستند المهيكلة متعددة الأقسام.

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
int - المستوى الذي يحدث فيه هذا **SDT** في شجرة المستند. القيمة المرجعة هي واحدة من ثوابت [MarkupLevel](../../com.aspose.words/markuplevel/).
### getLockContentControl() {#getLockContentControl}
```
public abstract boolean getLockContentControl()
```


عند تعيينه إلى true، سيمنع هذا الخصائص المستخدم من حذف هذا **SDT**.

 **Examples:** 

يظهر كيفية تطبيق قيود التحرير على علامات المستند المهيكلة.

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
boolean - القيمة المنطقية المقابلة.
### getLockContents() {#getLockContents}
```
public abstract boolean getLockContents()
```


عند تعيينه إلى true، سيمنع هذا الخصائص المستخدم من تعديل محتويات هذا **SDT**.

 **Examples:** 

يظهر كيفية تطبيق قيود التحرير على علامات المستند المهيكلة.

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
boolean - القيمة المنطقية المقابلة.
### getNode() {#getNode}
```
public abstract Node getNode()
```


يعيد كائن Node الذي يطبق هذه الواجهة.

**Returns:**
[Node](../../com.aspose.words/node/) - Node object that implements this interface.
### getPlaceholder() {#getPlaceholder}
```
public abstract BuildingBlock getPlaceholder()
```


يحصل على الـ [BuildingBlock](../../com.aspose.words/buildingblock/) الذي يحتوي على نص العنصر النائب الذي يجب عرضه عندما تكون محتويات تشغيل الـ SDT فارغة، أو عندما يكون عنصر XML المرتبط فارغًا كما هو محدد عبر عنصر [getXmlMapping()](../../com.aspose.words/istructureddocumenttag/\#getXmlMapping) أو عندما يكون عنصر [isShowingPlaceholderText()](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/istructureddocumenttag/\#isShowingPlaceholderText-boolean) صحيح.

 **Remarks:** 

يمكن أن تكون null، مما يعني أن العنصر النائب غير قابل للتطبيق على هذا Sdt.

 **Examples:** 

يظهر كيفية استخدام محتويات كتلة بناء كنص عنصر نائب مخصص لعلامة المستند المهيكلة.

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


يحصل أو يحدد اسم الـ [BuildingBlock](../../com.aspose.words/buildingblock/) الذي يحتوي على نص العنصر النائب.

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getSdtType() {#getSdtType}
```
public abstract int getSdtType()
```


يحصل على نوع هذه **Structured document tag**.

**Returns:**
int - نوع هذه **Structured document tag**. القيمة المرجعة هي واحدة من ثوابت [SdtType](../../com.aspose.words/sdttype/).
### getTag() {#getTag}
```
public abstract String getTag()
```


يحدد علامة مرتبطة بعقدة SDT الحالية. لا يمكن أن تكون null.

 **Examples:** 

يظهر كيفية إنشاء علامة مستند مهيكلة في مربع نص عادي وتعديل مظهرها.

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
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getTitle() {#getTitle}
```
public abstract String getTitle()
```


يحدد الاسم الودي المرتبط بهذا **SDT**. لا يمكن أن يكون null.

 **Examples:** 

يظهر كيفية الحصول على علامة المستند المهيكلة.

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
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getWordOpenXML() {#getWordOpenXML}
```
public abstract String getWordOpenXML()
```


يحصل على سلسلة تمثل XML الموجود داخل العقدة بتنسيق [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC).

 **Examples:** 

يظهر كيفية الحصول على XML الموجود داخل العقدة بتنسيق FlatOpc.

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
java.lang.String - سلسلة تمثل XML الموجود داخل العقدة بتنسيق [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC).
### getXmlMapping() {#getXmlMapping}
```
public abstract XmlMapping getXmlMapping()
```


يحصل على كائن يمثل ربط هذه علامة المستند المهيكلة ببيانات XML في جزء XML مخصص للمستند الحالي.

 **Remarks:** 

يمكنك استخدام طريقة [XmlMapping.setMapping(com.aspose.words.CustomXmlPart, java.lang.String, java.lang.String)](../../com.aspose.words/xmlmapping/\#setMapping-com.aspose.words.CustomXmlPart--java.lang.String--java.lang.String) لهذا الكائن لربط علامة المستند المهيكلة ببيانات XML.

 **Examples:** 

يوضح كيفية إنشاء علامة مستند مُنظم ببيانات XML مخصصة.

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


يعيد true إذا كانت هذه الحالة علامة مستند مهيكلة ذات نطاق (متعددة الأقسام).

 **Examples:** 

يظهر كيفية الحصول على علامة المستند المهيكلة.

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
boolean - صحيح إذا كان هذا المثال علامة مستند مهيكلة بنطاق (متعدد الأقسام).
### isShowingPlaceholderText() {#isShowingPlaceholderText}
```
public abstract boolean isShowingPlaceholderText()
```


يحدد ما إذا كان محتوى هذا **SDT** يجب تفسيره كاحتواء نص عنصر نائب (بدلاً من محتويات نصية عادية داخل الـ SDT).

إذا تم تعيينه إلى true، ستستأنف هذه الحالة (عرض نص العنصر النائب) عند فتح المستند.

 **Examples:** 

يظهر كيفية استخدام محتويات كتلة بناء كنص عنصر نائب مخصص لعلامة المستند المهيكلة.

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
boolean - القيمة المنطقية المقابلة.
### isShowingPlaceholderText(boolean value) {#isShowingPlaceholderText-boolean}
```
public abstract void isShowingPlaceholderText(boolean value)
```


يحدد ما إذا كان محتوى هذا **SDT** يجب تفسيره كاحتواء نص عنصر نائب (بدلاً من محتويات نصية عادية داخل الـ SDT).

إذا تم تعيينه إلى true، ستستأنف هذه الحالة (عرض نص العنصر النائب) عند فتح المستند.

 **Examples:** 

يظهر كيفية استخدام محتويات كتلة بناء كنص عنصر نائب مخصص لعلامة المستند المهيكلة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### removeSelfOnly() {#removeSelfOnly}
```
public abstract void removeSelfOnly()
```


يزيل عقدة الـ SDT هذه فقط، مع الحفاظ على محتواها داخل شجرة المستند.

 **Examples:** 

يوضح كيفية إزالة علامة المستند المهيكلة، مع الحفاظ على المحتوى داخلها.

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


يضبط مظهر علامة المستند المهيكلة.

 **Examples:** 

يوضح كيفية إظهار العلامة حول المحتوى.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");
 StructuredDocumentTagRangeStart tag = (StructuredDocumentTagRangeStart) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, true);

 if (tag.getAppearance() == SdtAppearance.HIDDEN)
     tag.setAppearance(SdtAppearance.TAGS);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | مظهر علامة المستند المهيكلة. يجب أن تكون القيمة واحدة من ثوابت [SdtAppearance](../../com.aspose.words/sdtappearance/). |

### setColor(Color value) {#setColor-java.awt.Color}
```
public abstract void setColor(Color value)
```


يضبط لون علامة المستند المهيكلة.

 **Examples:** 

يوضح كيفية الحصول على خصائص علامات المستند المهيكلة متعددة الأقسام.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | لون علامة المستند المهيكلة. |

### setLockContentControl(boolean value) {#setLockContentControl-boolean}
```
public abstract void setLockContentControl(boolean value)
```


عند تعيينه إلى true، سيمنع هذا الخصائص المستخدم من حذف هذا **SDT**.

 **Examples:** 

يظهر كيفية تطبيق قيود التحرير على علامات المستند المهيكلة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setLockContents(boolean value) {#setLockContents-boolean}
```
public abstract void setLockContents(boolean value)
```


عند تعيينه إلى true، سيمنع هذا الخصائص المستخدم من تعديل محتويات هذا **SDT**.

 **Examples:** 

يظهر كيفية تطبيق قيود التحرير على علامات المستند المهيكلة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setPlaceholderName(String value) {#setPlaceholderName-java.lang.String}
```
public abstract void setPlaceholderName(String value)
```


يحصل أو يحدد اسم الـ [BuildingBlock](../../com.aspose.words/buildingblock/) الذي يحتوي على نص العنصر النائب.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

### setTag(String value) {#setTag-java.lang.String}
```
public abstract void setTag(String value)
```


يحدد علامة مرتبطة بعقدة SDT الحالية. لا يمكن أن تكون null.

 **Examples:** 

يظهر كيفية إنشاء علامة مستند مهيكلة في مربع نص عادي وتعديل مظهرها.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

### setTitle(String value) {#setTitle-java.lang.String}
```
public abstract void setTitle(String value)
```


يحدد الاسم الودي المرتبط بهذا **SDT**. لا يمكن أن يكون null.

 **Examples:** 

يظهر كيفية الحصول على علامة المستند المهيكلة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

