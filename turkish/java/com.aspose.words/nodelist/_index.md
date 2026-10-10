---
title: "NodeList"
linktitle: "NodeList"
second_title: "Aspose.Words Java için"
description: "Java'da CompositeNode.selectNodesjava.lang.String yöntemi kullanılarak yürütülen bir XPath sorgusuyla eşleşen düğümlerin bir koleksiyonunu temsil eder."
type: docs
weight: 481
url: /tr/java/com.aspose.words/nodelist/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class NodeList implements Iterable
```

XPath sorgusuyla eşleşen düğümlerin bir koleksiyonunu, [CompositeNode.selectNodes(java.lang.String)](../../com.aspose.words/compositenode/\\#selectNodes-java.lang.String) yöntemi kullanılarak temsil eder.

Daha fazla bilgi edinmek için, [ Aspose.Words Document Object Model (DOM) ][Aspose.Words Document Object Model _DOM_] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

[NodeList](../../com.aspose.words/nodelist/) is returned by [CompositeNode.selectNodes(java.lang.String)](../../com.aspose.words/compositenode/\#selectNodes-java.lang.String) and contains a collection of nodes matching the XPath query.

[NodeList](../../com.aspose.words/nodelist/) supports indexed access and iteration.

[NodeList](../../com.aspose.words/nodelist/) koleksiyonunu bir \"snapshot\" koleksiyonu gibi ele alın. [NodeList](../../com.aspose.words/nodelist/) bir \"live\" koleksiyon olarak başlar çünkü XPath sorgusu çalıştırıldığında düğümler gerçekte alınmaz. Düğümler yalnızca erişildiğinde alınır ve bu sırada düğüm ve ondan önceki tüm düğümler önbelleğe alınarak bir \"snapshot\" koleksiyonu oluşturulur.

 **Examples:** 

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


[Aspose.Words Document Object Model _DOM_]: https://docs.aspose.com/words/java/aspose-words-document-object-model/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get(int index)](#get-int) | Verilen indeksdeki bir düğümü alır. |
| [getCount()](#getCount) | Listedeki düğüm sayısını alır. |
| [iterator()](#iterator) | Düğümlerin koleksiyonu üzerinde basit bir "foreach" tarzı yineleme sağlar. |
| [toArray()](#toArray) | Koleksiyondaki tüm düğümleri yeni bir düğüm dizisine kopyalar. |
### get(int index) {#get-int}
```
public Node get(int index)
```


Verilen indeksdeki bir düğümü alır.

 **Remarks:** 

Dizin sıfır tabanlıdır.

Negatif dizinlere izin verilir ve koleksiyonun sonundan erişimi gösterir. Örneğin -1 son öğeyi, -2 sondan bir önceki öğeyi ve böyle devam eder.

Eğer dizin listedeki öğe sayısına eşit veya daha büyükse, bu null referans döndürür.

Eğer dizin negatifse ve mutlak değeri listedeki öğe sayısından büyükse, bu null referans döndürür.

 **Examples:** 

XPaths kullanarak bir NodeList içinde nasıl gezileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert some nodes with a DocumentBuilder.
 builder.writeln("Hello world!");

 builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endTable();

 builder.insertImage(getImageDir() + "Logo.jpg");

 // Our document contains three Run nodes.
 NodeList runs = doc.selectNodes("//Run");

 Assert.assertEquals(3, runs.getCount());

 // Use a double forward slash to select all Run nodes
 // that are indirect descendants of a Table node, which would be the runs inside the two cells we inserted.
 runs = doc.selectNodes("//Table//Run");

 Assert.assertEquals(2, runs.getCount());

 // Single forward slashes specify direct descendant relationships,
 // which we skipped when we used double slashes.
 Assert.assertEquals(doc.selectNodes("//Table//Run"),
         doc.selectNodes("//Table/Row/Cell/Paragraph/Run"));

 // Access the shape that contains the image we inserted.
 NodeList shapes = doc.selectNodes("//Shape");

 Assert.assertEquals(1, shapes.getCount());

 Shape shape = (Shape) shapes.get(0);
 Assert.assertTrue(shape.hasImage());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int | Düğüm listesindeki bir indeks. |

**Returns:**
[Node](../../com.aspose.words/node/) - The corresponding [Node](../../com.aspose.words/node/) value.
### getCount() {#getCount}
```
public int getCount()
```


Listedeki düğüm sayısını alır.

 **Examples:** 

XPaths kullanarak bir NodeList içinde nasıl gezileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert some nodes with a DocumentBuilder.
 builder.writeln("Hello world!");

 builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endTable();

 builder.insertImage(getImageDir() + "Logo.jpg");

 // Our document contains three Run nodes.
 NodeList runs = doc.selectNodes("//Run");

 Assert.assertEquals(3, runs.getCount());

 // Use a double forward slash to select all Run nodes
 // that are indirect descendants of a Table node, which would be the runs inside the two cells we inserted.
 runs = doc.selectNodes("//Table//Run");

 Assert.assertEquals(2, runs.getCount());

 // Single forward slashes specify direct descendant relationships,
 // which we skipped when we used double slashes.
 Assert.assertEquals(doc.selectNodes("//Table//Run"),
         doc.selectNodes("//Table/Row/Cell/Paragraph/Run"));

 // Access the shape that contains the image we inserted.
 NodeList shapes = doc.selectNodes("//Shape");

 Assert.assertEquals(1, shapes.getCount());

 Shape shape = (Shape) shapes.get(0);
 Assert.assertTrue(shape.hasImage());
 
```

