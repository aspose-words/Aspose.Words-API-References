---
title: "StructuredDocumentTagRangeStart"
linktitle: "StructuredDocumentTagRangeStart"
second_title: "Aspose.Words Java için"
description: "Java'da çok bölümlü içerik kabul eden aralıklı yapılandırılmış belge etiketi başlangıcını temsil eder."
type: docs
weight: 640
url: /tr/java/com.aspose.words/structureddocumenttagrangestart/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node/)

**All Implemented Interfaces:**
[com.aspose.words.IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/), java.lang.Iterable
```
public class StructuredDocumentTagRangeStart extends Node implements IStructuredDocumentTag, Iterable
```

**ranged** yapılandırılmış belge etiketinin başlangıcını temsil eder ve çok bölümlü içerik kabul eder. Ayrıca bakınız [StructuredDocumentTagRangeEnd](../../com.aspose.words/structureddocumenttagrangeend/).

Daha fazla bilgi için, [ Yapılandırılmış Belge Etiketleri veya İçerik Kontrolü ][Yapılandırılmış Belge Etiketleri veya İçerik Kontrolü] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

[Body](../../com.aspose.words/body/) düğümünün **yalnızca** doğrudan çocuğu olabilir.

 **Examples:** 

Çok bölümlü yapılandırılmış belge etiketlerinin özelliklerini nasıl alacağınızı gösterir.

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


