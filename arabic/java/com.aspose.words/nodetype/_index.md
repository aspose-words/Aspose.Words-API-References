---
title: "NodeType"
linktitle: "NodeType"
second_title: "Aspose.Words لـ Java"
description: "يحدد نوع عقدة مستند Word في Java."
type: docs
weight: 483
url: /ar/java/com.aspose.words/nodetype/
---

**Inheritance:**
java.lang.Object
```
public class NodeType
```

يحدد نوع عقدة مستند Word.

 **Examples:** 

يوضح كيفية التجوال عبر مجموعة العقد الفرعية لعقدة مركبة.

```

 Document doc = new Document();

 // Add two runs and one shape as child nodes to the first paragraph of this document.
 Paragraph paragraph = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);
 paragraph.appendChild(new Run(doc, "Hello world! "));

 Shape shape = new Shape(doc, ShapeType.RECTANGLE);
 shape.setWidth(200.0);
 shape.setHeight(200.0);
 // Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
 shape.setCustomNodeId(100);
 shape.setWrapType(WrapType.INLINE);
 paragraph.appendChild(shape);

 paragraph.appendChild(new Run(doc, "Hello again!"));

 // Iterate through the paragraph's collection of immediate children,
 // and print any runs or shapes that we find within.
 NodeCollection children = paragraph.getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, false).getCount());

 for (Node child : (Iterable) children)
     switch (child.getNodeType()) {
         case NodeType.RUN:
             System.out.println("Run contents:");
             System.out.println(MessageFormat.format("\t\"{0}\"", child.getText().trim()));
             break;
         case NodeType.SHAPE:
             Shape childShape = (Shape)child;
             System.out.println("Shape:");
             System.out.println(MessageFormat.format("\t{0}, {1}x{2}", childShape.getShapeType(), childShape.getWidth(), childShape.getHeight()));
             break;
     }
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [ANY](#ANY) | يشير إلى جميع أنواع العقد. |
| [BODY](#BODY) | كائن [Body](../../com.aspose.words/body/) يحتوي على النص الرئيسي لقسم (قصة النص الرئيسي). |
| [BOOKMARK_END](#BOOKMARK-END) | نهاية علامة مرجعية. |
| [BOOKMARK_START](#BOOKMARK-START) | بداية علامة مرجعية. |
| [BUILDING_BLOCK](#BUILDING-BLOCK) | كتلة بناء داخل مستند مسرد (مثال |
| [CELL](#CELL) | خلية من صف جدول. |
| [COMMENT](#COMMENT) | تعليق في مستند Word. |
| [COMMENT_RANGE_END](#COMMENT-RANGE-END) | عقدة علامة تمثل نهاية نطاق مُعلق. |
| [COMMENT_RANGE_START](#COMMENT-RANGE-START) | عقدة علامة تمثل بداية نطاق مُعلق. |
| [DOCUMENT](#DOCUMENT) | كائن [Document](../../com.aspose.words/document/) الذي، كجذر شجرة المستند، يوفر الوصول إلى مستند Word بالكامل. |
| [EDITABLE_RANGE_END](#EDITABLE-RANGE-END) | نهاية نطاق قابل للتحرير. |
| [EDITABLE_RANGE_START](#EDITABLE-RANGE-START) | بداية نطاق قابل للتحرير. |
| [FIELD_END](#FIELD-END) | حرف خاص يحدد نهاية حقل Word. |
| [FIELD_SEPARATOR](#FIELD-SEPARATOR) | حرف خاص يفصل شفرة الحقل عن نتيجة الحقل. |
| [FIELD_START](#FIELD-START) | حرف خاص يحدد بداية حقل Word. |
| [FOOTNOTE](#FOOTNOTE) | حاشية سفلية أو حاشية نهائية في مستند Word. |
| [FORM_FIELD](#FORM-FIELD) | حقل نموذج. |
| [GLOSSARY_DOCUMENT](#GLOSSARY-DOCUMENT) | مستند مسرد داخل المستند الرئيسي. |
| [GROUP_SHAPE](#GROUP-SHAPE) | مجموعة من الأشكال، الصور، كائنات OLE أو أشكال مجموعة أخرى. |
| [HEADER_FOOTER](#HEADER-FOOTER) | كائن [HeaderFooter](../../com.aspose.words/headerfooter/) يحتوي على نص رأس أو تذييل معين داخل قسم. |
| [MOVE_FROM_RANGE_END](#MOVE-FROM-RANGE-END) | نهاية نطاق MoveFrom. |
| [MOVE_FROM_RANGE_START](#MOVE-FROM-RANGE-START) | بداية نطاق MoveFrom. |
| [MOVE_TO_RANGE_END](#MOVE-TO-RANGE-END) | نهاية نطاق MoveTo. |
| [MOVE_TO_RANGE_START](#MOVE-TO-RANGE-START) | بداية نطاق MoveTo. |
| [NULL](#NULL) | محجوز للاستخدام الداخلي من قبل Aspose.Words. |
| [OFFICE_MATH](#OFFICE-MATH) | كائن Office Math. |
| [PARAGRAPH](#PARAGRAPH) | فقرة نصية. |
| [ROW](#ROW) | صف من جدول. |
| [RUN](#RUN) | مقطع نصي. |
| [SECTION](#SECTION) | كائن [Section](../../com.aspose.words/section/) يتطابق مع قسم واحد في مستند Word. |
| [SHAPE](#SHAPE) | كائن رسم، مثل شكل OfficeArt أو صورة أو كائن OLE. |
| [SMART_TAG](#SMART-TAG) | علامة ذكية حول بنية (أو أكثر) مضمَّنة (مقاطع، صور، حقول، إلخ) داخل فقرة. |
| [SPECIAL_CHAR](#SPECIAL-CHAR) | حرف خاص ليس أحد الأنواع المحددة الأخرى للأحرف الخاصة. |
| [STRUCTURED_DOCUMENT_TAG](#STRUCTURED-DOCUMENT-TAG) | يسمح بتعريف معلومات مخصصة للعميل وطريقة عرضها. |
| [STRUCTURED_DOCUMENT_TAG_RANGE_END](#STRUCTURED-DOCUMENT-TAG-RANGE-END) | نهاية **ranged** لعلامة مستند منظم تقبل محتوى متعدد الأقسام. |
| [STRUCTURED_DOCUMENT_TAG_RANGE_START](#STRUCTURED-DOCUMENT-TAG-RANGE-START) | بداية **ranged** لعلامة مستند منظم تقبل محتوى متعدد الأقسام. |
| [SUB_DOCUMENT](#SUB-DOCUMENT) | عقدة مستند فرعي هي رابط إلى مستند آخر. |
| [SYSTEM](#SYSTEM) | محجوز للاستخدام الداخلي من قبل Aspose.Words. |
| [TABLE](#TABLE) | كائن [Table](../../com.aspose.words/table/) يمثل جدولًا في مستند Word. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String nodeTypeName)](#fromName-java.lang.String) |  |
| [getName(int nodeType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int nodeType)](#toString-int) |  |
### ANY {#ANY}
```
public static int ANY
```


يشير إلى جميع أنواع العقد. يسمح باختيار جميع العناصر الفرعية.

### BODY {#BODY}
```
public static int BODY
```


كائن [Body](../../com.aspose.words/body/) يحتوي على النص الرئيسي لقسم (قصة النص الرئيسي).

يمكن لعقدة [Body](../../com.aspose.words/body/) أن تحتوي على عقد [Paragraph](../../com.aspose.words/paragraph/) و[Table](../../com.aspose.words/table/).

### BOOKMARK_END {#BOOKMARK-END}
```
public static int BOOKMARK_END
```


نهاية علامة مرجعية.

### BOOKMARK_START {#BOOKMARK-START}
```
public static int BOOKMARK_START
```


بداية علامة مرجعية.

### BUILDING_BLOCK {#BUILDING-BLOCK}
```
public static int BUILDING_BLOCK
```


كتلة بناء داخل مستند مسرد (مثال: إدخال مستند مسرد).

### CELL {#CELL}
```
public static int CELL
```


خلية من صف جدول.

يمكن لعقدة [Cell](../../com.aspose.words/cell/) أن تحتوي على عقد [Paragraph](../../com.aspose.words/paragraph/) و[Table](../../com.aspose.words/table/).

### COMMENT {#COMMENT}
```
public static int COMMENT
```


تعليق في مستند Word.

يمكن لعقدة [Comment](../../com.aspose.words/comment/) أن تحتوي على عقد [Paragraph](../../com.aspose.words/paragraph/) و[Table](../../com.aspose.words/table/).

### COMMENT_RANGE_END {#COMMENT-RANGE-END}
```
public static int COMMENT_RANGE_END
```


عقدة علامة تمثل نهاية نطاق مُعلق.

### COMMENT_RANGE_START {#COMMENT-RANGE-START}
```
public static int COMMENT_RANGE_START
```


عقدة علامة تمثل بداية نطاق مُعلق.

### DOCUMENT {#DOCUMENT}
```
public static int DOCUMENT
```


كائن [Document](../../com.aspose.words/document/) الذي، كجذر شجرة المستند، يوفر الوصول إلى مستند Word بالكامل.

يمكن لعقدة [Document](../../com.aspose.words/document/) أن تحتوي على عقد [Section](../../com.aspose.words/section/).

### EDITABLE_RANGE_END {#EDITABLE-RANGE-END}
```
public static int EDITABLE_RANGE_END
```


نهاية نطاق قابل للتحرير.

### EDITABLE_RANGE_START {#EDITABLE-RANGE-START}
```
public static int EDITABLE_RANGE_START
```


بداية نطاق قابل للتحرير.

### FIELD_END {#FIELD-END}
```
public static int FIELD_END
```


حرف خاص يحدد نهاية حقل Word.

### FIELD_SEPARATOR {#FIELD-SEPARATOR}
```
public static int FIELD_SEPARATOR
```


حرف خاص يفصل شفرة الحقل عن نتيجة الحقل.

### FIELD_START {#FIELD-START}
```
public static int FIELD_START
```


حرف خاص يحدد بداية حقل Word.

### FOOTNOTE {#FOOTNOTE}
```
public static int FOOTNOTE
```


حاشية سفلية أو حاشية نهائية في مستند Word.

يمكن لعقدة [Footnote](../../com.aspose.words/footnote/) أن تحتوي على عقد [Paragraph](../../com.aspose.words/paragraph/) و[Table](../../com.aspose.words/table/).

### FORM_FIELD {#FORM-FIELD}
```
public static int FORM_FIELD
```


حقل نموذج.

### GLOSSARY_DOCUMENT {#GLOSSARY-DOCUMENT}
```
public static int GLOSSARY_DOCUMENT
```


مستند مسرد داخل المستند الرئيسي.

### GROUP_SHAPE {#GROUP-SHAPE}
```
public static int GROUP_SHAPE
```


مجموعة من الأشكال، الصور، كائنات OLE أو أشكال مجموعة أخرى.

يمكن لعقدة [GroupShape](../../com.aspose.words/groupshape/) أن تحتوي على عقد أخرى من نوع [Shape](../../com.aspose.words/shape/) و[GroupShape](../../com.aspose.words/groupshape/).

### HEADER_FOOTER {#HEADER-FOOTER}
```
public static int HEADER_FOOTER
```


كائن [HeaderFooter](../../com.aspose.words/headerfooter/) يحتوي على نص رأس أو تذييل معين داخل قسم.

يمكن لعقدة [HeaderFooter](../../com.aspose.words/headerfooter/) أن تحتوي على عقد [Paragraph](../../com.aspose.words/paragraph/) و[Table](../../com.aspose.words/table/).

### MOVE_FROM_RANGE_END {#MOVE-FROM-RANGE-END}
```
public static int MOVE_FROM_RANGE_END
```


نهاية نطاق MoveFrom.

### MOVE_FROM_RANGE_START {#MOVE-FROM-RANGE-START}
```
public static int MOVE_FROM_RANGE_START
```


بداية نطاق MoveFrom.

### MOVE_TO_RANGE_END {#MOVE-TO-RANGE-END}
```
public static int MOVE_TO_RANGE_END
```


نهاية نطاق MoveTo.

### MOVE_TO_RANGE_START {#MOVE-TO-RANGE-START}
```
public static int MOVE_TO_RANGE_START
```


بداية نطاق MoveTo.

### NULL {#NULL}
```
public static int NULL
```


محجوز للاستخدام الداخلي من قبل Aspose.Words.

### OFFICE_MATH {#OFFICE-MATH}
```
public static int OFFICE_MATH
```


كائن Office Math. يمكن أن يكون معادلة أو دالة أو مصفوفة أو أحد الكائنات الرياضية الأخرى. يمكن أن يكون مجموعة من الكائنات الرياضية ويمكن أيضًا أن يحتوي على بعض الكائنات غير الرياضية مثل مقاطع النص.

### PARAGRAPH {#PARAGRAPH}
```
public static int PARAGRAPH
```


فقرة نصية.

عقدة [Paragraph](../../com.aspose.words/paragraph/) هي حاوية لعناصر المستوى الداخلي مثل [Run](../../com.aspose.words/run/), [FieldStart](../../com.aspose.words/fieldstart/), [FieldSeparator](../../com.aspose.words/fieldseparator/), [FieldEnd](../../com.aspose.words/fieldend/), [FormField](../../com.aspose.words/formfield/), [Shape](../../com.aspose.words/shape/), [GroupShape](../../com.aspose.words/groupshape/), [Footnote](../../com.aspose.words/footnote/), [Comment](../../com.aspose.words/comment/), [SpecialChar](../../com.aspose.words/specialchar/), بالإضافة إلى [BookmarkStart](../../com.aspose.words/bookmarkstart/) و[BookmarkEnd](../../com.aspose.words/bookmarkend/).

### ROW {#ROW}
```
public static int ROW
```


صف من جدول.

يمكن لعقدة [Row](../../com.aspose.words/row/) أن تحتوي على عقد [Cell](../../com.aspose.words/cell/).

### RUN {#RUN}
```
public static int RUN
```


مقطع نصي.

### SECTION {#SECTION}
```
public static int SECTION
```


كائن [Section](../../com.aspose.words/section/) يتطابق مع قسم واحد في مستند Word.

يمكن لعقدة [Section](../../com.aspose.words/section/) أن تحتوي على عقد [Body](../../com.aspose.words/body/) و[HeaderFooter](../../com.aspose.words/headerfooter/).

### SHAPE {#SHAPE}
```
public static int SHAPE
```


كائن رسم، مثل شكل OfficeArt أو صورة أو كائن OLE.

يمكن لعقدة [Shape](../../com.aspose.words/shape/) أن تحتوي على عقد [Paragraph](../../com.aspose.words/paragraph/) و[Table](../../com.aspose.words/table/).

### SMART_TAG {#SMART-TAG}
```
public static int SMART_TAG
```


علامة ذكية حول بنية (أو أكثر) مضمَّنة (مقاطع، صور، حقول، إلخ) داخل فقرة.

### SPECIAL_CHAR {#SPECIAL-CHAR}
```
public static int SPECIAL_CHAR
```


حرف خاص ليس أحد الأنواع المحددة الأخرى للأحرف الخاصة.

### STRUCTURED_DOCUMENT_TAG {#STRUCTURED-DOCUMENT-TAG}
```
public static int STRUCTURED_DOCUMENT_TAG
```


يسمح بتعريف معلومات مخصصة للعميل وطريقة عرضها.

### STRUCTURED_DOCUMENT_TAG_RANGE_END {#STRUCTURED-DOCUMENT-TAG-RANGE-END}
```
public static int STRUCTURED_DOCUMENT_TAG_RANGE_END
```


نهاية **ranged** لعلامة مستند منظم تقبل محتوى متعدد الأقسام.

### STRUCTURED_DOCUMENT_TAG_RANGE_START {#STRUCTURED-DOCUMENT-TAG-RANGE-START}
```
public static int STRUCTURED_DOCUMENT_TAG_RANGE_START
```


بداية **ranged** لعلامة مستند منظم تقبل محتوى متعدد الأقسام.

### SUB_DOCUMENT {#SUB-DOCUMENT}
```
public static int SUB_DOCUMENT
```


عقدة مستند فرعي هي رابط إلى مستند آخر.

### SYSTEM {#SYSTEM}
```
public static int SYSTEM
```


محجوز للاستخدام الداخلي من قبل Aspose.Words.

### TABLE {#TABLE}
```
public static int TABLE
```


كائن [Table](../../com.aspose.words/table/) يمثل جدولًا في مستند Word.

يمكن لعقدة [Table](../../com.aspose.words/table/) أن تحتوي على عقد [Row](../../com.aspose.words/row/).

### length {#length}
```
public static int length
```


### fromName(String nodeTypeName) {#fromName-java.lang.String}
```
public static int fromName(String nodeTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| nodeTypeName | java.lang.String |  |

**Returns:**
int
### getName(int nodeType) {#getName-int}
```
public static String getName(int nodeType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int nodeType) {#toString-int}
```
public static String toString(int nodeType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
