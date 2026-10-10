---
title: "FieldStart"
linktitle: "FieldStart"
second_title: "Aspose.Words Java için"
description: "Java'da bir belgede Word alanının başlangıcını temsil eder."
type: docs
weight: 288
url: /tr/java/com.aspose.words/fieldstart/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node/), [com.aspose.words.Inline](../../com.aspose.words/inline/), [com.aspose.words.SpecialChar](../../com.aspose.words/specialchar/), [com.aspose.words.FieldChar](../../com.aspose.words/fieldchar/)
```
public class FieldStart extends FieldChar
```

Bir belgede bir Word alanının başlangıcını temsil eder.

Daha fazla bilgi için, [ Working with Fields ][Working with Fields] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

[FieldStart](../../com.aspose.words/fieldstart/) is an inline-level node and represented by the [ControlChar.FIELD\_START\_CHAR](../../com.aspose.words/controlchar/\#FIELD-START-CHAR) control character in the document.

[FieldStart](../../com.aspose.words/fieldstart/) can only be a child of [Paragraph](../../com.aspose.words/paragraph/).

Microsoft Word belgesindeki tam bir alan, alan başlangıç karakteri, alan kodu, alan ayırıcı karakteri, alan sonucu ve alan bitiş karakterinden oluşan karmaşık bir yapıdır. Bazı alanlarda yalnızca alan başlangıcı, alan kodu ve alan bitişi bulunur.

Bir belgeye yeni bir alan eklemeyi kolayca yapmak için, [DocumentBuilder.insertField(java.lang.String)](../../com.aspose.words/documentbuilder/\#insertField-java.lang.String) metodunu kullanın.

 **Examples:** 

Alan koleksiyonu ile nasıl çalışılacağını gösterir.

```

 public void fieldCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
     builder.insertField(" TIME ");
     builder.insertField(" REVNUM ");
     builder.insertField(" AUTHOR  \"John Doe\" ");
     builder.insertField(" SUBJECT \"My Subject\" ");
     builder.insertField(" QUOTE \"Hello world!\" ");
     doc.updateFields();

     FieldCollection fields = doc.getRange().getFields();

     Assert.assertEquals(6, fields.getCount());

     // Iterate over the field collection, and print contents and type
     // of every field using a custom visitor implementation.
     FieldVisitor fieldVisitor = new FieldVisitor();

     Iterator fieldEnumerator = fields.iterator();

     while (fieldEnumerator.hasNext()) {
         if (fieldEnumerator != null) {
             Field currentField = fieldEnumerator.next();

             currentField.getStart().accept(fieldVisitor);
             if (currentField.getSeparator() != null) {
                 currentField.getSeparator().accept(fieldVisitor);
             }
             currentField.getEnd().accept(fieldVisitor);
         } else {
             System.out.println("There are no fields in the document.");
         }
     }

     System.out.println(fieldVisitor.getText());
 }

 /// 
 /// Document visitor implementation that prints field info.
 /// 
 public static class FieldVisitor extends DocumentVisitor {
     public FieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(final FieldStart fieldStart) {
         mBuilder.append("Found field: " + fieldStart.getFieldType() + "\r\n");
         mBuilder.append("\tField code: " + fieldStart.getField().getFieldCode() + "\r\n");
         mBuilder.append("\tDisplayed as: " + fieldStart.getField().getResult() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(final FieldSeparator fieldSeparator) {
         mBuilder.append("\tFound separator: " + fieldSeparator.getText() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) {
         mBuilder.append("End of field: " + fieldEnd.getFieldType() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     private final  StringBuilder mBuilder;
 }
 
```

Bir Word belgesindeki tüm hiperlinkleri nasıl bulacağınızı ve ardından URL'lerini ve görüntülenen adlarını nasıl değiştireceğinizi gösterir.

```

 import com.aspose.words.*;
 import org.testng.annotations.Test;

 import java.util.regex.Matcher;
 import java.util.regex.Pattern;

 public class ExReplaceHyperlinks extends ApiExampleBase {
     public void fields() throws Exception {
         Document doc = new Document(getMyDir() + "Hyperlinks.docx");

         // Hyperlinks in a Word documents are fields. To begin looking for hyperlinks, we must first find all the fields.
         // Use the "SelectNodes" method to find all the fields in the document via an XPath.
         NodeList fieldStarts = doc.selectNodes("//FieldStart");
         for (FieldStart fieldStart : (Iterable) fieldStarts) {
             if (fieldStart.getFieldType() == FieldType.FIELD_HYPERLINK) {
                 Hyperlink hyperlink = new Hyperlink(fieldStart);

                 // Hyperlinks that link to bookmarks do not have URLs.
                 if (hyperlink.isLocal()) continue;

                 // Give each URL hyperlink a new URL and name.
                 hyperlink.setTarget(NEW_URL);
                 hyperlink.setName(NEW_NAME);
             }
         }

         doc.save(getArtifactsDir() + "ReplaceHyperlinks.Fields.docx");
     }

     private static final String NEW_URL = "http://www.aspose.com";
     private static final String NEW_NAME = "Aspose - The .NET & Java Component Publisher";
 }

 // This "facade" class makes it easier to work with a hyperlink field in a Word document.
 // 
 // HYPERLINK fields contain and display hyperlinks in the document body. A field in Aspose.Words
 // consists of several nodes, and it might be difficult to work with all those nodes directly.
 // This implementation will work only if the hyperlink code and name each consist of only one Run node.
 // 
 // The node structure for fields is as follows:
 // 
 // [FieldStart][Run - field code][FieldSeparator][Run - field result][FieldEnd]
 // 
 // Below are two example field codes of HYPERLINK fields:
 // HYPERLINK "url"
 // HYPERLINK \l "bookmark name"
 // 
 // A field's "Result" property contains text that the field displays in the document body to the user.
 class Hyperlink {
     Hyperlink(final FieldStart fieldStart) throws Exception {
         if (fieldStart == null) {
             throw new IllegalArgumentException("fieldStart");
         }

         if (fieldStart.getFieldType() != FieldType.FIELD_HYPERLINK) {
             throw new IllegalArgumentException("Field start type must be FieldHyperlink.");
         }

         mFieldStart = fieldStart;

         // Find the field separator node.
         mFieldSeparator = findNextSibling(mFieldStart, NodeType.FIELD_SEPARATOR);
         if (mFieldSeparator == null) {
             throw new IllegalStateException("Cannot find field separator.");
         }

         // Normally, we can always find the field's end node, but the example document
         // contains a paragraph break inside a hyperlink, which puts the field end
         // in the next paragraph. It will be much more complicated to handle fields which span several
         // paragraphs correctly. In this case allowing field end to be null is enough.
         mFieldEnd = findNextSibling(mFieldSeparator, NodeType.FIELD_END);

         // Field code looks something like "HYPERLINK "http:\\www.myurl.com"", but it can consist of several runs.
         String fieldCode = getTextSameParent(mFieldStart.getNextSibling(), mFieldSeparator);
         Matcher matcher = G_REGEX.matcher(fieldCode.trim());
         matcher.find();

         // The hyperlink is local if \l is present in the field code.
         mIsLocal = (matcher.group(1) != null) && (matcher.group(1).length() > 0);
         mTarget = matcher.group(2);
     }

     // Gets or sets the display name of the hyperlink.
     String getName() throws Exception {
         return getTextSameParent(mFieldSeparator, mFieldEnd);
     }

     void setName(final String value) throws Exception {
         // Hyperlink display name is stored in the field result, which is a Run
         // node between field separator and field end.
         Run fieldResult = (Run) mFieldSeparator.getNextSibling();
         fieldResult.setText(value);

         // If the field result consists of more than one run, delete these runs.
         removeSameParent(fieldResult.getNextSibling(), mFieldEnd);
     }

     // Gets or sets the target URL or bookmark name of the hyperlink.
     String getTarget() {
         return mTarget;
     }

     void setTarget(final String value) throws Exception {
         mTarget = value;
         updateFieldCode();
     }

     // True if the hyperlinks target is a bookmark inside the document. False if the hyperlink is a URL.
     boolean isLocal() {
         return mIsLocal;
     }

     void isLocal(final boolean value) throws Exception {
         mIsLocal = value;
         updateFieldCode();
     }

     private void updateFieldCode() throws Exception {
         // A field's field code is in a Run node between the field's start node and field separator.
         Run fieldCode = (Run) mFieldStart.getNextSibling();
         fieldCode.setText(java.text.MessageFormat.format("HYPERLINK {0}\"{1}\"", ((mIsLocal) ? "\\l " : ""), mTarget));

         // If the field code consists of more than one run, delete these runs.
         removeSameParent(fieldCode.getNextSibling(), mFieldSeparator);
     }

     // Goes through siblings starting from the start node until it finds a node of the specified type or null.
     private static Node findNextSibling(final Node startNode, final int nodeType) {
         for (Node node = startNode; node != null; node = node.getNextSibling()) {
             if (node.getNodeType() == nodeType) return node;
         }
         return null;
     }

     // Retrieves text from start up to but not including the end node.
     private static String getTextSameParent(final Node startNode, final Node endNode) {
         if ((endNode != null) && (startNode.getParentNode() != endNode.getParentNode())) {
             throw new IllegalArgumentException("Start and end nodes are expected to have the same parent.");
         }

         StringBuilder builder = new StringBuilder();
         for (Node child = startNode; !child.equals(endNode); child = child.getNextSibling()) {
             builder.append(child.getText());
         }

         return builder.toString();
     }

     // Removes nodes from start up to but not including the end node.
     // Assumes that the start and end nodes have the same parent.
     private static void removeSameParent(final Node startNode, final Node endNode) {
         if ((endNode != null) && (startNode.getParentNode() != endNode.getParentNode())) {
             throw new IllegalArgumentException("Start and end nodes are expected to have the same parent.");
         }

         Node curChild = startNode;
         while ((curChild != null) && (curChild != endNode)) {
             Node nextChild = curChild.getNextSibling();
             curChild.remove();
             curChild = nextChild;
         }
     }

     private final Node mFieldStart;
     private final Node mFieldSeparator;
     private final Node mFieldEnd;
     private boolean mIsLocal;
     private String mTarget;

     private static final Pattern G_REGEX = Pattern.compile(
             "\\S+" +             // One or more non spaces HYPERLINK or other word in other languages.
                     "\\s+" +             // One or more spaces.
                     "(?:\"\"\\s+)?" +    // Non-capturing optional "" and one or more spaces.
                     "(\\\\l\\s+)?" +     // Optional \l flag followed by one or more spaces.
                     "\"" +               // One apostrophe.
                     "([^\"]+)" +         // One or more characters, excluding the apostrophe (hyperlink target).
                     "\""                 // One closing apostrophe.
     );
 }
 
```


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor) | Bir ziyaretçiyi kabul eder. |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean) | Düğümün bir kopyasını oluşturur. |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int) |  |
| [getAncestor(int ancestorType)](#getAncestor-int) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class) | Belirtilen nesne tipinin ilk atasını alır. |
| [getCustomNodeId()](#getCustomNodeId) | Özel düğüm tanımlayıcısını belirtir. |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getDocument()](#getDocument) | Bu düğümün ait olduğu belgeyi alır. |
| [getDocument_IInline()](#getDocument-IInline) |  |
| [getField()](#getField) | Alan karakteri için bir alan döndürür. |
| [getFieldData()](#getFieldData) | Alanla ilişkili özel alan verilerini alır. |
| [getFieldType()](#getFieldType) | Alan tipini döndürür. |
| [getFont()](#getFont) | Bu nesnenin yazı tipi biçimlendirmesine erişim sağlar. |
| [getNextSibling()](#getNextSibling) | Bu düğümü hemen izleyen düğümü alır. |
| [getNodeType()](#getNodeType) | Şu değeri döndürür: [NodeType.FIELD\_START](../../com.aspose.words/nodetype/\#FIELD-START). |
| [getParentNode()](#getParentNode) | Bu düğümün hemen üst ebeveynini alır. |
| [getParentParagraph()](#getParentParagraph) | Bu düğümün üst [Paragraph](../../com.aspose.words/paragraph/) öğesini alır. |
| [getParentParagraph_IInline()](#getParentParagraph-IInline) |  |
| [getPreviousSibling()](#getPreviousSibling) | Bu düğümden hemen önce gelen düğümü alır. |
| [getRange()](#getRange) | Bu düğümde bulunan bir belgenin bölümünü temsil eden bir [Range](../../com.aspose.words/range/) nesnesini döndürür. |
| [getText()](#getText) | Bu düğümün temsil ettiği özel karakteri alır. |
| [isComposite()](#isComposite) | Bu düğüm diğer düğümleri içerebiliyorsa  true  döndürür. |
| [isDeleteRevision()](#isDeleteRevision) | Değişiklik izleme etkinken bu nesne Microsoft Word'de silinmişse true döndürür. |
| [isDirty()](#isDirty) | Belgenin diğer değişiklikleri nedeniyle alanın mevcut sonucunun artık doğru (eski) olup olmadığını alır. |
| [isDirty(boolean value)](#isDirty-boolean) | Belgenin diğer değişiklikleri nedeniyle alanın mevcut sonucunun artık doğru (eski) olup olmadığını ayarlar. |
| [isFormatRevision()](#isFormatRevision) | Değişiklik izleme etkinken nesnenin biçimlendirmesi Microsoft Word'de değiştirilmişse true döndürür. |
| [isInsertRevision()](#isInsertRevision) | Değişiklik izleme etkinken bu nesne Microsoft Word'e eklenmişse true döndürür. |
| [isLocked()](#isLocked) | Üst alanın kilitli olup olmadığını alır (sonucu yeniden hesaplamamalıdır). |
| [isLocked(boolean value)](#isLocked-boolean) | Üst alanın kilitli olup olmadığını ayarlar (sonucu yeniden hesaplamamalıdır). |
| [isMoveFromRevision()](#isMoveFromRevision) | Değişiklik izleme etkinken bu nesne Microsoft Word'de taşınmış (silinmiş) ise  true  döndürür. |
| [isMoveToRevision()](#isMoveToRevision) | Değişiklik izleme etkinken bu nesne Microsoft Word'de taşınmış (eklenmiş) ise  true  döndürür. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node) | Ön sipariş ağaç dolaşım algoritmasına göre bir sonraki düğümü alır. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int) |  |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node) | Ön sipariş ağaç dolaşım algoritmasına göre önceki düğümü alır. |
| [remove()](#remove) | Kendisini ebeveyninden kaldırır. |
| [removeMoveRevisions()](#removeMoveRevisions) |  |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [setCustomNodeId(int value)](#setCustomNodeId-int) | Özel düğüm tanımlayıcısını belirtir. |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object) |  |
| [toString()](#toString) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions) | Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır. |
| [toString(int saveFormat)](#toString-int) |  |
### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor}
```
public boolean accept(DocumentVisitor visitor)
```


Bir ziyaretçiyi kabul eder.

 **Remarks:** 

Şunu çağırır: [DocumentVisitor.visitFieldStart(com.aspose.words.FieldStart)](../../com.aspose.words/documentvisitor/\#visitFieldStart-com.aspose.words.FieldStart).

Daha fazla bilgi için Visitor tasarım desenine bakın.

 **Examples:** 

Alan koleksiyonu ile nasıl çalışılacağını gösterir.

```

 public void fieldCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
     builder.insertField(" TIME ");
     builder.insertField(" REVNUM ");
     builder.insertField(" AUTHOR  \"John Doe\" ");
     builder.insertField(" SUBJECT \"My Subject\" ");
     builder.insertField(" QUOTE \"Hello world!\" ");
     doc.updateFields();

     FieldCollection fields = doc.getRange().getFields();

     Assert.assertEquals(6, fields.getCount());

     // Iterate over the field collection, and print contents and type
     // of every field using a custom visitor implementation.
     FieldVisitor fieldVisitor = new FieldVisitor();

     Iterator fieldEnumerator = fields.iterator();

     while (fieldEnumerator.hasNext()) {
         if (fieldEnumerator != null) {
             Field currentField = fieldEnumerator.next();

             currentField.getStart().accept(fieldVisitor);
             if (currentField.getSeparator() != null) {
                 currentField.getSeparator().accept(fieldVisitor);
             }
             currentField.getEnd().accept(fieldVisitor);
         } else {
             System.out.println("There are no fields in the document.");
         }
     }

     System.out.println(fieldVisitor.getText());
 }

 /// 
 /// Document visitor implementation that prints field info.
 /// 
 public static class FieldVisitor extends DocumentVisitor {
     public FieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(final FieldStart fieldStart) {
         mBuilder.append("Found field: " + fieldStart.getFieldType() + "\r\n");
         mBuilder.append("\tField code: " + fieldStart.getField().getFieldCode() + "\r\n");
         mBuilder.append("\tDisplayed as: " + fieldStart.getField().getResult() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(final FieldSeparator fieldSeparator) {
         mBuilder.append("\tFound separator: " + fieldSeparator.getText() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) {
         mBuilder.append("End of field: " + fieldEnd.getFieldType() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     private final  StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | Düğümü ziyaret edecek ziyaretçi. |

**Returns:**
boolean - Ziyaretçi yinelemeyi durdurmak istediğinde **False**.
### clearRunAttrs() {#clearRunAttrs}
```
public void clearRunAttrs()
```




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
### fetchInheritedRunAttr(int fontAttr) {#fetchInheritedRunAttr-int}
```
public Object fetchInheritedRunAttr(int fontAttr)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fontAttr | int |  |

**Returns:**
java.lang.Object
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
### getDirectRunAttr(int key) {#getDirectRunAttr-int}
```
public Object getDirectRunAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key, int revisionsView) {#getDirectRunAttr-int-int}
```
public Object getDirectRunAttr(int key, int revisionsView)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
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
### getDocument_IInline() {#getDocument-IInline}
```
public DocumentBase getDocument_IInline()
```




**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/)
### getField() {#getField}
```
public Field getField()
```


Alan karakteri için bir alan döndürür.

 **Remarks:** 

Metod her çağrıldığında yeni bir [Field](../../com.aspose.words/field/) nesnesi oluşturulur.

 **Examples:** 

Bir FieldStart düğümüyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDate field = (FieldDate) builder.insertField(FieldType.FIELD_DATE, true);
 field.getFormat().setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 FieldChar fieldStart = field.getStart();

 Assert.assertEquals(FieldType.FIELD_DATE, fieldStart.getFieldType());
 Assert.assertEquals(false, fieldStart.isDirty());
 Assert.assertEquals(false, fieldStart.isLocked());

 // Retrieve the facade object which represents the field in the document.
 field = (FieldDate) fieldStart.getField();

 Assert.assertEquals(false, field.isLocked());
 Assert.assertEquals(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());

 // Update the field to show the current date.
 field.update();
 
```

**Returns:**
[Field](../../com.aspose.words/field/) - A field for the field char.
### getFieldData() {#getFieldData}
```
public byte[] getFieldData()
```


Alanla ilişkili özel alan verilerini alır.

 **Examples:** 

Alanla ilişkili verilerin nasıl alınacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Field sample - Field with data.docx");

 Field field = doc.getRange().getFields().get(2);
 System.out.println(new String(field.getStart().getFieldData(), StandardCharsets.UTF_8));
 
```

**Returns:**
byte[] - Alanla ilişkili özel alan verileri.
### getFieldType() {#getFieldType}
```
public int getFieldType()
```


Alan tipini döndürür.

 **Examples:** 

Bir FieldStart düğümüyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDate field = (FieldDate) builder.insertField(FieldType.FIELD_DATE, true);
 field.getFormat().setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 FieldChar fieldStart = field.getStart();

 Assert.assertEquals(FieldType.FIELD_DATE, fieldStart.getFieldType());
 Assert.assertEquals(false, fieldStart.isDirty());
 Assert.assertEquals(false, fieldStart.isLocked());

 // Retrieve the facade object which represents the field in the document.
 field = (FieldDate) fieldStart.getField();

 Assert.assertEquals(false, field.isLocked());
 Assert.assertEquals(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());

 // Update the field to show the current date.
 field.update();
 
```

**Returns:**
int - Alanın tipi. Döndürülen değer [FieldType](../../com.aspose.words/fieldtype/) sabitlerinden biridir.
### getFont() {#getFont}
```
public Font getFont()
```


Bu nesnenin yazı tipi biçimlendirmesine erişim sağlar.

 **Examples:** 

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
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
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
### getNodeType() {#getNodeType}
```
public int getNodeType()
```


Şu değeri döndürür: [NodeType.FIELD\_START](../../com.aspose.words/nodetype/\#FIELD-START).

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
int - [NodeType.FIELD\_START](../../com.aspose.words/nodetype/\#FIELD-START). Döndürülen değer, [NodeType](../../com.aspose.words/nodetype/) sabitlerinden biridir.
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
### getParentParagraph() {#getParentParagraph}
```
public Paragraph getParentParagraph()
```


Bu düğümün üst [Paragraph](../../com.aspose.words/paragraph/) öğesini alır.

 **Examples:** 

Satır içi bir düğümün revizyon tipinin nasıl belirleneceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Revision runs.docx");

 // When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
 // is turned on in Microsoft Word, the changes we apply count as revisions.
 // When editing a document using Aspose.Words, we can begin tracking revisions by
 // invoking the document's "StartTrackRevisions" method and stop tracking by using the "StopTrackRevisions" method.
 // We can either accept revisions to assimilate them into the document
 // or reject them to change the proposed change effectively.
 Assert.assertEquals(6, doc.getRevisions().getCount());

 // The parent node of a revision is the run that the revision concerns. A Run is an Inline node.
 Run run = (Run) doc.getRevisions().get(0).getParentNode();

 Paragraph firstParagraph = run.getParentParagraph();
 RunCollection runs = firstParagraph.getRuns();

 Assert.assertEquals(runs.getCount(), 6);

 // Below are five types of revisions that can flag an Inline node.
 // 1 -  An "insert" revision:
 // This revision occurs when we insert text while tracking changes.
 Assert.assertTrue(runs.get(2).isInsertRevision());

 // 2 -  A "format" revision:
 // This revision occurs when we change the formatting of text while tracking changes.
 Assert.assertTrue(runs.get(2).isFormatRevision());

 // 3 -  A "move from" revision:
 // When we highlight text in Microsoft Word, and then drag it to a different place in the document
 // while tracking changes, two revisions appear.
 // The "move from" revision is a copy of the text originally before we moved it.
 Assert.assertTrue(runs.get(4).isMoveFromRevision());

 // 4 -  A "move to" revision:
 // The "move to" revision is the text that we moved in its new position in the document.
 // "Move from" and "move to" revisions appear in pairs for every move revision we carry out.
 // Accepting a move revision deletes the "move from" revision and its text,
 // and keeps the text from the "move to" revision.
 // Rejecting a move revision conversely keeps the "move from" revision and deletes the "move to" revision.
 Assert.assertTrue(runs.get(1).isMoveToRevision());

 // 5 -  A "delete" revision:
 // This revision occurs when we delete text while tracking changes. When we delete text like this,
 // it will stay in the document as a revision until we either accept the revision,
 // which will delete the text for good, or reject the revision, which will keep the text we deleted where it was.
 Assert.assertTrue(runs.get(5).isDeleteRevision());
 
```

**Returns:**
[Paragraph](../../com.aspose.words/paragraph/) - The corresponding [Paragraph](../../com.aspose.words/paragraph/) value.
### getParentParagraph_IInline() {#getParentParagraph-IInline}
```
public Paragraph getParentParagraph_IInline()
```




**Returns:**
[Paragraph](../../com.aspose.words/paragraph/)
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
### getText() {#getText}
```
public String getText()
```


Bu düğümün temsil ettiği özel karakteri alır.

 **Examples:** 

Bir DocumentVisitor uygulamasının nasıl kullanılacağını göstererek bir belgeden tüm gizli içeriği kaldırır.

```

 public void removeHiddenContentFromDocument() throws Exception {
     Document doc = new Document(getMyDir() + "Hidden content.docx");
     RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

     // Below are three types of fields which can accept a document visitor,
     // which will allow it to visit the accepting node, and then traverse its child nodes in a depth-first manner.
     // 1 -  Paragraph node:
     Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 4, true);
     para.accept(hiddenContentRemover);

     // 2 -  Table node:
     Table table = doc.getFirstSection().getBody().getTables().get(0);
     table.accept(hiddenContentRemover);

     // 3 -  Document node:
     doc.accept(hiddenContentRemover);

     doc.save(getArtifactsDir() + "Font.RemoveHiddenContentFromDocument.docx");
 }

 /// 
 /// Removes all visited nodes marked as "hidden content".
 /// 
 public static class RemoveHiddenContentVisitor extends DocumentVisitor {
     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(FieldStart fieldStart) {
         if (fieldStart.getFont().getHidden())
             fieldStart.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(FieldEnd fieldEnd) {
         if (fieldEnd.getFont().getHidden())
             fieldEnd.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(FieldSeparator fieldSeparator) {
         if (fieldSeparator.getFont().getHidden())
             fieldSeparator.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(Run run) {
         if (run.getFont().getHidden())
             run.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(Paragraph paragraph) {
         if (paragraph.getParagraphBreakFont().getHidden())
             paragraph.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FormField is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         if (formField.getFont().getHidden())
             formField.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a GroupShape is encountered in the document.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         if (groupShape.getFont().getHidden())
             groupShape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Shape is encountered in the document.
     /// 
     public int visitShapeStart(Shape shape) {
         if (shape.getFont().getHidden())
             shape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Comment is encountered in the document.
     /// 
     public int visitCommentStart(Comment comment) {
         if (comment.getFont().getHidden())
             comment.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Footnote is encountered in the document.
     /// 
     public int visitFootnoteStart(Footnote footnote) {
         if (footnote.getFont().getHidden())
             footnote.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SpecialCharacter is encountered in the document.
     /// 
     public int visitSpecialChar(SpecialChar specialChar) {
         if (specialChar.getFont().getHidden())
             specialChar.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Table node is ended in the document.
     /// 
     public int visitTableEnd(Table table) {
         // The content inside table cells may have the hidden content flag, but the tables themselves cannot.
         // If this table had nothing but hidden content, this visitor would have removed all of it,
         // and there would be no child nodes left.
         // Thus, we can also treat the table itself as hidden content and remove it.
         // Tables which are empty but do not have hidden content will have cells with empty paragraphs inside,
         // which this visitor will not remove.
         if (!table.hasChildNodes())
             table.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Cell node is ended in the document.
     /// 
     public int visitCellEnd(Cell cell) {
         if (!cell.hasChildNodes() && cell.getParentNode() != null)
             cell.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Row node is ended in the document.
     /// 
     public int visitRowEnd(Row row) {
         if (!row.hasChildNodes() && row.getParentNode() != null)
             row.remove();

         return VisitorAction.CONTINUE;
     }
 }
 
```

**Returns:**
java.lang.String - Bu düğümün temsil ettiği karakteri içeren dize.
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
### isDeleteRevision() {#isDeleteRevision}
```
public boolean isDeleteRevision()
```


Değişiklik izleme etkinken bu nesne Microsoft Word'de silinmişse true döndürür.

 **Examples:** 

Satır içi bir düğümün revizyon tipinin nasıl belirleneceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Revision runs.docx");

 // When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
 // is turned on in Microsoft Word, the changes we apply count as revisions.
 // When editing a document using Aspose.Words, we can begin tracking revisions by
 // invoking the document's "StartTrackRevisions" method and stop tracking by using the "StopTrackRevisions" method.
 // We can either accept revisions to assimilate them into the document
 // or reject them to change the proposed change effectively.
 Assert.assertEquals(6, doc.getRevisions().getCount());

 // The parent node of a revision is the run that the revision concerns. A Run is an Inline node.
 Run run = (Run) doc.getRevisions().get(0).getParentNode();

 Paragraph firstParagraph = run.getParentParagraph();
 RunCollection runs = firstParagraph.getRuns();

 Assert.assertEquals(runs.getCount(), 6);

 // Below are five types of revisions that can flag an Inline node.
 // 1 -  An "insert" revision:
 // This revision occurs when we insert text while tracking changes.
 Assert.assertTrue(runs.get(2).isInsertRevision());

 // 2 -  A "format" revision:
 // This revision occurs when we change the formatting of text while tracking changes.
 Assert.assertTrue(runs.get(2).isFormatRevision());

 // 3 -  A "move from" revision:
 // When we highlight text in Microsoft Word, and then drag it to a different place in the document
 // while tracking changes, two revisions appear.
 // The "move from" revision is a copy of the text originally before we moved it.
 Assert.assertTrue(runs.get(4).isMoveFromRevision());

 // 4 -  A "move to" revision:
 // The "move to" revision is the text that we moved in its new position in the document.
 // "Move from" and "move to" revisions appear in pairs for every move revision we carry out.
 // Accepting a move revision deletes the "move from" revision and its text,
 // and keeps the text from the "move to" revision.
 // Rejecting a move revision conversely keeps the "move from" revision and deletes the "move to" revision.
 Assert.assertTrue(runs.get(1).isMoveToRevision());

 // 5 -  A "delete" revision:
 // This revision occurs when we delete text while tracking changes. When we delete text like this,
 // it will stay in the document as a revision until we either accept the revision,
 // which will delete the text for good, or reject the revision, which will keep the text we deleted where it was.
 Assert.assertTrue(runs.get(5).isDeleteRevision());
 
```

**Returns:**
boolean - Değişiklik izleme etkinken bu nesne Microsoft Word'de silinmişse true.
### isDirty() {#isDirty}
```
public boolean isDirty()
```


Belgenin diğer değişiklikleri nedeniyle alanın mevcut sonucunun artık doğru (eski) olup olmadığını alır.

 **Examples:** 

Bir FieldStart düğümüyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDate field = (FieldDate) builder.insertField(FieldType.FIELD_DATE, true);
 field.getFormat().setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 FieldChar fieldStart = field.getStart();

 Assert.assertEquals(FieldType.FIELD_DATE, fieldStart.getFieldType());
 Assert.assertEquals(false, fieldStart.isDirty());
 Assert.assertEquals(false, fieldStart.isLocked());

 // Retrieve the facade object which represents the field in the document.
 field = (FieldDate) fieldStart.getField();

 Assert.assertEquals(false, field.isLocked());
 Assert.assertEquals(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());

 // Update the field to show the current date.
 field.update();
 
```

**Returns:**
boolean - Alanın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru olmaması (eski) olup olmadığı.
### isDirty(boolean value) {#isDirty-boolean}
```
public void isDirty(boolean value)
```


Belgenin diğer değişiklikleri nedeniyle alanın mevcut sonucunun artık doğru (eski) olup olmadığını ayarlar.

 **Examples:** 

Bir FieldStart düğümüyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDate field = (FieldDate) builder.insertField(FieldType.FIELD_DATE, true);
 field.getFormat().setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 FieldChar fieldStart = field.getStart();

 Assert.assertEquals(FieldType.FIELD_DATE, fieldStart.getFieldType());
 Assert.assertEquals(false, fieldStart.isDirty());
 Assert.assertEquals(false, fieldStart.isLocked());

 // Retrieve the facade object which represents the field in the document.
 field = (FieldDate) fieldStart.getField();

 Assert.assertEquals(false, field.isLocked());
 Assert.assertEquals(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());

 // Update the field to show the current date.
 field.update();
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Alanın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru olmaması (eski) olup olmadığı. |

### isFormatRevision() {#isFormatRevision}
```
public boolean isFormatRevision()
```


Değişiklik izleme etkinken nesnenin biçimlendirmesi Microsoft Word'de değiştirilmişse true döndürür.

 **Examples:** 

Satır içi bir düğümün revizyon tipinin nasıl belirleneceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Revision runs.docx");

 // When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
 // is turned on in Microsoft Word, the changes we apply count as revisions.
 // When editing a document using Aspose.Words, we can begin tracking revisions by
 // invoking the document's "StartTrackRevisions" method and stop tracking by using the "StopTrackRevisions" method.
 // We can either accept revisions to assimilate them into the document
 // or reject them to change the proposed change effectively.
 Assert.assertEquals(6, doc.getRevisions().getCount());

 // The parent node of a revision is the run that the revision concerns. A Run is an Inline node.
 Run run = (Run) doc.getRevisions().get(0).getParentNode();

 Paragraph firstParagraph = run.getParentParagraph();
 RunCollection runs = firstParagraph.getRuns();

 Assert.assertEquals(runs.getCount(), 6);

 // Below are five types of revisions that can flag an Inline node.
 // 1 -  An "insert" revision:
 // This revision occurs when we insert text while tracking changes.
 Assert.assertTrue(runs.get(2).isInsertRevision());

 // 2 -  A "format" revision:
 // This revision occurs when we change the formatting of text while tracking changes.
 Assert.assertTrue(runs.get(2).isFormatRevision());

 // 3 -  A "move from" revision:
 // When we highlight text in Microsoft Word, and then drag it to a different place in the document
 // while tracking changes, two revisions appear.
 // The "move from" revision is a copy of the text originally before we moved it.
 Assert.assertTrue(runs.get(4).isMoveFromRevision());

 // 4 -  A "move to" revision:
 // The "move to" revision is the text that we moved in its new position in the document.
 // "Move from" and "move to" revisions appear in pairs for every move revision we carry out.
 // Accepting a move revision deletes the "move from" revision and its text,
 // and keeps the text from the "move to" revision.
 // Rejecting a move revision conversely keeps the "move from" revision and deletes the "move to" revision.
 Assert.assertTrue(runs.get(1).isMoveToRevision());

 // 5 -  A "delete" revision:
 // This revision occurs when we delete text while tracking changes. When we delete text like this,
 // it will stay in the document as a revision until we either accept the revision,
 // which will delete the text for good, or reject the revision, which will keep the text we deleted where it was.
 Assert.assertTrue(runs.get(5).isDeleteRevision());
 
```

**Returns:**
boolean - Değişiklik izleme etkinken nesnenin biçimlendirmesi Microsoft Word'de değiştirilmişse true.
### isInsertRevision() {#isInsertRevision}
```
public boolean isInsertRevision()
```


Değişiklik izleme etkinken bu nesne Microsoft Word'e eklenmişse true döndürür.

 **Examples:** 

Satır içi bir düğümün revizyon tipinin nasıl belirleneceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Revision runs.docx");

 // When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
 // is turned on in Microsoft Word, the changes we apply count as revisions.
 // When editing a document using Aspose.Words, we can begin tracking revisions by
 // invoking the document's "StartTrackRevisions" method and stop tracking by using the "StopTrackRevisions" method.
 // We can either accept revisions to assimilate them into the document
 // or reject them to change the proposed change effectively.
 Assert.assertEquals(6, doc.getRevisions().getCount());

 // The parent node of a revision is the run that the revision concerns. A Run is an Inline node.
 Run run = (Run) doc.getRevisions().get(0).getParentNode();

 Paragraph firstParagraph = run.getParentParagraph();
 RunCollection runs = firstParagraph.getRuns();

 Assert.assertEquals(runs.getCount(), 6);

 // Below are five types of revisions that can flag an Inline node.
 // 1 -  An "insert" revision:
 // This revision occurs when we insert text while tracking changes.
 Assert.assertTrue(runs.get(2).isInsertRevision());

 // 2 -  A "format" revision:
 // This revision occurs when we change the formatting of text while tracking changes.
 Assert.assertTrue(runs.get(2).isFormatRevision());

 // 3 -  A "move from" revision:
 // When we highlight text in Microsoft Word, and then drag it to a different place in the document
 // while tracking changes, two revisions appear.
 // The "move from" revision is a copy of the text originally before we moved it.
 Assert.assertTrue(runs.get(4).isMoveFromRevision());

 // 4 -  A "move to" revision:
 // The "move to" revision is the text that we moved in its new position in the document.
 // "Move from" and "move to" revisions appear in pairs for every move revision we carry out.
 // Accepting a move revision deletes the "move from" revision and its text,
 // and keeps the text from the "move to" revision.
 // Rejecting a move revision conversely keeps the "move from" revision and deletes the "move to" revision.
 Assert.assertTrue(runs.get(1).isMoveToRevision());

 // 5 -  A "delete" revision:
 // This revision occurs when we delete text while tracking changes. When we delete text like this,
 // it will stay in the document as a revision until we either accept the revision,
 // which will delete the text for good, or reject the revision, which will keep the text we deleted where it was.
 Assert.assertTrue(runs.get(5).isDeleteRevision());
 
```

**Returns:**
boolean - Değişiklik izleme etkinken bu nesne Microsoft Word'e eklenmişse true.
### isLocked() {#isLocked}
```
public boolean isLocked()
```


Üst alanın kilitli olup olmadığını alır (sonucu yeniden hesaplamamalıdır).

 **Examples:** 

Bir FieldStart düğümüyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDate field = (FieldDate) builder.insertField(FieldType.FIELD_DATE, true);
 field.getFormat().setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 FieldChar fieldStart = field.getStart();

 Assert.assertEquals(FieldType.FIELD_DATE, fieldStart.getFieldType());
 Assert.assertEquals(false, fieldStart.isDirty());
 Assert.assertEquals(false, fieldStart.isLocked());

 // Retrieve the facade object which represents the field in the document.
 field = (FieldDate) fieldStart.getField();

 Assert.assertEquals(false, field.isLocked());
 Assert.assertEquals(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());

 // Update the field to show the current date.
 field.update();
 
```

**Returns:**
boolean - Üst alanın kilitli olup olmadığı (sonucu yeniden hesaplamamalıdır).
### isLocked(boolean value) {#isLocked-boolean}
```
public void isLocked(boolean value)
```


Üst alanın kilitli olup olmadığını ayarlar (sonucu yeniden hesaplamamalıdır).

 **Examples:** 

Bir FieldStart düğümüyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDate field = (FieldDate) builder.insertField(FieldType.FIELD_DATE, true);
 field.getFormat().setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 FieldChar fieldStart = field.getStart();

 Assert.assertEquals(FieldType.FIELD_DATE, fieldStart.getFieldType());
 Assert.assertEquals(false, fieldStart.isDirty());
 Assert.assertEquals(false, fieldStart.isLocked());

 // Retrieve the facade object which represents the field in the document.
 field = (FieldDate) fieldStart.getField();

 Assert.assertEquals(false, field.isLocked());
 Assert.assertEquals(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());

 // Update the field to show the current date.
 field.update();
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Üst alanın kilitli olup olmadığı (sonucu yeniden hesaplamamalıdır). |

### isMoveFromRevision() {#isMoveFromRevision}
```
public boolean isMoveFromRevision()
```


Değişiklik izleme etkinken bu nesne Microsoft Word'de taşınmış (silinmiş) ise  true  döndürür.

 **Examples:** 

Satır içi bir düğümün revizyon tipinin nasıl belirleneceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Revision runs.docx");

 // When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
 // is turned on in Microsoft Word, the changes we apply count as revisions.
 // When editing a document using Aspose.Words, we can begin tracking revisions by
 // invoking the document's "StartTrackRevisions" method and stop tracking by using the "StopTrackRevisions" method.
 // We can either accept revisions to assimilate them into the document
 // or reject them to change the proposed change effectively.
 Assert.assertEquals(6, doc.getRevisions().getCount());

 // The parent node of a revision is the run that the revision concerns. A Run is an Inline node.
 Run run = (Run) doc.getRevisions().get(0).getParentNode();

 Paragraph firstParagraph = run.getParentParagraph();
 RunCollection runs = firstParagraph.getRuns();

 Assert.assertEquals(runs.getCount(), 6);

 // Below are five types of revisions that can flag an Inline node.
 // 1 -  An "insert" revision:
 // This revision occurs when we insert text while tracking changes.
 Assert.assertTrue(runs.get(2).isInsertRevision());

 // 2 -  A "format" revision:
 // This revision occurs when we change the formatting of text while tracking changes.
 Assert.assertTrue(runs.get(2).isFormatRevision());

 // 3 -  A "move from" revision:
 // When we highlight text in Microsoft Word, and then drag it to a different place in the document
 // while tracking changes, two revisions appear.
 // The "move from" revision is a copy of the text originally before we moved it.
 Assert.assertTrue(runs.get(4).isMoveFromRevision());

 // 4 -  A "move to" revision:
 // The "move to" revision is the text that we moved in its new position in the document.
 // "Move from" and "move to" revisions appear in pairs for every move revision we carry out.
 // Accepting a move revision deletes the "move from" revision and its text,
 // and keeps the text from the "move to" revision.
 // Rejecting a move revision conversely keeps the "move from" revision and deletes the "move to" revision.
 Assert.assertTrue(runs.get(1).isMoveToRevision());

 // 5 -  A "delete" revision:
 // This revision occurs when we delete text while tracking changes. When we delete text like this,
 // it will stay in the document as a revision until we either accept the revision,
 // which will delete the text for good, or reject the revision, which will keep the text we deleted where it was.
 Assert.assertTrue(runs.get(5).isDeleteRevision());
 
```

**Returns:**
boolean -  true  eğer bu nesne Microsoft Word'de taşınmış (silinmiş) ise.
### isMoveToRevision() {#isMoveToRevision}
```
public boolean isMoveToRevision()
```


Değişiklik izleme etkinken bu nesne Microsoft Word'de taşınmış (eklenmiş) ise  true  döndürür.

 **Examples:** 

Satır içi bir düğümün revizyon tipinin nasıl belirleneceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Revision runs.docx");

 // When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
 // is turned on in Microsoft Word, the changes we apply count as revisions.
 // When editing a document using Aspose.Words, we can begin tracking revisions by
 // invoking the document's "StartTrackRevisions" method and stop tracking by using the "StopTrackRevisions" method.
 // We can either accept revisions to assimilate them into the document
 // or reject them to change the proposed change effectively.
 Assert.assertEquals(6, doc.getRevisions().getCount());

 // The parent node of a revision is the run that the revision concerns. A Run is an Inline node.
 Run run = (Run) doc.getRevisions().get(0).getParentNode();

 Paragraph firstParagraph = run.getParentParagraph();
 RunCollection runs = firstParagraph.getRuns();

 Assert.assertEquals(runs.getCount(), 6);

 // Below are five types of revisions that can flag an Inline node.
 // 1 -  An "insert" revision:
 // This revision occurs when we insert text while tracking changes.
 Assert.assertTrue(runs.get(2).isInsertRevision());

 // 2 -  A "format" revision:
 // This revision occurs when we change the formatting of text while tracking changes.
 Assert.assertTrue(runs.get(2).isFormatRevision());

 // 3 -  A "move from" revision:
 // When we highlight text in Microsoft Word, and then drag it to a different place in the document
 // while tracking changes, two revisions appear.
 // The "move from" revision is a copy of the text originally before we moved it.
 Assert.assertTrue(runs.get(4).isMoveFromRevision());

 // 4 -  A "move to" revision:
 // The "move to" revision is the text that we moved in its new position in the document.
 // "Move from" and "move to" revisions appear in pairs for every move revision we carry out.
 // Accepting a move revision deletes the "move from" revision and its text,
 // and keeps the text from the "move to" revision.
 // Rejecting a move revision conversely keeps the "move from" revision and deletes the "move to" revision.
 Assert.assertTrue(runs.get(1).isMoveToRevision());

 // 5 -  A "delete" revision:
 // This revision occurs when we delete text while tracking changes. When we delete text like this,
 // it will stay in the document as a revision until we either accept the revision,
 // which will delete the text for good, or reject the revision, which will keep the text we deleted where it was.
 Assert.assertTrue(runs.get(5).isDeleteRevision());
 
```

**Returns:**
boolean -  true  eğer bu nesne Microsoft Word'de değişiklik izleme etkinken taşındıysa (eklenmişse).
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

### removeMoveRevisions() {#removeMoveRevisions}
```
public void removeMoveRevisions()
```




### removeRunAttr(int key) {#removeRunAttr-int}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

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

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int key, Object value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |
| değer | java.lang.Object |  |

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