[Structured Document Tags or Content Control]: https://docs.aspose.com/words/java/working-with-content-control-sdt/
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [StructuredDocumentTagRangeStart(DocumentBase doc, int type)](#StructuredDocumentTagRangeStart-com.aspose.words.DocumentBase-int) | Bu sınıfın yeni bir örneğini başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor) | Bir ziyaretçiyi kabul eder. |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node) | Belirtilen düğümü stdContent aralığının sonuna ekler. |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean) | Düğümün bir kopyasını oluşturur. |
| [getAncestor(int ancestorType)](#getAncestor-int) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class) | Belirtilen nesne tipinin ilk atasını alır. |
| [getAppearance()](#getAppearance) | Yapılandırılmış belge etiketinin görünümünü alır. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean) |  |
| [getColor()](#getColor) | Yapılandırılmış belge etiketinin rengini alır. |
| [getCustomNodeId()](#getCustomNodeId) | Özel düğüm tanımlayıcısını belirtir. |
| [getDocument()](#getDocument) | Bu düğümün ait olduğu belgeyi alır. |
| [getId()](#getId) | Bu yapılandırılmış belge etiketi için benzersiz, yalnızca okunabilir, kalıcı sayısal Id belirtir. |
| [getLastChild()](#getLastChild) | stdContent aralığındaki son çocuğu alır. |
| [getLevel()](#getLevel) | Bu yapılandırılmış belge etiketi aralığı başlangıcının belge ağacında gerçekleştiği seviyeyi alır. |
| [getLockContentControl()](#getLockContentControl) | true olarak ayarlandığında, bu özellik bir kullanıcının bu yapılandırılmış belge etiketini silmesini engeller. |
| [getLockContents()](#getLockContents) | true olarak ayarlandığında, bu özellik bir kullanıcının bu yapılandırılmış belge etiketinin içeriğini düzenlemesini engeller. |
| [getNextSibling()](#getNextSibling) | Bu düğümü hemen izleyen düğümü alır. |
| [getNode()](#getNode) |  |
| [getNodeType()](#getNodeType) | Döndürür [NodeType.STRUCTURED\_DOCUMENT\_TAG\_RANGE\_START](../../com.aspose.words/nodetype/\#STRUCTURED-DOCUMENT-TAG-RANGE-START). |
| [getParentNode()](#getParentNode) | Bu düğümün hemen üst ebeveynini alır. |
| [getPlaceholder()](#getPlaceholder) | Bu yapılandırılmış belge etiketi çalıştırma içeriği boş olduğunda, ilgili eşlenmiş XML öğesi [getXmlMapping()](../../com.aspose.words/structureddocumenttagrangestart/\#getXmlMapping) ile belirtildiği gibi boş olduğunda veya [isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttagrangestart/\#isShowingPlaceholderText) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttagrangestart/\#isShowingPlaceholderText-boolean) öğesi true olduğunda görüntülenmesi gereken yer tutucu metni içeren [BuildingBlock](../../com.aspose.words/buildingblock/) öğesini alır. |
| [getPlaceholderName()](#getPlaceholderName) | [BuildingBlock](../../com.aspose.words/buildingblock/) içinde yer tutucu metni içeren adını alır veya ayarlar. |
| [getPreviousSibling()](#getPreviousSibling) | Bu düğümden hemen önce gelen düğümü alır. |
| [getRange()](#getRange) | Bu düğümde bulunan bir belgenin bölümünü temsil eden bir [Range](../../com.aspose.words/range/) nesnesini döndürür. |
| [getRangeEnd()](#getRangeEnd) | Eğer [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) aralıklı bir yapılandırılmış belge etiketi ise, aralığın sonunu belirtir. |
| [getSdtType()](#getSdtType) | Bu yapılandırılmış belge etiketinin türünü alır. |
| [getTag()](#getTag) | Mevcut yapılandırılmış belge etiketi düğümüyle ilişkili bir etiketi belirtir. |
| [getText()](#getText) | Bu düğümün ve tüm alt düğümlerinin metnini alır. |
| [getTitle()](#getTitle) | Bu yapılandırılmış belge etiketiyle ilişkili dostane adı belirtir. |
| [getWordOpenXML()](#getWordOpenXML) | Düğüm içinde bulunan XML'i [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC) formatında temsil eden bir dizeyi alır. |
| [getWordOpenXMLMinimal()](#getWordOpenXMLMinimal) | Düğüm içinde bulunan XML'i [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC) formatında temsil eden bir dizeyi alır. |
| [getXmlMapping()](#getXmlMapping) | Bu yapılandırılmış belge etiketi aralığının, geçerli belgenin özel bir XML bölümündeki XML verisine eşlemesini temsil eden bir nesneyi alır. |
| [isComposite()](#isComposite) | Bu düğüm diğer düğümleri içerebiliyorsa  true  döndürür. |
| [isMultiSection()](#isMultiSection) |  |
| [isShowingPlaceholderText()](#isShowingPlaceholderText) | Bu yapılandırılmış belge etiketinin içeriğinin yer tutucu metin içerdiği (yapılandırılmış belge etiketi içindeki normal metin içeriğine kıyasla) yorumlanıp yorumlanmayacağını belirtir. |
| [isShowingPlaceholderText(boolean value)](#isShowingPlaceholderText-boolean) | Bu yapılandırılmış belge etiketinin içeriğinin yer tutucu metin içerdiği (yapılandırılmış belge etiketi içindeki normal metin içeriğine kıyasla) yorumlanıp yorumlanmayacağını belirtir. |
| [iterator()](#iterator) | Bu düğümün alt düğümleri üzerinde foreach tarzı yineleme desteği sağlar. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node) | Ön sipariş ağaç dolaşım algoritmasına göre bir sonraki düğümü alır. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int) |  |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node) | Ön sipariş ağaç dolaşım algoritmasına göre önceki düğümü alır. |
| [remove()](#remove) | Kendisini ebeveyninden kaldırır. |
| [removeAllChildren()](#removeAllChildren) | Bu aralık başlangıç düğümü ile aralık bitiş düğümü arasındaki tüm düğümleri kaldırır. |
| [removeSelfOnly()](#removeSelfOnly) | Bu yapılandırılmış belge etiketinin aralık başlangıç ve uygun aralık bitiş düğümlerini kaldırır, ancak içeriğini belge ağacında tutar. |
| [setAppearance(int value)](#setAppearance-int) | Yapılandırılmış belge etiketinin görünümünü ayarlar. |
| [setColor(Color value)](#setColor-java.awt.Color) | Yapılandırılmış belge etiketinin rengini ayarlar. |
| [setCustomNodeId(int value)](#setCustomNodeId-int) | Özel düğüm tanımlayıcısını belirtir. |
| [setLockContentControl(boolean value)](#setLockContentControl-boolean) | true olarak ayarlandığında, bu özellik bir kullanıcının bu yapılandırılmış belge etiketini silmesini engeller. |
| [setLockContents(boolean value)](#setLockContents-boolean) | true olarak ayarlandığında, bu özellik bir kullanıcının bu yapılandırılmış belge etiketinin içeriğini düzenlemesini engeller. |
| [setPlaceholderName(String value)](#setPlaceholderName-java.lang.String) | [BuildingBlock](../../com.aspose.words/buildingblock/) içinde yer tutucu metni içeren adını alır veya ayarlar. |
| [setTag(String value)](#setTag-java.lang.String) | Mevcut yapılandırılmış belge etiketi düğümüyle ilişkili bir etiketi belirtir. |
| [setTitle(String value)](#setTitle-java.lang.String) | Bu yapılandırılmış belge etiketiyle ilişkili dostane adı belirtir. |
| [toString()](#toString) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions) | Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır. |
| [toString(int saveFormat)](#toString-int) |  |
### StructuredDocumentTagRangeStart(DocumentBase doc, int type) {#StructuredDocumentTagRangeStart-com.aspose.words.DocumentBase-int}
```
public StructuredDocumentTagRangeStart(DocumentBase doc, int type)
```


Bu sınıfın yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| tip | int |  |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor}
```
public boolean accept(DocumentVisitor visitor)
```


Bir ziyaretçiyi kabul eder.

 **Remarks:** 

Bu düğüm ve tüm çocukları üzerinde yineleme yapar. Her düğüm, [DocumentVisitor](../../com.aspose.words/documentvisitor/) üzerindeki ilgili yöntemi çağırır.

Daha fazla bilgi için Visitor tasarım desenine bakın.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | Düğümleri ziyaret edecek ziyaretçi. |

**Returns:**
boolean - Tüm düğümler ziyaret edildiyse true; [DocumentVisitor](../../com.aspose.words/documentvisitor/) tüm düğümleri ziyaret etmeden işlemi durdurduysa false.
### appendChild(Node newChild) {#appendChild-com.aspose.words.Node}
```
public Node appendChild(Node newChild)
```


Belirtilen düğümü stdContent aralığının sonuna ekler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | Eklenecek düğüm. |

**Returns:**
[Node](../../com.aspose.words/node/) - The node added.
### deepClone(boolean isCloneChildren) {#deepClone-boolean}
```
public Node deepClone(boolean isCloneChildren)
```


Düğümün bir kopyasını oluşturur.

 **Remarks:** 

Bu yöntem, düğümler için bir kopya yapıcı görevi görür. Kopyalanan düğümün ebeveyni yoktur, ancak orijinal düğümle aynı belgeye aittir.

Bu yöntem her zaman düğümün derin bir kopyasını yapar.  isCloneChildren  parametresi, tüm çocuk düğümlerin de kopyalanıp kopyalanmayacağını belirtir.

 **Examples:** 

Bir birleşik düğümün nasıl kopyalanacağını gösterir.

```

 Document doc = new Document();
 Paragraph para = doc.getFirstSection().getBody().getFirstParagraph();
 para.appendChild(new Run(doc, "Hello world!"));

 // Below are two ways of cloning a composite node.
 // 1 -  Create a clone of a node, and create a clone of each of its child nodes as well.
 Node cloneWithChildren = para.deepClone(true);

 Assert.assertTrue(((CompositeNode) cloneWithChildren).hasChildNodes());
 Assert.assertEquals("Hello world!", cloneWithChildren.getText().trim());

 // 2 -  Create a clone of a node just by itself without any children.
 Node cloneWithoutChildren = para.deepClone(false);

 Assert.assertFalse(((CompositeNode) cloneWithoutChildren).hasChildNodes());
 Assert.assertEquals("", cloneWithoutChildren.getText().trim());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| isCloneChildren | boolean | Belirtilen düğümün alt ağacını yinelemeli olarak kopyalamak için true; yalnızca düğümü kendisini kopyalamak için false. |

**Returns:**
[Node](../../com.aspose.words/node/) - The cloned node.
### getAncestor(int ancestorType) {#getAncestor-int}
```
public CompositeNode getAncestor(int ancestorType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| ancestorType | int |  |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/)
### getAncestor(Class ancestorType) {#getAncestor-java.lang.Class}
```
public CompositeNode getAncestor(Class ancestorType)
```


Belirtilen nesne tipinin ilk atasını alır.

 **Remarks:** 

Atalar tipi,  ancestorType  değerine eşitse veya  ancestorType  değerinden türetilmişse eşleşir.

 **Examples:** 

Tabloların iç içe olup olmadığını bulmayı gösterir.

```

 public void calculateDepthOfNestedTables() throws Exception {
     Document doc = new Document(getMyDir() + "Nested tables.docx");
     NodeCollection tables = doc.getChildNodes(NodeType.TABLE, true);
     for (int i = 0; i < tables.getCount(); i++) {
         Table table = (Table) tables.get(i);

         // Find out if any cells in the table have other tables as children.
         int count = getChildTableCount(table);
         System.out.print(MessageFormat.format("Table #{0} has {1} tables directly within its cells", i, count));

         // Find out if the table is nested inside another table, and, if so, at what depth.
         int tableDepth = getNestedDepthOfTable(table);

         if (tableDepth > 0)
             System.out.println(MessageFormat.format("Table #{0} is nested inside another table at depth of {1}", i, tableDepth));
         else
             System.out.println(MessageFormat.format("Table #{0} is a non nested table (is not a child of another table)", i));
     }
 }

 // Calculates what level a table is nested inside other tables.
 //
 // Returns An integer containing the level the table is nested at.
 // 0 = Table is not nested inside any other table
 // 1 = Table is nested within one parent table
 // 2 = Table is nested within two parent tables etc..
 private static int getNestedDepthOfTable(final Table table) {
     int depth = 0;
     Node parent = table.getAncestor(table.getNodeType());

     while (parent != null) {
         depth++;
         parent = parent.getAncestor(Table.class);
     }

     return depth;
 }

 // Determines if a table contains any immediate child table within its cells.
 // Does not recursively traverse through those tables to check for further tables.
 //
 // Returns true if at least one child cell contains a table.
 // Returns false if no cells in the table contains a table.
 private static int getChildTableCount(final Table table) {
     int childTableCount = 0;

     for (Row row : table.getRows()) {
         for (Cell cell : row.getCells()) {
             TableCollection childTables = cell.getTables();

             if (childTables.getCount() > 0) childTableCount++;
         }
     }

     return childTableCount;
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| ancestorType | java.lang.Class | Alınacak atanın nesne tipi. |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/) - The ancestor of the specified type or  null  if no ancestor of this type was found.
### getAppearance() {#getAppearance}
```
public int getAppearance()
```


Yapılandırılmış belge etiketinin görünümünü alır.

 **Examples:** 

İçeriğin etrafında etiketi nasıl göstereceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");
 StructuredDocumentTagRangeStart tag = (StructuredDocumentTagRangeStart) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, true);

 if (tag.getAppearance() == SdtAppearance.HIDDEN)
     tag.setAppearance(SdtAppearance.TAGS);
 
```

**Returns:**
int - Yapılandırılmış belge etiketinin görünümü. Döndürülen değer, [SdtAppearance](../../com.aspose.words/sdtappearance/) sabitlerinden biridir.
### getChildNodes(int nodeType, boolean isDeep) {#getChildNodes-int-boolean}
```
public NodeCollection getChildNodes(int nodeType, boolean isDeep)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| nodeType | int |  |
| isDeep | boolean |  |

**Returns:**
[NodeCollection](../../com.aspose.words/nodecollection/)
### getColor() {#getColor}
```
public Color getColor()
```


Yapılandırılmış belge etiketinin rengini alır.

 **Examples:** 

Çok bölümlü yapılandırılmış belge etiketlerinin özelliklerini nasıl alacağınızı gösterir.

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
java.awt.Color - Yapılandırılmış belge etiketinin rengi.
### getCustomNodeId() {#getCustomNodeId}
```
public int getCustomNodeId()
```


Özel düğüm tanımlayıcısını belirtir.

 **Remarks:** 

Varsayılan sıfırdır.

Bu tanımlayıcı isteğe bağlı olarak ayarlanabilir ve kullanılabilir. Örneğin, harici verileri almak için bir anahtar olarak.

Önemli not, belirtilen değer bir çıkış dosyasına kaydedilmez ve yalnızca düğüm ömrü boyunca var olur.

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

**Returns:**
int - İlgili  int  değeri.
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Bu düğümün ait olduğu belgeyi alır.

 **Remarks:** 

Düğüm, yeni oluşturulmuş ve henüz ağaca eklenmemiş olsa ya da ağaçtan kaldırılmış olsa bile her zaman bir belgeye aittir.

 **Examples:** 

Bir düğüm oluşturmayı ve sahip olduğu belgeyi ayarlamayı gösterir.

```

 Document doc = new Document();
 Paragraph para = new Paragraph(doc);
 para.appendChild(new Run(doc, "Hello world!"));

 // We have not yet appended this paragraph as a child to any composite node.
 Assert.assertNull(para.getParentNode());

 // If a node is an appropriate child node type of another composite node,
 // we can attach it as a child only if both nodes have the same owner document.
 // The owner document is the document we passed to the node's constructor.
 // We have not attached this paragraph to the document, so the document does not contain its text.
 Assert.assertEquals(para.getDocument(), doc);
 Assert.assertEquals("", doc.getText().trim());

 // Since the document owns this paragraph, we can apply one of its styles to the paragraph's contents.
 para.getParagraphFormat().setStyleName("Heading 1");

 // Add this node to the document, and then verify its contents.
 doc.getFirstSection().getBody().appendChild(para);

 Assert.assertEquals(doc.getFirstSection().getBody(), para.getParentNode());
 Assert.assertEquals("Hello world!", doc.getText().trim());
 
```

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/) - The document to which this node belongs.
### getId() {#getId}
```
public int getId()
```


Bu yapılandırılmış belge etiketi için benzersiz, yalnızca okunabilir, kalıcı sayısal Id belirtir.

 **Remarks:** 

Id özniteliği şu kurallara uymalıdır:

 *  The document shall retain structured document tag ids only if the whole document is cloned [Document.deepClone()](../../com.aspose.words/document/\#deepClone).
 *  During [DocumentBase.importNode(com.aspose.words.Node, boolean)](../../com.aspose.words/documentbase/\#importNode-com.aspose.words.Node--boolean) Id shall be retained if import does not cause conflicts with other structured document tag Ids in the target document.
 *  If multiple structured document tag nodes specify the same decimal number value for the Id attribute, then the first structured document tag in the document shall maintain this original Id, and all subsequent structured document tag nodes shall have new identifiers assigned to them when the document is loaded.
 *  During standalone structured document tag **M:Aspose.Words.Markup.StructuredDocumentTag.Clone(System.Boolean,Aspose.Words.INodeCloningListener)** operation new unique ID will be generated for the cloned structured document tag node.
 *  If Id is not specified in the source document, then the structured document tag node shall have a new unique identifier assigned to it when the document is loaded.

 **Examples:** 

Çok bölümlü yapılandırılmış belge etiketlerinin özelliklerini nasıl alacağınızı gösterir.

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
int - İlgili  int  değeri.
### getLastChild() {#getLastChild}
```
public Node getLastChild()
```


stdContent aralığındaki son çocuğu alır.

 **Remarks:** 

Eğer son çocuk düğüm yoksa, bir  null  döndürülür.

**Returns:**
[Node](../../com.aspose.words/node/) - The last child in the stdContent range.
### getLevel() {#getLevel}
```
public int getLevel()
```


Bu yapılandırılmış belge etiketi aralığı başlangıcının belge ağacında gerçekleştiği seviyeyi alır.

 **Examples:** 

Çok bölümlü yapılandırılmış belge etiketlerinin özelliklerini nasıl alacağınızı gösterir.

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
int - Bu yapılandırılmış belge etiketi aralık başlangıcının belge ağacında bulunduğu seviye. Döndürülen değer, [MarkupLevel](../../com.aspose.words/markuplevel/) sabitlerinden biridir.
### getLockContentControl() {#getLockContentControl}
```
public boolean getLockContentControl()
```


true olarak ayarlandığında, bu özellik bir kullanıcının bu yapılandırılmış belge etiketini silmesini engeller.

 **Examples:** 

Çok bölümlü yapılandırılmış belge etiketlerinin özelliklerini nasıl alacağınızı gösterir.

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
boolean - İlgili  boolean  değeri.
### getLockContents() {#getLockContents}
```
public boolean getLockContents()
```


true olarak ayarlandığında, bu özellik bir kullanıcının bu yapılandırılmış belge etiketinin içeriğini düzenlemesini engeller.

 **Examples:** 

Çok bölümlü yapılandırılmış belge etiketlerinin özelliklerini nasıl alacağınızı gösterir.

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
boolean - İlgili  boolean  değeri.
### getNextSibling() {#getNextSibling}
```
public Node getNextSibling()
```


Bu düğümü hemen izleyen düğümü alır.

 **Remarks:** 

Eğer sonraki düğüm yoksa,  null  döndürülür.

 **Examples:** 

Bir birleşik düğümün alt düğüm ağacını nasıl dolaşacağınızı gösterir.

```

 public void recurseChildren() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");

     // Any node that can contain child nodes, such as the document itself, is composite.
     Assert.assertTrue(doc.isComposite());

     // Invoke the recursive function that will go through and print all the child nodes of a composite node.
     traverseAllNodes(doc, 0);
 }

 /// 
 /// Recursively traverses a node tree while printing the type of each node
 /// with an indent depending on depth as well as the contents of all inline nodes.
 /// 
 public void traverseAllNodes(CompositeNode parentNode, int depth) {
     for (Node childNode = parentNode.getFirstChild(); childNode != null; childNode = childNode.getNextSibling()) {
         System.out.println(MessageFormat.format("{0}{1}", String.format("    ", depth), Node.nodeTypeToString(childNode.getNodeType())));

         // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
         if (childNode.isComposite()) {
             System.out.println();
             traverseAllNodes((CompositeNode) childNode, depth + 1);
         } else if (childNode instanceof Inline) {
             System.out.println(MessageFormat.format(" - \"{0}\"", childNode.getText().trim()));
         } else {
             System.out.println();
         }
     }
 }
 
```

Bir düğümün NextSibling özelliğini kullanarak doğrudan alt öğelerini nasıl numaralandıracağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Paragraphs.docx");

 for (Node node = doc.getFirstSection().getBody().getFirstChild(); node != null; node = node.getNextSibling()) {
     System.out.println(Node.nodeTypeToString(node.getNodeType()));
 }
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The node immediately following this node.
### getNode() {#getNode}
```
public Node getNode()
```


Bu arayüzü uygulayan Node nesnesini döndürür.

**Returns:**
[Node](../../com.aspose.words/node/)
### getNodeType() {#getNodeType}
```
public int getNodeType()
```


Döndürür [NodeType.STRUCTURED\_DOCUMENT\_TAG\_RANGE\_START](../../com.aspose.words/nodetype/\#STRUCTURED-DOCUMENT-TAG-RANGE-START).

**Returns:**
int - [NodeType.STRUCTURED\_DOCUMENT\_TAG\_RANGE\_START](../../com.aspose.words/nodetype/\#STRUCTURED-DOCUMENT-TAG-RANGE-START). Döndürülen değer, [NodeType](../../com.aspose.words/nodetype/) sabitlerinden biridir.
### getParentNode() {#getParentNode}
```
public CompositeNode getParentNode()
```


Bu düğümün hemen üst ebeveynini alır.

 **Remarks:** 

Bir düğüm yeni oluşturulmuş ve henüz ağaca eklenmemişse veya ağaçtan kaldırılmışsa, üst düğüm  null  olur.

 **Examples:** 

Bir düğümün üst düğümüne nasıl erişileceğini gösterir.

```

 Document doc = new Document();
 Paragraph para = doc.getFirstSection().getBody().getFirstParagraph();

 // Append a child Run node to the document's first paragraph.
 Run run = new Run(doc, "Hello world!");
 para.appendChild(run);

 // The paragraph is the parent node of the run node. We can trace this lineage
 // all the way to the document node, which is the root of the document's node tree.
 Assert.assertEquals(para, run.getParentNode());
 Assert.assertEquals(doc.getFirstSection().getBody(), para.getParentNode());
 Assert.assertEquals(doc.getFirstSection(), doc.getFirstSection().getBody().getParentNode());
 Assert.assertEquals(doc, doc.getFirstSection().getParentNode());
 
```

Bir düğüm oluşturmayı ve sahip olduğu belgeyi ayarlamayı gösterir.

```

 Document doc = new Document();
 Paragraph para = new Paragraph(doc);
 para.appendChild(new Run(doc, "Hello world!"));

 // We have not yet appended this paragraph as a child to any composite node.
 Assert.assertNull(para.getParentNode());

 // If a node is an appropriate child node type of another composite node,
 // we can attach it as a child only if both nodes have the same owner document.
 // The owner document is the document we passed to the node's constructor.
 // We have not attached this paragraph to the document, so the document does not contain its text.
 Assert.assertEquals(para.getDocument(), doc);
 Assert.assertEquals("", doc.getText().trim());

 // Since the document owns this paragraph, we can apply one of its styles to the paragraph's contents.
 para.getParagraphFormat().setStyleName("Heading 1");

 // Add this node to the document, and then verify its contents.
 doc.getFirstSection().getBody().appendChild(para);

 Assert.assertEquals(doc.getFirstSection().getBody(), para.getParentNode());
 Assert.assertEquals("Hello world!", doc.getText().trim());
 
```

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/) - The immediate parent of this node.
### getPlaceholder() {#getPlaceholder}
```
public BuildingBlock getPlaceholder()
```


Bu yapılandırılmış belge etiketi çalıştırma içeriği boş olduğunda, ilgili eşlenmiş XML öğesi [getXmlMapping()](../../com.aspose.words/structureddocumenttagrangestart/\#getXmlMapping) ile belirtildiği gibi boş olduğunda veya [isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttagrangestart/\#isShowingPlaceholderText) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttagrangestart/\#isShowingPlaceholderText-boolean) öğesi true olduğunda görüntülenmesi gereken yer tutucu metni içeren [BuildingBlock](../../com.aspose.words/buildingblock/) öğesini alır.

 **Remarks:** 

null olabilir, bu da yer tutucunun bu yapılandırılmış belge etiketi için geçerli olmadığını gösterir.

**Returns:**
[BuildingBlock](../../com.aspose.words/buildingblock/) - The [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text which should be displayed when this structured document tag run contents are empty, the associated mapped XML element is empty as specified via the [getXmlMapping()](../../com.aspose.words/structureddocumenttagrangestart/\#getXmlMapping) element or the [isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttagrangestart/\#isShowingPlaceholderText) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttagrangestart/\#isShowingPlaceholderText-boolean) element is  true .
### getPlaceholderName() {#getPlaceholderName}
```
public String getPlaceholderName()
```


[BuildingBlock](../../com.aspose.words/buildingblock/) içinde yer tutucu metni içeren adını alır veya ayarlar.

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getPreviousSibling() {#getPreviousSibling}
```
public Node getPreviousSibling()
```


Bu düğümden hemen önce gelen düğümü alır.

 **Remarks:** 

Eğer önceki düğüm yoksa,  null  döndürülür.

 **Examples:** 

Node ve CompositeNode yöntemlerini kullanarak belgede son bölümden önceki bir bölümü nasıl kaldıracağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1 text.");
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.writeln("Section 2 text.");

 // Both sections are siblings of each other.
 Section lastSection = (Section) doc.getLastChild();
 Section firstSection = (Section) lastSection.getPreviousSibling();

 // Remove a section based on its sibling relationship with another section.
 if (lastSection.getPreviousSibling() != null)
     doc.removeChild(firstSection);

 // The section we removed was the first one, leaving the document with only the second.
 Assert.assertEquals("Section 2 text.", doc.getText().trim());
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The node immediately preceding this node.
### getRange() {#getRange}
```
public Range getRange()
```


Bu düğümde bulunan bir belgenin bölümünü temsil eden bir [Range](../../com.aspose.words/range/) nesnesini döndürür.

 **Examples:** 

Bir aralıktaki tüm düğümleri nasıl sileceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add text to the first section in the document, and then add another section.
 builder.write("Section 1. ");
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.write("Section 2.");

 Assert.assertEquals("Section 1. \fSection 2.", doc.getText().trim());

 // Remove the first section entirely by removing all the nodes
 // within its range, including the section itself.
 doc.getSections().get(0).getRange().delete();

 Assert.assertEquals(1, doc.getSections().getCount());
 Assert.assertEquals("Section 2.", doc.getText().trim());
 
```

**Returns:**
[Range](../../com.aspose.words/range/) - A [Range](../../com.aspose.words/range/) object that represents the portion of a document that is contained in this node.
### getRangeEnd() {#getRangeEnd}
```
public StructuredDocumentTagRangeEnd getRangeEnd()
```


Aralığın sonunu, [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) bir aralıklı yapılandırılmış belge etiketi ise belirtir. Aksi takdirde null döndürür.

 **Examples:** 

Çok bölümlü yapılandırılmış belge etiketlerinin özelliklerini nasıl alacağınızı gösterir.

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
[StructuredDocumentTagRangeEnd](../../com.aspose.words/structureddocumenttagrangeend/) - The corresponding [StructuredDocumentTagRangeEnd](../../com.aspose.words/structureddocumenttagrangeend/) value.
### getSdtType() {#getSdtType}
```
public int getSdtType()
```


Bu yapılandırılmış belge etiketinin türünü alır.

 **Examples:** 

Çok bölümlü yapılandırılmış belge etiketlerinin özelliklerini nasıl alacağınızı gösterir.

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
int - Bu yapılandırılmış belge etiketinin türü. Döndürülen değer, [SdtType](../../com.aspose.words/sdttype/) sabitlerinden biridir.
### getTag() {#getTag}
```
public String getTag()
```


Geçerli yapılandırılmış belge etiketi düğümüyle ilişkili bir etiketi belirtir. null olamaz.

 **Remarks:** 

Etiket, uygulamaların yapılandırılmış belge etiketiyle ilişkilendirebileceği, görünür bir dostane ad sağlamadan onu tanımlamak için kullanılan keyfi bir dizedir.

 **Examples:** 

Çok bölümlü yapılandırılmış belge etiketlerinin özelliklerini nasıl alacağınızı gösterir.

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
java.lang.String - İlgili java.lang.String değeri.
### getText() {#getText}
```
public String getText()
```


Bu düğümün ve tüm alt düğümlerinin metnini alır.

 **Remarks:** 

Döndürülen dize, [ControlChar](../../com.aspose.words/controlchar/) içinde açıklandığı gibi tüm kontrol ve özel karakterleri içerir.

 **Examples:** 

Kontrol karakterlerini nasıl kullanacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert paragraphs with text with DocumentBuilder.
 builder.writeln("Hello world!");
 builder.writeln("Hello again!");

 // Converting the document to text form reveals that control characters
 // represent some of the document's structural elements, such as page breaks.
 Assert.assertEquals(MessageFormat.format("Hello world!{0}", ControlChar.CR) +
         MessageFormat.format("Hello again!{0}", ControlChar.CR) +
         ControlChar.PAGE_BREAK, doc.getText());

 // When converting a document to string form,
 // we can omit some of the control characters with the Trim method.
 Assert.assertEquals(MessageFormat.format("Hello world!{0}", ControlChar.CR) +
         "Hello again!", doc.getText().trim());
 
```

Aspose.Words belgesini elle nasıl oluşturacağınızı gösterir.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Returns:**
java.lang.String
### getTitle() {#getTitle}
```
public String getTitle()
```


Bu yapılandırılmış belge etiketiyle ilişkili dostane adı belirtir. null olamaz.

 **Examples:** 

Çok bölümlü yapılandırılmış belge etiketlerinin özelliklerini nasıl alacağınızı gösterir.

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
java.lang.String - İlgili java.lang.String değeri.
### getWordOpenXML() {#getWordOpenXML}
```
public String getWordOpenXML()
```


Düğüm içinde bulunan XML'i [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC) formatında temsil eden bir dizeyi alır.

 **Examples:** 

Çok bölümlü yapılandırılmış belge etiketlerinin özelliklerini nasıl alacağınızı gösterir.

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
java.lang.String - Düğüm içinde [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC) formatında bulunan XML'i temsil eden bir dize.
### getWordOpenXMLMinimal() {#getWordOpenXMLMinimal}
```
public String getWordOpenXMLMinimal()
```


Düğüm içinde bulunan XML'i [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC) formatında temsil eden bir dize alır. [getWordOpenXML()](../../com.aspose.words/structureddocumenttagrangestart/\#getWordOpenXML) özelliğinin aksine, bu yöntem içerik dışı bölümleri hariç tutan sadeleştirilmiş bir belge oluşturur.

 **Examples:** 

Düğüm içinde bulunan minimal XML'i FlatOpc formatında nasıl alacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");
 StructuredDocumentTagRangeStart tag = (StructuredDocumentTagRangeStart) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, true);

 Assert.assertTrue(tag.getWordOpenXMLMinimal()
         .contains(
                 ""));
 Assert.assertFalse(tag.getWordOpenXMLMinimal().contains("xmlns:w16cid=\"http://schemas.microsoft.com/office/word/2016/wordml/cid\""));
 
```

**Returns:**
java.lang.String - Düğüm içinde [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC) formatında bulunan XML'i temsil eden bir dize.
### getXmlMapping() {#getXmlMapping}
```
public XmlMapping getXmlMapping()
```


Bu yapılandırılmış belge etiketi aralığının, geçerli belgenin özel bir XML bölümündeki XML verisine eşlemesini temsil eden bir nesneyi alır.

 **Remarks:** 

Bu nesnenin [XmlMapping.setMapping(com.aspose.words.CustomXmlPart, java.lang.String, java.lang.String)](../../com.aspose.words/xmlmapping/\#setMapping-com.aspose.words.CustomXmlPart--java.lang.String--java.lang.String) metodunu kullanarak bir yapılandırılmış belge etiketi aralığını XML verisine eşleyebilirsiniz.

 **Examples:** 

Bir yapılandırılmış belge etiketi aralık başlangıcı için XML eşlemelerini nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 // Construct an XML part that contains text and add it to the document's CustomXmlPart collection.
 String xmlPartId = UUID.randomUUID().toString();
 String xmlPartContent = "Text element #1Text element #2";
 CustomXmlPart xmlPart = doc.getCustomXmlParts().add(xmlPartId, xmlPartContent);

 // Create a structured document tag that will display the contents of our CustomXmlPart in the document.
 StructuredDocumentTagRangeStart sdtRangeStart = (StructuredDocumentTagRangeStart) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, true);

 // If we set a mapping for our structured document tag,
 // it will only display a portion of the CustomXmlPart that the XPath points to.
 // This XPath will point to the contents second "" element of the first "" element of our CustomXmlPart.
 sdtRangeStart.getXmlMapping().setMapping(xmlPart, "/root[1]/text[2]", null);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.StructuredDocumentTagRangeStartXmlMapping.docx");
 
```

**Returns:**
[XmlMapping](../../com.aspose.words/xmlmapping/) - An object that represents the mapping of this structured document tag range to XML data in a custom XML part of the current document.
### isComposite() {#isComposite}
```
public boolean isComposite()
```


Bu düğüm diğer düğümleri içerebiliyorsa  true  döndürür. (197141,6)

 **Examples:** 

Bir birleşik düğümün alt düğüm ağacını nasıl dolaşacağınızı gösterir.

```

 public void recurseChildren() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");

     // Any node that can contain child nodes, such as the document itself, is composite.
     Assert.assertTrue(doc.isComposite());

     // Invoke the recursive function that will go through and print all the child nodes of a composite node.
     traverseAllNodes(doc, 0);
 }

 /// 
 /// Recursively traverses a node tree while printing the type of each node
 /// with an indent depending on depth as well as the contents of all inline nodes.
 /// 
 public void traverseAllNodes(CompositeNode parentNode, int depth) {
     for (Node childNode = parentNode.getFirstChild(); childNode != null; childNode = childNode.getNextSibling()) {
         System.out.println(MessageFormat.format("{0}{1}", String.format("    ", depth), Node.nodeTypeToString(childNode.getNodeType())));

         // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
         if (childNode.isComposite()) {
             System.out.println();
             traverseAllNodes((CompositeNode) childNode, depth + 1);
         } else if (childNode instanceof Inline) {
             System.out.println(MessageFormat.format(" - \"{0}\"", childNode.getText().trim()));
         } else {
             System.out.println();
         }
     }
 }
 
```

**Returns:**
boolean -  true  bu düğüm diğer düğümleri içerebiliyorsa.
### isMultiSection() {#isMultiSection}
```
public boolean isMultiSection()
```


Bu örnek bir aralıklı (çok bölümlü) yapılandırılmış belge etiketi ise true döndürür.

 **Examples:** 

Yapılandırılmış belge etiketinin nasıl alınacağını gösterir.

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
boolean
### isShowingPlaceholderText() {#isShowingPlaceholderText}
```
public boolean isShowingPlaceholderText()
```


Bu yapılandırılmış belge etiketinin içeriğinin yer tutucu metin içerdiği (yapılandırılmış belge etiketi içindeki normal metin içeriğine kıyasla) yorumlanıp yorumlanmayacağını belirtir.

true olarak ayarlanırsa, bu durum belge açıldığında (yer tutucu metni göstererek) devam eder.

 **Examples:** 

Çok bölümlü yapılandırılmış belge etiketlerinin özelliklerini nasıl alacağınızı gösterir.

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
boolean - İlgili  boolean  değeri.
### isShowingPlaceholderText(boolean value) {#isShowingPlaceholderText-boolean}
```
public void isShowingPlaceholderText(boolean value)
```


Bu yapılandırılmış belge etiketinin içeriğinin yer tutucu metin içerdiği (yapılandırılmış belge etiketi içindeki normal metin içeriğine kıyasla) yorumlanıp yorumlanmayacağını belirtir.

true olarak ayarlanırsa, bu durum belge açıldığında (yer tutucu metni göstererek) devam eder.

 **Examples:** 

Çok bölümlü yapılandırılmış belge etiketlerinin özelliklerini nasıl alacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### iterator() {#iterator}
```
public Iterator iterator()
```


Bu düğümün alt düğümleri üzerinde foreach tarzı yineleme desteği sağlar.

**Returns:**
java.util.Iterator
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node}
```
public Node nextPreOrder(Node rootNode)
```


Ön sipariş ağaç dolaşım algoritmasına göre bir sonraki düğümü alır.

 **Examples:** 

Belgenin düğüm ağacını ön sipariş (pre-order) dolaşım algoritmasıyla nasıl dolaşacağınızı ve karşılaşılan görüntülü şekilleri nasıl sileceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Images.docx");
 ArrayList shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(9, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));

 Node curNode = doc;
 while (curNode != null) {
     Node nextNode = curNode.nextPreOrder(doc);

     if (curNode.previousPreOrder(doc) != null && nextNode != null)
         Assert.assertEquals(curNode, nextNode.previousPreOrder(doc));

     if (curNode.getNodeType() == NodeType.SHAPE && ((Shape) curNode).hasImage())
         curNode.remove();

     curNode = nextNode;
 }

 shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(0, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node/) | Dolaşımın üst düğümü (limit). |

**Returns:**
[Node](../../com.aspose.words/node/) - Next node in pre-order order. Null if reached the  rootNode .
### nodeTypeToString(int nodeType) {#nodeTypeToString-int}
```
public static String nodeTypeToString(int nodeType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node}
```
public Node previousPreOrder(Node rootNode)
```


Ön sipariş ağaç dolaşım algoritmasına göre önceki düğümü alır.

 **Examples:** 

Belgenin düğüm ağacını ön sipariş (pre-order) dolaşım algoritmasıyla nasıl dolaşacağınızı ve karşılaşılan görüntülü şekilleri nasıl sileceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Images.docx");
 ArrayList shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(9, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));

 Node curNode = doc;
 while (curNode != null) {
     Node nextNode = curNode.nextPreOrder(doc);

     if (curNode.previousPreOrder(doc) != null && nextNode != null)
         Assert.assertEquals(curNode, nextNode.previousPreOrder(doc));

     if (curNode.getNodeType() == NodeType.SHAPE && ((Shape) curNode).hasImage())
         curNode.remove();

     curNode = nextNode;
 }

 shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(0, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node/) | Dolaşımın üst düğümü (limit). |

**Returns:**
[Node](../../com.aspose.words/node/) - Previous node in pre-order order. Null if reached the  rootNode .
### remove() {#remove}
```
public void remove()
```


Kendisini ebeveyninden kaldırır.

 **Examples:** 

Bir belgede bulunan tüm görüntülü şekilleri nasıl sileceğinizi gösterir.

```

 Document doc = new Document(getMyDir() + "Images.docx");
 ArrayList shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(9, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));

 for (Shape shape : shapes)
     if (shape.hasImage())
         shape.remove();

 shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(0, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));
 
```

Bir birleşik düğümden belirli bir türdeki tüm alt düğümleri nasıl kaldıracağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 Assert.assertEquals(2, doc.getChildNodes(NodeType.TABLE, true).getCount());

 Node curNode = doc.getFirstSection().getBody().getFirstChild();

 while (curNode != null) {
     // Save the next sibling node as a variable in case we want to move to it after deleting this node.
     Node nextNode = curNode.getNextSibling();

     // A section body can contain Paragraph and Table nodes.
     // If the node is a Table, remove it from the parent.
     if (curNode.getNodeType() == NodeType.TABLE) {
         curNode.remove();
     }

     curNode = nextNode;
 }

 Assert.assertEquals(0, doc.getChildNodes(NodeType.TABLE, true).getCount());
 
```

### removeAllChildren() {#removeAllChildren}
```
public void removeAllChildren()
```


Bu aralık başlangıç düğümü ile aralık bitiş düğümü arasındaki tüm düğümleri kaldırır.

 **Examples:** 

Yapılandırılmış belge etiketinin ve içeriğinin nasıl oluşturulup/kaldırılacağını gösterir.

```
{@code
 public void sdtRangeExtendedMethods() throws Exception
 {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("StructuredDocumentTag element");

     StructuredDocumentTagRangeStart rangeStart = insertStructuredDocumentTagRanges(doc);

     // Removes ranged structured document tag, but keeps content inside.
     rangeStart.removeSelfOnly();

     rangeStart = (StructuredDocumentTagRangeStart)doc.getChild(
         NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, false);
     Assert.assertEquals(null, rangeStart);

     StructuredDocumentTagRangeEnd rangeEnd = (StructuredDocumentTagRangeEnd)doc.getChild(
         NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, 0, false);

     Assert.assertEquals(null, rangeEnd);
     Assert.assertEquals("StructuredDocumentTag element", doc.getText().trim());

     rangeStart = insertStructuredDocumentTagRanges(doc);

     Node paragraphNode = rangeStart.getLastChild();
     if (paragraphNode != null)
         Assert.assertEquals("StructuredDocumentTag element", paragraphNode.getText().trim());

     // Removes ranged structured document tag and content inside.
     rangeStart.removeAllChildren();

     paragraphNode = rangeStart.getLastChild();
     Assert.assertEquals("",  paragraphNode.getText());
 }
```

### removeSelfOnly() {#removeSelfOnly}
```
public void removeSelfOnly()
```


Bu yapılandırılmış belge etiketinin aralık başlangıç ve uygun aralık bitiş düğümlerini kaldırır, ancak içeriğini belge ağacında tutar.

 **Examples:** 

Yapılandırılmış belge etiketinin ve içeriğinin nasıl oluşturulup/kaldırılacağını gösterir.

```
{@code
 public void sdtRangeExtendedMethods() throws Exception
 {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("StructuredDocumentTag element");

     StructuredDocumentTagRangeStart rangeStart = insertStructuredDocumentTagRanges(doc);

     // Removes ranged structured document tag, but keeps content inside.
     rangeStart.removeSelfOnly();

     rangeStart = (StructuredDocumentTagRangeStart)doc.getChild(
         NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, false);
     Assert.assertEquals(null, rangeStart);

     StructuredDocumentTagRangeEnd rangeEnd = (StructuredDocumentTagRangeEnd)doc.getChild(
         NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, 0, false);

     Assert.assertEquals(null, rangeEnd);
     Assert.assertEquals("StructuredDocumentTag element", doc.getText().trim());

     rangeStart = insertStructuredDocumentTagRanges(doc);

     Node paragraphNode = rangeStart.getLastChild();
     if (paragraphNode != null)
         Assert.assertEquals("StructuredDocumentTag element", paragraphNode.getText().trim());

     // Removes ranged structured document tag and content inside.
     rangeStart.removeAllChildren();

     paragraphNode = rangeStart.getLastChild();
     Assert.assertEquals("",  paragraphNode.getText());
 }
```

### setAppearance(int value) {#setAppearance-int}
```
public void setAppearance(int value)
```


Yapılandırılmış belge etiketinin görünümünü ayarlar.

 **Examples:** 

İçeriğin etrafında etiketi nasıl göstereceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");
 StructuredDocumentTagRangeStart tag = (StructuredDocumentTagRangeStart) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, true);

 if (tag.getAppearance() == SdtAppearance.HIDDEN)
     tag.setAppearance(SdtAppearance.TAGS);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Yapılandırılmış belge etiketinin görünümü. Değer, [SdtAppearance](../../com.aspose.words/sdtappearance/) sabitlerinden biri olmalıdır. |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Yapılandırılmış belge etiketinin rengini ayarlar.

 **Examples:** 

Çok bölümlü yapılandırılmış belge etiketlerinin özelliklerini nasıl alacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color | Yapılandırılmış belge etiketinin rengi. |

### setCustomNodeId(int value) {#setCustomNodeId-int}
```
public void setCustomNodeId(int value)
```


Özel düğüm tanımlayıcısını belirtir.

 **Remarks:** 

Varsayılan sıfırdır.

Bu tanımlayıcı isteğe bağlı olarak ayarlanabilir ve kullanılabilir. Örneğin, harici verileri almak için bir anahtar olarak.

Önemli not, belirtilen değer bir çıkış dosyasına kaydedilmez ve yalnızca düğüm ömrü boyunca var olur.

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | İlgili  int  değeri. |

### setLockContentControl(boolean value) {#setLockContentControl-boolean}
```
public void setLockContentControl(boolean value)
```


true olarak ayarlandığında, bu özellik bir kullanıcının bu yapılandırılmış belge etiketini silmesini engeller.

 **Examples:** 

Çok bölümlü yapılandırılmış belge etiketlerinin özelliklerini nasıl alacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setLockContents(boolean value) {#setLockContents-boolean}
```
public void setLockContents(boolean value)
```


true olarak ayarlandığında, bu özellik bir kullanıcının bu yapılandırılmış belge etiketinin içeriğini düzenlemesini engeller.

 **Examples:** 

Çok bölümlü yapılandırılmış belge etiketlerinin özelliklerini nasıl alacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setPlaceholderName(String value) {#setPlaceholderName-java.lang.String}
```
public void setPlaceholderName(String value)
```


[BuildingBlock](../../com.aspose.words/buildingblock/) içinde yer tutucu metni içeren adını alır veya ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setTag(String value) {#setTag-java.lang.String}
```
public void setTag(String value)
```


Geçerli yapılandırılmış belge etiketi düğümüyle ilişkili bir etiketi belirtir. null olamaz.

 **Remarks:** 

Etiket, uygulamaların yapılandırılmış belge etiketiyle ilişkilendirebileceği, görünür bir dostane ad sağlamadan onu tanımlamak için kullanılan keyfi bir dizedir.

 **Examples:** 

Çok bölümlü yapılandırılmış belge etiketlerinin özelliklerini nasıl alacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setTitle(String value) {#setTitle-java.lang.String}
```
public void setTitle(String value)
```


Bu yapılandırılmış belge etiketiyle ilişkili dostane adı belirtir. null olamaz.

 **Examples:** 

Çok bölümlü yapılandırılmış belge etiketlerinin özelliklerini nasıl alacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(SaveOptions saveOptions) {#toString-com.aspose.words.SaveOptions}
```
public String toString(SaveOptions saveOptions)
```


Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır.

 **Examples:** 

Bir düğümün içeriğini HTML formatında String olarak dışa aktarır.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 Node node = doc.getLastSection().getBody().getLastParagraph();

 // When we call the ToString method using the html SaveFormat overload,
 // it converts the node's contents to their raw html representation.
 Assert.assertEquals(" " +
         "Hello World!" +
         "", node.toString(SaveFormat.HTML));

 // We can also modify the result of this conversion using a SaveOptions object.
 HtmlSaveOptions saveOptions = new HtmlSaveOptions();
 saveOptions.setExportRelativeFontSize(true);

 Assert.assertEquals(" " +
         "Hello World!" +
         "", node.toString(saveOptions));
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Düğümün nasıl kaydedileceğini kontrol eden seçenekleri belirtir. |

**Returns:**
java.lang.String - Düğümün belirtilen formatta içeriği.
### toString(int saveFormat) {#toString-int}
```
public String toString(int saveFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
