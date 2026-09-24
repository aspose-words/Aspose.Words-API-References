---
title: "NodeType"
linktitle: "NodeType"
second_title: "Aspose.Words Java için"
description: "Java'da bir Word belge düğümünün tipini belirtir."
type: docs
weight: 483
url: /tr/java/com.aspose.words/nodetype/
---

**Inheritance:**
java.lang.Object
```
public class NodeType
```

Bir Word belgesi düğümünün türünü belirtir.

 **Examples:** 

Bir birleşik düğümün çocuk düğüm koleksiyonunda nasıl gezileceğini gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [ANY](#ANY) | Tüm düğüm tiplerini gösterir. |
| [BODY](#BODY) | Bir bölümün ana metnini (ana metin hikayesi) içeren bir [Body](../../com.aspose.words/body/) nesnesi. |
| [BOOKMARK_END](#BOOKMARK-END) | Bir yer imi işaretleyicisinin sonu. |
| [BOOKMARK_START](#BOOKMARK-START) | Bir yer imi işaretleyicisinin başlangıcı. |
| [BUILDING_BLOCK](#BUILDING-BLOCK) | Bir sözlük belgesi içinde bir yapı taşı (ör.  |
| [CELL](#CELL) | Bir tablo satırının hücresi. |
| [COMMENT](#COMMENT) | Word belgesindeki bir yorum. |
| [COMMENT_RANGE_END](#COMMENT-RANGE-END) | Yorumlu bir aralığın sonunu temsil eden bir işaretçi düğüm. |
| [COMMENT_RANGE_START](#COMMENT-RANGE-START) | Yorumlu bir aralığın başlangıcını temsil eden bir işaretçi düğüm. |
| [DOCUMENT](#DOCUMENT) | Belge ağacının kökü olarak tüm Word belgesine erişim sağlayan bir [Document](../../com.aspose.words/document/) nesnesi. |
| [EDITABLE_RANGE_END](#EDITABLE-RANGE-END) | Düzenlenebilir bir aralığın sonu. |
| [EDITABLE_RANGE_START](#EDITABLE-RANGE-START) | Düzenlenebilir bir aralığın başlangıcı. |
| [FIELD_END](#FIELD-END) | Bir Word alanının sonunu belirten özel bir karakter. |
| [FIELD_SEPARATOR](#FIELD-SEPARATOR) | Bir alan kodunu alan sonucundan ayıran özel bir karakter. |
| [FIELD_START](#FIELD-START) | Bir Word alanının başlangıcını belirten özel bir karakter. |
| [FOOTNOTE](#FOOTNOTE) | Bir Word belgesindeki dipnot veya sonnot. |
| [FORM_FIELD](#FORM-FIELD) | Bir form alanı. |
| [GLOSSARY_DOCUMENT](#GLOSSARY-DOCUMENT) | Ana belge içinde bir sözlük belgesi. |
| [GROUP_SHAPE](#GROUP-SHAPE) | Şekiller, görseller, OLE nesneleri veya diğer grup şekillerinden oluşan bir grup. |
| [HEADER_FOOTER](#HEADER-FOOTER) | Bir bölüm içinde belirli bir üstbilgi veya altbilginin metnini içeren bir [HeaderFooter](../../com.aspose.words/headerfooter/) nesnesi. |
| [MOVE_FROM_RANGE_END](#MOVE-FROM-RANGE-END) | Bir MoveFrom aralığının sonu. |
| [MOVE_FROM_RANGE_START](#MOVE-FROM-RANGE-START) | Bir MoveFrom aralığının başlangıcı. |
| [MOVE_TO_RANGE_END](#MOVE-TO-RANGE-END) | Bir MoveTo aralığının sonu. |
| [MOVE_TO_RANGE_START](#MOVE-TO-RANGE-START) | Bir MoveTo aralığının başlangıcı. |
| [NULL](#NULL) | Aspose.Words tarafından dahili kullanım için ayrılmıştır. |
| [OFFICE_MATH](#OFFICE-MATH) | Bir Office Math nesnesi. |
| [PARAGRAPH](#PARAGRAPH) | Bir metin paragrafı. |
| [ROW](#ROW) | Bir tablo satırı. |
| [RUN](#RUN) | Bir metin çalışması. |
| [SECTION](#SECTION) | Bir Word belgesindeki bir bölüme karşılık gelen bir [Section](../../com.aspose.words/section/) nesnesi. |
| [SHAPE](#SHAPE) | Bir çizim nesnesi, örneğin bir OfficeArt şekli, görsel veya bir OLE nesnesi. |
| [SMART_TAG](#SMART-TAG) | Bir paragrafta bir veya daha fazla satır içi yapının (çalışmalar, görseller, alanlar, vb.) etrafında bir akıllı etiket. |
| [SPECIAL_CHAR](#SPECIAL-CHAR) | Daha spesifik özel karakter türlerinden biri olmayan bir özel karakter. |
| [STRUCTURED_DOCUMENT_TAG](#STRUCTURED-DOCUMENT-TAG) | Müşteriye özgü bilgileri ve bunların sunum biçimini tanımlamayı sağlar. |
| [STRUCTURED_DOCUMENT_TAG_RANGE_END](#STRUCTURED-DOCUMENT-TAG-RANGE-END) | Bir **ranged** yapılandırılmış belge etiketinin sonu, çok bölümlü içeriği kabul eder. |
| [STRUCTURED_DOCUMENT_TAG_RANGE_START](#STRUCTURED-DOCUMENT-TAG-RANGE-START) | Bir **ranged** yapılandırılmış belge etiketinin başlangıcı, çok bölümlü içeriği kabul eder. |
| [SUB_DOCUMENT](#SUB-DOCUMENT) | Başka bir belgeye bağlantı olan bir alt belge düğümü. |
| [SYSTEM](#SYSTEM) | Aspose.Words tarafından dahili kullanım için ayrılmıştır. |
| [TABLE](#TABLE) | Bir [Table](../../com.aspose.words/table/) nesnesi, Word belgesindeki bir tabloyu temsil eder. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String nodeTypeName)](#fromName-java.lang.String) |  |
| [getName(int nodeType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int nodeType)](#toString-int) |  |
### ANY {#ANY}
```
public static int ANY
```


Tüm düğüm türlerini gösterir. Tüm alt düğümleri seçmeye izin verir.

### BODY {#BODY}
```
public static int BODY
```


Bir bölümün ana metnini (ana metin hikayesi) içeren bir [Body](../../com.aspose.words/body/) nesnesi.

Bir [Body](../../com.aspose.words/body/) düğümü, [Paragraph](../../com.aspose.words/paragraph/) ve [Table](../../com.aspose.words/table/) düğümlerine sahip olabilir.

### BOOKMARK_END {#BOOKMARK-END}
```
public static int BOOKMARK_END
```


Bir yer imi işaretleyicisinin sonu.

### BOOKMARK_START {#BOOKMARK-START}
```
public static int BOOKMARK_START
```


Bir yer imi işaretleyicisinin başlangıcı.

### BUILDING_BLOCK {#BUILDING-BLOCK}
```
public static int BUILDING_BLOCK
```


Bir sözlük belgesi içinde bir yapı taşı (ör. sözlük belge girişi).

### CELL {#CELL}
```
public static int CELL
```


Bir tablo satırının hücresi.

Bir [Cell](../../com.aspose.words/cell/) düğümü, [Paragraph](../../com.aspose.words/paragraph/) ve [Table](../../com.aspose.words/table/) düğümlerine sahip olabilir.

### COMMENT {#COMMENT}
```
public static int COMMENT
```


Word belgesindeki bir yorum.

Bir [Comment](../../com.aspose.words/comment/) düğümü, [Paragraph](../../com.aspose.words/paragraph/) ve [Table](../../com.aspose.words/table/) düğümlerine sahip olabilir.

### COMMENT_RANGE_END {#COMMENT-RANGE-END}
```
public static int COMMENT_RANGE_END
```


Yorumlu bir aralığın sonunu temsil eden bir işaretçi düğüm.

### COMMENT_RANGE_START {#COMMENT-RANGE-START}
```
public static int COMMENT_RANGE_START
```


Yorumlu bir aralığın başlangıcını temsil eden bir işaretçi düğüm.

### DOCUMENT {#DOCUMENT}
```
public static int DOCUMENT
```


Belge ağacının kökü olarak tüm Word belgesine erişim sağlayan bir [Document](../../com.aspose.words/document/) nesnesi.

Bir [Document](../../com.aspose.words/document/) düğümü, [Section](../../com.aspose.words/section/) düğümlerine sahip olabilir.

### EDITABLE_RANGE_END {#EDITABLE-RANGE-END}
```
public static int EDITABLE_RANGE_END
```


Düzenlenebilir bir aralığın sonu.

### EDITABLE_RANGE_START {#EDITABLE-RANGE-START}
```
public static int EDITABLE_RANGE_START
```


Düzenlenebilir bir aralığın başlangıcı.

### FIELD_END {#FIELD-END}
```
public static int FIELD_END
```


Bir Word alanının sonunu belirten özel bir karakter.

### FIELD_SEPARATOR {#FIELD-SEPARATOR}
```
public static int FIELD_SEPARATOR
```


Bir alan kodunu alan sonucundan ayıran özel bir karakter.

### FIELD_START {#FIELD-START}
```
public static int FIELD_START
```


Bir Word alanının başlangıcını belirten özel bir karakter.

### FOOTNOTE {#FOOTNOTE}
```
public static int FOOTNOTE
```


Bir Word belgesindeki dipnot veya sonnot.

Bir [Footnote](../../com.aspose.words/footnote/) düğümü, [Paragraph](../../com.aspose.words/paragraph/) ve [Table](../../com.aspose.words/table/) düğümlerine sahip olabilir.

### FORM_FIELD {#FORM-FIELD}
```
public static int FORM_FIELD
```


Bir form alanı.

### GLOSSARY_DOCUMENT {#GLOSSARY-DOCUMENT}
```
public static int GLOSSARY_DOCUMENT
```


Ana belge içinde bir sözlük belgesi.

### GROUP_SHAPE {#GROUP-SHAPE}
```
public static int GROUP_SHAPE
```


Şekiller, görseller, OLE nesneleri veya diğer grup şekillerinden oluşan bir grup.

Bir [GroupShape](../../com.aspose.words/groupshape/) düğümü, diğer [Shape](../../com.aspose.words/shape/) ve [GroupShape](../../com.aspose.words/groupshape/) düğümlerini içerebilir.

### HEADER_FOOTER {#HEADER-FOOTER}
```
public static int HEADER_FOOTER
```


Bir bölüm içinde belirli bir üstbilgi veya altbilginin metnini içeren bir [HeaderFooter](../../com.aspose.words/headerfooter/) nesnesi.

Bir [HeaderFooter](../../com.aspose.words/headerfooter/) düğümü, [Paragraph](../../com.aspose.words/paragraph/) ve [Table](../../com.aspose.words/table/) düğümlerine sahip olabilir.

### MOVE_FROM_RANGE_END {#MOVE-FROM-RANGE-END}
```
public static int MOVE_FROM_RANGE_END
```


Bir MoveFrom aralığının sonu.

### MOVE_FROM_RANGE_START {#MOVE-FROM-RANGE-START}
```
public static int MOVE_FROM_RANGE_START
```


Bir MoveFrom aralığının başlangıcı.

### MOVE_TO_RANGE_END {#MOVE-TO-RANGE-END}
```
public static int MOVE_TO_RANGE_END
```


Bir MoveTo aralığının sonu.

### MOVE_TO_RANGE_START {#MOVE-TO-RANGE-START}
```
public static int MOVE_TO_RANGE_START
```


Bir MoveTo aralığının başlangıcı.

### NULL {#NULL}
```
public static int NULL
```


Aspose.Words tarafından dahili kullanım için ayrılmıştır.

### OFFICE_MATH {#OFFICE-MATH}
```
public static int OFFICE_MATH
```


Bir Office Math nesnesi. Denklem, fonksiyon, matris veya diğer matematiksel nesnelerden biri olabilir. Matematiksel nesnelerden oluşan bir koleksiyon olabilir ve ayrıca metin akışları gibi bazı matematik dışı nesneleri de içerebilir.

### PARAGRAPH {#PARAGRAPH}
```
public static int PARAGRAPH
```


Bir metin paragrafı.

Bir [Paragraph](../../com.aspose.words/paragraph/) düğümü, satır içi düzeydeki öğeler olan [Run](../../com.aspose.words/run/), [FieldStart](../../com.aspose.words/fieldstart/), [FieldSeparator](../../com.aspose.words/fieldseparator/), [FieldEnd](../../com.aspose.words/fieldend/), [FormField](../../com.aspose.words/formfield/), [Shape](../../com.aspose.words/shape/), [GroupShape](../../com.aspose.words/groupshape/), [Footnote](../../com.aspose.words/footnote/), [Comment](../../com.aspose.words/comment/), [SpecialChar](../../com.aspose.words/specialchar/) ve ayrıca [BookmarkStart](../../com.aspose.words/bookmarkstart/) ile [BookmarkEnd](../../com.aspose.words/bookmarkend/) için bir kapsayıcıdır.

### ROW {#ROW}
```
public static int ROW
```


Bir tablo satırı.

Bir [Row](../../com.aspose.words/row/) düğümü, [Cell](../../com.aspose.words/cell/) düğümlerine sahip olabilir.

### RUN {#RUN}
```
public static int RUN
```


Bir metin çalışması.

### SECTION {#SECTION}
```
public static int SECTION
```


Bir Word belgesindeki bir bölüme karşılık gelen bir [Section](../../com.aspose.words/section/) nesnesi.

Bir [Section](../../com.aspose.words/section/) düğümü, [Body](../../com.aspose.words/body/) ve [HeaderFooter](../../com.aspose.words/headerfooter/) düğümlerine sahip olabilir.

### SHAPE {#SHAPE}
```
public static int SHAPE
```


Bir çizim nesnesi, örneğin bir OfficeArt şekli, görsel veya bir OLE nesnesi.

Bir [Shape](../../com.aspose.words/shape/) düğümü, [Paragraph](../../com.aspose.words/paragraph/) ve [Table](../../com.aspose.words/table/) düğümlerini içerebilir.

### SMART_TAG {#SMART-TAG}
```
public static int SMART_TAG
```


Bir paragrafta bir veya daha fazla satır içi yapının (çalışmalar, görseller, alanlar, vb.) etrafında bir akıllı etiket.

### SPECIAL_CHAR {#SPECIAL-CHAR}
```
public static int SPECIAL_CHAR
```


Daha spesifik özel karakter türlerinden biri olmayan bir özel karakter.

### STRUCTURED_DOCUMENT_TAG {#STRUCTURED-DOCUMENT-TAG}
```
public static int STRUCTURED_DOCUMENT_TAG
```


Müşteriye özgü bilgileri ve bunların sunum biçimini tanımlamayı sağlar.

### STRUCTURED_DOCUMENT_TAG_RANGE_END {#STRUCTURED-DOCUMENT-TAG-RANGE-END}
```
public static int STRUCTURED_DOCUMENT_TAG_RANGE_END
```


Bir **ranged** yapılandırılmış belge etiketinin sonu, çok bölümlü içeriği kabul eder.

### STRUCTURED_DOCUMENT_TAG_RANGE_START {#STRUCTURED-DOCUMENT-TAG-RANGE-START}
```
public static int STRUCTURED_DOCUMENT_TAG_RANGE_START
```


Bir **ranged** yapılandırılmış belge etiketinin başlangıcı, çok bölümlü içeriği kabul eder.

### SUB_DOCUMENT {#SUB-DOCUMENT}
```
public static int SUB_DOCUMENT
```


Başka bir belgeye bağlantı olan bir alt belge düğümü.

### SYSTEM {#SYSTEM}
```
public static int SYSTEM
```


Aspose.Words tarafından dahili kullanım için ayrılmıştır.

### TABLE {#TABLE}
```
public static int TABLE
```


Bir [Table](../../com.aspose.words/table/) nesnesi, Word belgesindeki bir tabloyu temsil eder.

Bir [Table](../../com.aspose.words/table/) düğümü, [Row](../../com.aspose.words/row/) düğümlerine sahip olabilir.

### length {#length}
```
public static int length
```


### fromName(String nodeTypeName) {#fromName-java.lang.String}
```
public static int fromName(String nodeTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| nodeTypeName | java.lang.String |  |

**Returns:**
int
### getName(int nodeType) {#getName-int}
```
public static String getName(int nodeType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