**Returns:**
int - Listedeki düğüm sayısı.
### iterator() {#iterator}
```
public Iterator iterator()
```


Düğümlerin koleksiyonu üzerinde basit bir "foreach" tarzı yineleme sağlar.

 **Examples:** 

XPath ifadesi kullanarak belirli düğümlerin nasıl seçileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 // This expression will extract all paragraph nodes,
 // which are descendants of any table node in the document.
 NodeList nodeList = doc.selectNodes("//Table//Paragraph");

 // Iterate through the list with an enumerator and print the contents of every paragraph in each cell of the table.
 int index = 0;

 Iterator e = nodeList.iterator();
 while (e.hasNext()) {
     Node currentNode = e.next();
     System.out.println(MessageFormat.format("Table paragraph index {0}, contents: \"{1}\"", index++, currentNode.getText().trim()));
 }

 // This expression will select any paragraphs that are direct children of any Body node in the document.
 nodeList = doc.selectNodes("//Body/Paragraph");

 // We can treat the list as an array.
 Assert.assertEquals(nodeList.toArray().length, 4);

 // Use SelectSingleNode to select the first result of the same expression as above.
 Node node = doc.selectSingleNode("//Body/Paragraph");

 Assert.assertEquals(Paragraph.class, node.getClass());
 
```

**Returns:**
java.util.Iterator - Bir Iterator.
### toArray() {#toArray}
```
public Node[] toArray()
```


Koleksiyondaki tüm düğümleri yeni bir düğüm dizisine kopyalar.

 **Remarks:** 

Düğümler koleksiyonunu iterasyon sırasında eklememeli/kaldırmamalısınız çünkü bu, yineleyiciyi geçersiz kılar ve canlı koleksiyonlar için yenileme gerektirir.

Iterasyon sırasında düğüm ekleyip/çıkarmak için, bu yöntemi kullanarak düğümleri sabit boyutlu bir diziye kopyalayın ve ardından dizi üzerinde yineleyin.

 **Examples:** 

XPath ifadesi kullanarak belirli düğümlerin nasıl seçileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 // This expression will extract all paragraph nodes,
 // which are descendants of any table node in the document.
 NodeList nodeList = doc.selectNodes("//Table//Paragraph");

 // Iterate through the list with an enumerator and print the contents of every paragraph in each cell of the table.
 int index = 0;

 Iterator e = nodeList.iterator();
 while (e.hasNext()) {
     Node currentNode = e.next();
     System.out.println(MessageFormat.format("Table paragraph index {0}, contents: \"{1}\"", index++, currentNode.getText().trim()));
 }

 // This expression will select any paragraphs that are direct children of any Body node in the document.
 nodeList = doc.selectNodes("//Body/Paragraph");

 // We can treat the list as an array.
 Assert.assertEquals(nodeList.toArray().length, 4);

 // Use SelectSingleNode to select the first result of the same expression as above.
 Node node = doc.selectSingleNode("//Body/Paragraph");

 Assert.assertEquals(Paragraph.class, node.getClass());
 
```

**Returns:**
com.aspose.words.Node[] - Düğümlerin bir dizisi.
