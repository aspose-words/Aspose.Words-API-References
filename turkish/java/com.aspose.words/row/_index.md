---
title: "Satır"
linktitle: "Satır"
second_title: "Aspose.Words Java için"
description: "Java'da bir tablo satırını temsil eder."
type: docs
weight: 588
url: /tr/java/com.aspose.words/row/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node/), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode/)
```
public class Row extends CompositeNode
```

Bir tablo satırını temsil eder.

Daha fazla bilgi için, [ Working with Tables ][Working with Tables] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

[Row](../../com.aspose.words/row/) can only be a child of a [Table](../../com.aspose.words/table/).

[Row](../../com.aspose.words/row/) can contain one or more [Cell](../../com.aspose.words/cell/) nodes.

Geçerli bir minimal satırın en az bir [Cell](../../com.aspose.words/cell/) içermesi gerekir.

 **Examples:** 

Bir tablo oluşturmanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 Table table = new Table(doc);
 doc.getFirstSection().getBody().appendChild(table);

 // Tables contain rows, which contain cells, which may have paragraphs
 // with typical elements such as runs, shapes, and even other tables.
 // Calling the "EnsureMinimum" method on a table will ensure that
 // the table has at least one row, cell, and paragraph.
 Row firstRow = new Row(doc);
 table.appendChild(firstRow);

 Cell firstCell = new Cell(doc);
 firstRow.appendChild(firstCell);

 Paragraph paragraph = new Paragraph(doc);
 firstCell.appendChild(paragraph);

 // Add text to the first cell in the first row of the table.
 Run run = new Run(doc, "Hello world!");
 paragraph.appendChild(run);

 doc.save(getArtifactsDir() + "Table.CreateTable.docx");
 
```

Belgedeki tüm tabloları nasıl döngüyle gezileceğini ve her hücrenin içeriğinin nasıl yazdırılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Tables.docx");
 TableCollection tables = doc.getFirstSection().getBody().getTables();

 Assert.assertEquals(2, tables.toArray().length);

 for (int i = 0; i < tables.getCount(); i++) {
     System.out.println(MessageFormat.format("Start of Table {0}", i));

     RowCollection rows = tables.get(i).getRows();

     for (int j = 0; j < rows.getCount(); j++) {
         System.out.println(MessageFormat.format("\tStart of Row {0}", j));

         CellCollection cells = rows.get(j).getCells();

         for (int k = 0; k < cells.getCount(); k++) {
             String cellText = cells.get(k).toString(SaveFormat.TEXT).trim();
             System.out.println(MessageFormat.format("\t\tContents of Cell:{0} = \"{1}\"", k, cellText));
         }

         System.out.println(MessageFormat.format("\tEnd of Row {0}", j));
     }

     System.out.println(MessageFormat.format("End of Table {0}\n", i));
 }
 
```

Bir belge oluşturucu kullanmadan iç içe bir tablo oluşturmanın nasıl yapılacağını gösterir.

```

 public void createNestedTable() throws Exception {
     Document doc = new Document();

     // Create the outer table with three rows and four columns, and then add it to the document.
     Table outerTable = createTable(doc, 3, 4, "Outer Table");
     doc.getFirstSection().getBody().appendChild(outerTable);

     // Create another table with two rows and two columns and then insert it into the first table's first cell.
     Table innerTable = createTable(doc, 2, 2, "Inner Table");
     outerTable.getFirstRow().getFirstCell().appendChild(innerTable);

     doc.save(getArtifactsDir() + "Table.CreateNestedTable.docx");
 }

 // Creates a new table in the document with the given dimensions and text in each cell.
 private Table createTable(final Document doc, final int rowCount, final int cellCount, final String cellText) throws Exception {
     Table table = new Table(doc);

     for (int rowId = 1; rowId <= rowCount; rowId++) {
         Row row = new Row(doc);
         table.appendChild(row);

         for (int cellId = 1; cellId <= cellCount; cellId++) {
             Cell cell = new Cell(doc);
             cell.appendChild(new Paragraph(doc));
             cell.getFirstParagraph().appendChild(new Run(doc, cellText));

             row.appendChild(cell);
         }
     }

     // You can use the "Title" and "Description" properties to add a title and description respectively to your table.
     // The table must have at least one row before we can use these properties.
     // These properties are meaningful for ISO / IEC 29500 compliant .docx documents (see the OoxmlCompliance class).
     // If we save the document to pre-ISO/IEC 29500 formats, Microsoft Word ignores these properties.
     table.setTitle("Aspose table title");
     table.setDescription("Aspose table description");

     return table;
 }
 
```


[Working with Tables]: https://docs.aspose.com/words/java/working-with-tables/
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [Row(DocumentBase doc)](#Row-com.aspose.words.DocumentBase) | [Row](../../com.aspose.words/row/) sınıfının yeni bir örneğini başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor) | Bir ziyaretçiyi kabul eder. |
| [acceptEnd(DocumentVisitor visitor)](#acceptEnd-com.aspose.words.DocumentVisitor) | Satırın sonunu ziyaret etmek için bir ziyaretçiyi kabul eder. |
| [acceptStart(DocumentVisitor visitor)](#acceptStart-com.aspose.words.DocumentVisitor) | Satırın başlangıcını ziyaret etmek için bir ziyaretçiyi kabul eder. |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node) | Belirtilen düğümü bu düğümün alt düğüm listesine sonuna ekler. |
| [clearRowAttrs()](#clearRowAttrs) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean) | Düğümün bir kopyasını oluşturur. |
| [ensureMinimum()](#ensureMinimum) | Eğer [Row](../../com.aspose.words/row/) içinde hücre yoksa, bir [Cell](../../com.aspose.words/cell/) oluşturur ve ekler. |
| [fetchInheritedRowAttr(int key)](#fetchInheritedRowAttr-int) |  |
| [fetchRowAttr(int key)](#fetchRowAttr-int) |  |
| [getAncestor(int ancestorType)](#getAncestor-int) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class) | Belirtilen nesne tipinin ilk atasını alır. |
| [getCells()](#getCells) | Satırın [Cell](../../com.aspose.words/cell/) alt düğümlerine tipli erişim sağlar. |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean) |  |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean) |  |
| [getContainer()](#getContainer) |  |
| [getCount()](#getCount) | Bu düğümün doğrudan alt öğelerinin sayısını alır. |
| [getCurrentNode()](#getCurrentNode) |  |
| [getCustomNodeId()](#getCustomNodeId) | Özel düğüm tanımlayıcısını belirtir. |
| [getDirectRowAttr(int key)](#getDirectRowAttr-int) |  |
| [getDocument()](#getDocument) | Bu düğümün ait olduğu belgeyi alır. |
| [getFirstCell()](#getFirstCell) | Satırdaki ilk [Cell](../../com.aspose.words/cell/) öğesini döndürür. |
| [getFirstChild()](#getFirstChild) | Düğümün ilk alt öğesini alır. |
| [getHidden()](#getHidden) | Bu satırın gizli olup olmadığını gösteren bir bayrağı alır. |
| [getLastCell()](#getLastCell) | Satırdaki son [Cell](../../com.aspose.words/cell/) öğesini döndürür. |
| [getLastChild()](#getLastChild) | Düğümün son alt öğesini alır. |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node) |  |
| [getNextRow()](#getNextRow) | Sonraki [Row](../../com.aspose.words/row/) düğümünü alır. |
| [getNextSibling()](#getNextSibling) | Bu düğümü hemen izleyen düğümü alır. |
| [getNodeType()](#getNodeType) | Döndürür [NodeType.ROW](../../com.aspose.words/nodetype/\#ROW). |
| [getParentNode()](#getParentNode) | Bu düğümün hemen üst ebeveynini alır. |
| [getParentTable()](#getParentTable) | Satırın doğrudan üst tabloyu döndürür. |
| [getPreviousRow()](#getPreviousRow) | Önceki [Row](../../com.aspose.words/row/) düğümünü alır. |
| [getPreviousSibling()](#getPreviousSibling) | Bu düğümden hemen önce gelen düğümü alır. |
| [getRange()](#getRange) | Bu düğümde bulunan bir belgenin bölümünü temsil eden bir [Range](../../com.aspose.words/range/) nesnesini döndürür. |
| [getRowFormat()](#getRowFormat) | Satırın biçimlendirme özelliklerine erişim sağlar. |
| [getText()](#getText) | Bu satırdaki tüm hücrelerin metnini, satır sonu karakteri dahil olmak üzere alır. |
| [hasChildNodes()](#hasChildNodes) | Bu düğümün herhangi bir alt düğümü varsa  true  döndürür. |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node) | Belirtilen alt düğümün alt düğüm dizisindeki dizinini döndürür. |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node) | Belirtilen düğümü, belirtilen referans düğümünden hemen sonra ekler. |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node) | Belirtilen düğümü, belirtilen referans düğümünden hemen önce ekler. |
| [isComposite()](#isComposite) | Bu düğümün alt düğüm alabileceği için  true  döndürür. |
| [isFirstRow()](#isFirstRow) | Bir tabloda bu ilk satırsa true; aksi takdirde false. |
| [isLastRow()](#isLastRow) | Bir tabloda bu son satırsa true; aksi takdirde false. |
| [iterator()](#iterator) | Bu düğümün alt düğümleri üzerinde foreach tarzı yineleme desteği sağlar. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node) | Ön sipariş ağaç dolaşım algoritmasına göre bir sonraki düğümü alır. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int) |  |
| [prependChild(Node newChild)](#prependChild-com.aspose.words.Node) | Belirtilen düğümü, bu düğümün alt düğüm listesinin başına ekler. |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node) | Ön sipariş ağaç dolaşım algoritmasına göre önceki düğümü alır. |
| [remove()](#remove) | Kendisini ebeveyninden kaldırır. |
| [removeAllChildren()](#removeAllChildren) | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [removeChild(Node oldChild)](#removeChild-com.aspose.words.Node) | Belirtilen alt düğümü kaldırır. |
| [removeMoveRevisions()](#removeMoveRevisions) |  |
| [removeSmartTags()](#removeSmartTags) | Geçerli düğümün tüm [SmartTag](../../com.aspose.words/smarttag/) alt düğümlerini kaldırır. |
| [resetToDefaultAttrs()](#resetToDefaultAttrs) |  |
| [selectNodes(String xpath)](#selectNodes-java.lang.String) | XPath ifadesiyle eşleşen düğüm listesini seçer. |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String) | XPath ifadesiyle eşleşen ilk [Node](../../com.aspose.words/node/) öğesini seçer. |
| [setCustomNodeId(int value)](#setCustomNodeId-int) | Özel düğüm tanımlayıcısını belirtir. |
| [setHidden(boolean value)](#setHidden-boolean) | Bu satırın gizli olup olmadığını belirten bir bayrak ayarlar. |
| [setRowAttr(int key, Object value)](#setRowAttr-int-java.lang.Object) |  |
| [toString()](#toString) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions) | Düğümün içeriğini belirtilen kaydetme seçeneklerini kullanarak bir dizeye dışa aktarır. |
| [toString(int saveFormat)](#toString-int) |  |
### Row(DocumentBase doc) {#Row-com.aspose.words.DocumentBase}
```
public Row(DocumentBase doc)
```


[Row](../../com.aspose.words/row/) sınıfının yeni bir örneğini başlatır.

 **Remarks:** 

Bir [Row](../../com.aspose.words/row/) oluşturulduğunda, belirtilen belgeye aittir, ancak henüz belgenin bir parçası değildir ve [Node.getParentNode()](../../com.aspose.words/node/\#getParentNode)  null  dır.

Bir belgeye [Row](../../com.aspose.words/row/) eklemek için, satırın eklenmesini istediğiniz tabloda [CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertAfter-com.aspose.words.Node--com.aspose.words.Node) veya [CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertBefore-com.aspose.words.Node--com.aspose.words.Node) kullanın.

 **Examples:** 

Bir belge oluşturucu kullanmadan iç içe bir tablo oluşturmanın nasıl yapılacağını gösterir.

```

 public void createNestedTable() throws Exception {
     Document doc = new Document();

     // Create the outer table with three rows and four columns, and then add it to the document.
     Table outerTable = createTable(doc, 3, 4, "Outer Table");
     doc.getFirstSection().getBody().appendChild(outerTable);

     // Create another table with two rows and two columns and then insert it into the first table's first cell.
     Table innerTable = createTable(doc, 2, 2, "Inner Table");
     outerTable.getFirstRow().getFirstCell().appendChild(innerTable);

     doc.save(getArtifactsDir() + "Table.CreateNestedTable.docx");
 }

 // Creates a new table in the document with the given dimensions and text in each cell.
 private Table createTable(final Document doc, final int rowCount, final int cellCount, final String cellText) throws Exception {
     Table table = new Table(doc);

     for (int rowId = 1; rowId <= rowCount; rowId++) {
         Row row = new Row(doc);
         table.appendChild(row);

         for (int cellId = 1; cellId <= cellCount; cellId++) {
             Cell cell = new Cell(doc);
             cell.appendChild(new Paragraph(doc));
             cell.getFirstParagraph().appendChild(new Run(doc, cellText));

             row.appendChild(cell);
         }
     }

     // You can use the "Title" and "Description" properties to add a title and description respectively to your table.
     // The table must have at least one row before we can use these properties.
     // These properties are meaningful for ISO / IEC 29500 compliant .docx documents (see the OoxmlCompliance class).
     // If we save the document to pre-ISO/IEC 29500 formats, Microsoft Word ignores these properties.
     table.setTitle("Aspose table title");
     table.setDescription("Aspose table description");

     return table;
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase/) | Sahip belge. |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor}
```
public boolean accept(DocumentVisitor visitor)
```


Bir ziyaretçiyi kabul eder.

 **Remarks:** 

Bu düğüm ve tüm çocukları üzerinde yineleme yapar. Her düğüm, [DocumentVisitor](../../com.aspose.words/documentvisitor/) üzerindeki ilgili yöntemi çağırır.

Daha fazla bilgi için Visitor tasarım desenine bakın.

[DocumentVisitor.visitRowStart(com.aspose.words.Row)](../../com.aspose.words/documentvisitor/\#visitRowStart-com.aspose.words.Row) metodunu çağırır, ardından bölümün tüm alt düğümleri için [Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node/\#accept-com.aspose.words.DocumentVisitor) metodunu çağırır ve sonunda [DocumentVisitor.visitRowEnd(com.aspose.words.Row)](../../com.aspose.words/documentvisitor/\#visitRowEnd-com.aspose.words.Row) metodunu çağırır.

 **Examples:** 

Bir belgedeki her tablonun düğüm yapısını nasıl yazdıracağınızı gösterir.

```

 public void tableToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     TableStructurePrinter visitor = new TableStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered Table nodes and their children.
 /// 
 public static class TableStructurePrinter extends DocumentVisitor {
     public TableStructurePrinter() {
         mVisitedTables = new StringBuilder();
         mVisitorIsInsideTable = false;
     }

     public String getText() {
         return mVisitedTables.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// Runs that are not within tables are not recorded.
     /// 
     public int visitRun(Run run) {
         if (mVisitorIsInsideTable) indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Table is encountered in the document.
     /// 
     public int visitTableStart(final Table table) {
         int rows = 0;
         int columns = 0;

         if (table.getRows().getCount() > 0) {
             rows = table.getRows().getCount();
             columns = table.getFirstRow().getCount();
         }

         indentAndAppendLine("[Table start] Size: " + rows + "x" + columns);
         mDocTraversalDepth++;
         mVisitorIsInsideTable = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Table node have been visited.
     /// 
     public int visitTableEnd(final Table table) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Table end]");
         mVisitorIsInsideTable = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Row node is encountered in the document.
     /// 
     public int visitRowStart(final Row row) {
         String rowContents = row.getText().replaceAll("\\u0007", ", ").replaceAll(", , ", "");
         int rowWidth = row.indexOf(row.getLastCell()) + 1;
         int rowIndex = row.getParentTable().indexOf(row);
         String rowStatusInTable = row.isFirstRow() && row.isLastRow() ? "only" : row.isFirstRow() ? "first" : row.isLastRow() ? "last" : "";
         if (!"".equals(rowStatusInTable)) {
             rowStatusInTable = MessageFormat.format(", the {0} row in this table,", rowStatusInTable);
         }

         indentAndAppendLine(MessageFormat.format("[Row start] Row #{0}{1} width {2}, \"{3}\"", ++rowIndex, rowStatusInTable, rowWidth, rowContents));
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Row node have been visited.
     /// 
     public int visitRowEnd(final Row row) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Row end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Cell node is encountered in the document.
     /// 
     public int visitCellStart(final Cell cell) {
         Row row = cell.getParentRow();
         Table table = row.getParentTable();
         String cellStatusInRow = cell.isFirstCell() && cell.isLastCell() ? "only" : cell.isFirstCell() ? "first" : cell.isLastCell() ? "last" : "";
         if (!"".equals(cellStatusInRow)) {
             cellStatusInRow = MessageFormat.format(", the {0} cell in this row", cellStatusInRow);
         }

         indentAndAppendLine(MessageFormat.format("[Cell start] Row {0}, Col {1}{2}", table.indexOf(row) + 1, row.indexOf(cell) + 1, cellStatusInRow));
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Cell node have been visited.
     /// 
     public int visitCellEnd(final Cell cell) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Cell end]");
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is
     /// into the current table's tree of child nodes.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mVisitedTables.append("|  ");
         }

         mVisitedTables.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideTable;
     private int mDocTraversalDepth;
     private final  StringBuilder mVisitedTables;
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | Düğümleri ziyaret edecek ziyaretçi. |

**Returns:**
boolean - Tüm düğümler ziyaret edildiyse true; [DocumentVisitor](../../com.aspose.words/documentvisitor/) tüm düğümleri ziyaret etmeden işlemi durdurduysa false.
### acceptEnd(DocumentVisitor visitor) {#acceptEnd-com.aspose.words.DocumentVisitor}
```
public int acceptEnd(DocumentVisitor visitor)
```


Satırın sonunu ziyaret etmek için bir ziyaretçiyi kabul eder.

 **Examples:** 

Bir belgedeki her tablonun düğüm yapısını nasıl yazdıracağınızı gösterir.

```

 public void tableToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     TableStructurePrinter visitor = new TableStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered Table nodes and their children.
 /// 
 public static class TableStructurePrinter extends DocumentVisitor {
     public TableStructurePrinter() {
         mVisitedTables = new StringBuilder();
         mVisitorIsInsideTable = false;
     }

     public String getText() {
         return mVisitedTables.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// Runs that are not within tables are not recorded.
     /// 
     public int visitRun(Run run) {
         if (mVisitorIsInsideTable) indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Table is encountered in the document.
     /// 
     public int visitTableStart(final Table table) {
         int rows = 0;
         int columns = 0;

         if (table.getRows().getCount() > 0) {
             rows = table.getRows().getCount();
             columns = table.getFirstRow().getCount();
         }

         indentAndAppendLine("[Table start] Size: " + rows + "x" + columns);
         mDocTraversalDepth++;
         mVisitorIsInsideTable = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Table node have been visited.
     /// 
     public int visitTableEnd(final Table table) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Table end]");
         mVisitorIsInsideTable = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Row node is encountered in the document.
     /// 
     public int visitRowStart(final Row row) {
         String rowContents = row.getText().replaceAll("\\u0007", ", ").replaceAll(", , ", "");
         int rowWidth = row.indexOf(row.getLastCell()) + 1;
         int rowIndex = row.getParentTable().indexOf(row);
         String rowStatusInTable = row.isFirstRow() && row.isLastRow() ? "only" : row.isFirstRow() ? "first" : row.isLastRow() ? "last" : "";
         if (!"".equals(rowStatusInTable)) {
             rowStatusInTable = MessageFormat.format(", the {0} row in this table,", rowStatusInTable);
         }

         indentAndAppendLine(MessageFormat.format("[Row start] Row #{0}{1} width {2}, \"{3}\"", ++rowIndex, rowStatusInTable, rowWidth, rowContents));
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Row node have been visited.
     /// 
     public int visitRowEnd(final Row row) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Row end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Cell node is encountered in the document.
     /// 
     public int visitCellStart(final Cell cell) {
         Row row = cell.getParentRow();
         Table table = row.getParentTable();
         String cellStatusInRow = cell.isFirstCell() && cell.isLastCell() ? "only" : cell.isFirstCell() ? "first" : cell.isLastCell() ? "last" : "";
         if (!"".equals(cellStatusInRow)) {
             cellStatusInRow = MessageFormat.format(", the {0} cell in this row", cellStatusInRow);
         }

         indentAndAppendLine(MessageFormat.format("[Cell start] Row {0}, Col {1}{2}", table.indexOf(row) + 1, row.indexOf(cell) + 1, cellStatusInRow));
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Cell node have been visited.
     /// 
     public int visitCellEnd(final Cell cell) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Cell end]");
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is
     /// into the current table's tree of child nodes.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mVisitedTables.append("|  ");
         }

         mVisitedTables.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideTable;
     private int mDocTraversalDepth;
     private final  StringBuilder mVisitedTables;
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | Belge ziyaretçisi. |

**Returns:**
int - Ziyaretçi tarafından yapılacak eylem. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### acceptStart(DocumentVisitor visitor) {#acceptStart-com.aspose.words.DocumentVisitor}
```
public int acceptStart(DocumentVisitor visitor)
```


Satırın başlangıcını ziyaret etmek için bir ziyaretçiyi kabul eder.

 **Examples:** 

Bir belgedeki her tablonun düğüm yapısını nasıl yazdıracağınızı gösterir.

```

 public void tableToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     TableStructurePrinter visitor = new TableStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered Table nodes and their children.
 /// 
 public static class TableStructurePrinter extends DocumentVisitor {
     public TableStructurePrinter() {
         mVisitedTables = new StringBuilder();
         mVisitorIsInsideTable = false;
     }

     public String getText() {
         return mVisitedTables.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// Runs that are not within tables are not recorded.
     /// 
     public int visitRun(Run run) {
         if (mVisitorIsInsideTable) indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Table is encountered in the document.
     /// 
     public int visitTableStart(final Table table) {
         int rows = 0;
         int columns = 0;

         if (table.getRows().getCount() > 0) {
             rows = table.getRows().getCount();
             columns = table.getFirstRow().getCount();
         }

         indentAndAppendLine("[Table start] Size: " + rows + "x" + columns);
         mDocTraversalDepth++;
         mVisitorIsInsideTable = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Table node have been visited.
     /// 
     public int visitTableEnd(final Table table) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Table end]");
         mVisitorIsInsideTable = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Row node is encountered in the document.
     /// 
     public int visitRowStart(final Row row) {
         String rowContents = row.getText().replaceAll("\\u0007", ", ").replaceAll(", , ", "");
         int rowWidth = row.indexOf(row.getLastCell()) + 1;
         int rowIndex = row.getParentTable().indexOf(row);
         String rowStatusInTable = row.isFirstRow() && row.isLastRow() ? "only" : row.isFirstRow() ? "first" : row.isLastRow() ? "last" : "";
         if (!"".equals(rowStatusInTable)) {
             rowStatusInTable = MessageFormat.format(", the {0} row in this table,", rowStatusInTable);
         }

         indentAndAppendLine(MessageFormat.format("[Row start] Row #{0}{1} width {2}, \"{3}\"", ++rowIndex, rowStatusInTable, rowWidth, rowContents));
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Row node have been visited.
     /// 
     public int visitRowEnd(final Row row) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Row end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Cell node is encountered in the document.
     /// 
     public int visitCellStart(final Cell cell) {
         Row row = cell.getParentRow();
         Table table = row.getParentTable();
         String cellStatusInRow = cell.isFirstCell() && cell.isLastCell() ? "only" : cell.isFirstCell() ? "first" : cell.isLastCell() ? "last" : "";
         if (!"".equals(cellStatusInRow)) {
             cellStatusInRow = MessageFormat.format(", the {0} cell in this row", cellStatusInRow);
         }

         indentAndAppendLine(MessageFormat.format("[Cell start] Row {0}, Col {1}{2}", table.indexOf(row) + 1, row.indexOf(cell) + 1, cellStatusInRow));
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Cell node have been visited.
     /// 
     public int visitCellEnd(final Cell cell) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Cell end]");
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is
     /// into the current table's tree of child nodes.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mVisitedTables.append("|  ");
         }

         mVisitedTables.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideTable;
     private int mDocTraversalDepth;
     private final  StringBuilder mVisitedTables;
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | Belge ziyaretçisi. |

**Returns:**
int - Ziyaretçi tarafından yapılacak eylem. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### appendChild(Node newChild) {#appendChild-com.aspose.words.Node}
```
public Node appendChild(Node newChild)
```


Belirtilen düğümü bu düğümün alt düğüm listesine sonuna ekler.

 **Remarks:** 

Eğer  newChild  zaten ağaçta ise, önce kaldırılır.

Eğer eklenen düğüm başka bir belgeden oluşturulmuşsa, düğümü geçerli belgeye aktarmak için **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** kullanmalısınız. Aktarılan düğüm daha sonra geçerli belgeye eklenebilir.

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | Eklenecek düğüm. |

**Returns:**
[Node](../../com.aspose.words/node/) - The node added.
### clearRowAttrs() {#clearRowAttrs}
```
public void clearRowAttrs()
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
### ensureMinimum() {#ensureMinimum}
```
public void ensureMinimum()
```


Eğer [Row](../../com.aspose.words/row/) içinde hücre yoksa, bir [Cell](../../com.aspose.words/cell/) oluşturur ve ekler.

 **Examples:** 

Bir satır düğümünün, ona içerik eklemeye başlamak için ihtiyaç duyduğumuz düğümleri içerdiğini nasıl sağlayacağımızı gösterir.

```

 Document doc = new Document();
 Table table = new Table(doc);
 doc.getFirstSection().getBody().appendChild(table);
 Row row = new Row(doc);
 table.appendChild(row);

 // Rows contain cells, containing paragraphs with typical elements such as runs, shapes, and even other tables.
 // Our new row has none of these nodes, and we cannot add contents to it until it does.
 Assert.assertEquals(0, row.getChildNodes(NodeType.ANY, true).getCount());

 // Calling the "EnsureMinimum" method on a table will ensure that
 // the table has at least one cell with an empty paragraph.
 row.ensureMinimum();
 row.getFirstCell().getFirstParagraph().appendChild(new Run(doc, "Hello world!"));
 
```

### fetchInheritedRowAttr(int key) {#fetchInheritedRowAttr-int}
```
public Object fetchInheritedRowAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchRowAttr(int key) {#fetchRowAttr-int}
```
public Object fetchRowAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

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
### getCells() {#getCells}
```
public CellCollection getCells()
```


Satırın [Cell](../../com.aspose.words/cell/) alt düğümlerine tipli erişim sağlar.

 **Examples:** 

Belgedeki tüm tabloları nasıl döngüyle gezileceğini ve her hücrenin içeriğinin nasıl yazdırılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Tables.docx");
 TableCollection tables = doc.getFirstSection().getBody().getTables();

 Assert.assertEquals(2, tables.toArray().length);

 for (int i = 0; i < tables.getCount(); i++) {
     System.out.println(MessageFormat.format("Start of Table {0}", i));

     RowCollection rows = tables.get(i).getRows();

     for (int j = 0; j < rows.getCount(); j++) {
         System.out.println(MessageFormat.format("\tStart of Row {0}", j));

         CellCollection cells = rows.get(j).getCells();

         for (int k = 0; k < cells.getCount(); k++) {
             String cellText = cells.get(k).toString(SaveFormat.TEXT).trim();
             System.out.println(MessageFormat.format("\t\tContents of Cell:{0} = \"{1}\"", k, cellText));
         }

         System.out.println(MessageFormat.format("\tEnd of Row {0}", j));
     }

     System.out.println(MessageFormat.format("End of Table {0}\n", i));
 }
 
```

**Returns:**
[CellCollection](../../com.aspose.words/cellcollection/) - The corresponding [CellCollection](../../com.aspose.words/cellcollection/) value.
### getChild(int nodeType, int index, boolean isDeep) {#getChild-int-int-boolean}
```
public Node getChild(int nodeType, int index, boolean isDeep)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| nodeType | int |  |
| indeks | int |  |
| isDeep | boolean |  |

**Returns:**
[Node](../../com.aspose.words/node/)
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
### getContainer() {#getContainer}
```
public CompositeNode getContainer()
```




**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/)
### getCount() {#getCount}
```
public int getCount()
```


Bu düğümün doğrudan alt öğelerinin sayısını alır.

 **Examples:** 

CompositeNode'un çocuk koleksiyonuna alt düğüm ekleme, güncelleme ve silme işlemlerinin nasıl yapılacağını gösterir.

```

 Document doc = new Document();

 // An empty document, by default, has one paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getParagraphs().getCount());

 // Composite nodes such as our paragraph can contain other composite and inline nodes as children.
 Paragraph paragraph = doc.getFirstSection().getBody().getFirstParagraph();
 Run paragraphText = new Run(doc, "Initial text. ");
 paragraph.appendChild(paragraphText);

 // Create three more run nodes.
 Run run1 = new Run(doc, "Run 1. ");
 Run run2 = new Run(doc, "Run 2. ");
 Run run3 = new Run(doc, "Run 3. ");

 // The document body will not display these runs until we insert them into a composite node
 // that itself is a part of the document's node tree, as we did with the first run.
 // We can determine where the text contents of nodes that we insert
 // appears in the document by specifying an insertion location relative to another node in the paragraph.
 Assert.assertEquals("Initial text.", paragraph.getText().trim());

 // Insert the second run into the paragraph in front of the initial run.
 paragraph.insertBefore(run2, paragraphText);

 Assert.assertEquals("Run 2. Initial text.", paragraph.getText().trim());

 // Insert the third run after the initial run.
 paragraph.insertAfter(run3, paragraphText);

 Assert.assertEquals("Run 2. Initial text. Run 3.", paragraph.getText().trim());

 // Insert the first run to the start of the paragraph's child nodes collection.
 paragraph.prependChild(run1);

 Assert.assertEquals("Run 1. Run 2. Initial text. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(4, paragraph.getChildNodes(NodeType.ANY, true).getCount());

 // We can modify the contents of the run by editing and deleting existing child nodes.
 ((Run) paragraph.getChildNodes(NodeType.RUN, true).get(1)).setText("Updated run 2. ");
 paragraph.getChildNodes(NodeType.RUN, true).remove(paragraphText);

 Assert.assertEquals("Run 1. Updated run 2. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, true).getCount());
 
```

**Returns:**
int - Bu düğümün doğrudan çocuk sayısı.
### getCurrentNode() {#getCurrentNode}
```
public Node getCurrentNode()
```




**Returns:**
[Node](../../com.aspose.words/node/)
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
### getDirectRowAttr(int key) {#getDirectRowAttr-int}
```
public Object getDirectRowAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

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
### getFirstCell() {#getFirstCell}
```
public Cell getFirstCell()
```


Satırdaki ilk [Cell](../../com.aspose.words/cell/) öğesini döndürür.

 **Examples:** 

Bir belgedeki her tablonun düğüm yapısını nasıl yazdıracağınızı gösterir.

```

 public void tableToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     TableStructurePrinter visitor = new TableStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered Table nodes and their children.
 /// 
 public static class TableStructurePrinter extends DocumentVisitor {
     public TableStructurePrinter() {
         mVisitedTables = new StringBuilder();
         mVisitorIsInsideTable = false;
     }

     public String getText() {
         return mVisitedTables.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// Runs that are not within tables are not recorded.
     /// 
     public int visitRun(Run run) {
         if (mVisitorIsInsideTable) indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Table is encountered in the document.
     /// 
     public int visitTableStart(final Table table) {
         int rows = 0;
         int columns = 0;

         if (table.getRows().getCount() > 0) {
             rows = table.getRows().getCount();
             columns = table.getFirstRow().getCount();
         }

         indentAndAppendLine("[Table start] Size: " + rows + "x" + columns);
         mDocTraversalDepth++;
         mVisitorIsInsideTable = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Table node have been visited.
     /// 
     public int visitTableEnd(final Table table) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Table end]");
         mVisitorIsInsideTable = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Row node is encountered in the document.
     /// 
     public int visitRowStart(final Row row) {
         String rowContents = row.getText().replaceAll("\\u0007", ", ").replaceAll(", , ", "");
         int rowWidth = row.indexOf(row.getLastCell()) + 1;
         int rowIndex = row.getParentTable().indexOf(row);
         String rowStatusInTable = row.isFirstRow() && row.isLastRow() ? "only" : row.isFirstRow() ? "first" : row.isLastRow() ? "last" : "";
         if (!"".equals(rowStatusInTable)) {
             rowStatusInTable = MessageFormat.format(", the {0} row in this table,", rowStatusInTable);
         }

         indentAndAppendLine(MessageFormat.format("[Row start] Row #{0}{1} width {2}, \"{3}\"", ++rowIndex, rowStatusInTable, rowWidth, rowContents));
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Row node have been visited.
     /// 
     public int visitRowEnd(final Row row) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Row end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Cell node is encountered in the document.
     /// 
     public int visitCellStart(final Cell cell) {
         Row row = cell.getParentRow();
         Table table = row.getParentTable();
         String cellStatusInRow = cell.isFirstCell() && cell.isLastCell() ? "only" : cell.isFirstCell() ? "first" : cell.isLastCell() ? "last" : "";
         if (!"".equals(cellStatusInRow)) {
             cellStatusInRow = MessageFormat.format(", the {0} cell in this row", cellStatusInRow);
         }

         indentAndAppendLine(MessageFormat.format("[Cell start] Row {0}, Col {1}{2}", table.indexOf(row) + 1, row.indexOf(cell) + 1, cellStatusInRow));
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Cell node have been visited.
     /// 
     public int visitCellEnd(final Cell cell) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Cell end]");
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is
     /// into the current table's tree of child nodes.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mVisitedTables.append("|  ");
         }

         mVisitedTables.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideTable;
     private int mDocTraversalDepth;
     private final  StringBuilder mVisitedTables;
 }
 
```

**Returns:**
[Cell](../../com.aspose.words/cell/) - The first [Cell](../../com.aspose.words/cell/) in the row.
### getFirstChild() {#getFirstChild}
```
public Node getFirstChild()
```


Düğümün ilk alt öğesini alır.

 **Remarks:** 

Eğer ilk çocuk düğüm yoksa, bir  null  döndürülür.

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
[Node](../../com.aspose.words/node/) - The first child of the node.
### getHidden() {#getHidden}
```
public boolean getHidden()
```


Bu satırın gizli olup olmadığını gösteren bir bayrağı alır.

 **Remarks:** 

Gizli satır, WordML ve ODT belgeleri için desteklenmez.

 **Examples:** 

Bir tablo satırının nasıl gizleneceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 Row row = doc.getFirstSection().getBody().getTables().get(0).getFirstRow();
 row.setHidden(true);

 doc.save(getArtifactsDir() + "Table.HiddenRow.docx");

 doc = new Document(getArtifactsDir() + "Table.HiddenRow.docx");

 row = doc.getFirstSection().getBody().getTables().get(0).getFirstRow();
 Assert.assertTrue(row.getHidden());

 for (Cell cell : row.getCells())
 {
     for (Paragraph para : cell.getParagraphs())
     {
         for (Run run : para.getRuns())
             Assert.assertTrue(run.getFont().getHidden());
     }
 }
 
```

**Returns:**
boolean - Bu satırın gizli olup olmadığını gösteren bir işaret.
### getLastCell() {#getLastCell}
```
public Cell getLastCell()
```


Satırdaki son [Cell](../../com.aspose.words/cell/) öğesini döndürür.

 **Examples:** 

Bir belgedeki her tablonun düğüm yapısını nasıl yazdıracağınızı gösterir.

```

 public void tableToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     TableStructurePrinter visitor = new TableStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered Table nodes and their children.
 /// 
 public static class TableStructurePrinter extends DocumentVisitor {
     public TableStructurePrinter() {
         mVisitedTables = new StringBuilder();
         mVisitorIsInsideTable = false;
     }

     public String getText() {
         return mVisitedTables.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// Runs that are not within tables are not recorded.
     /// 
     public int visitRun(Run run) {
         if (mVisitorIsInsideTable) indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Table is encountered in the document.
     /// 
     public int visitTableStart(final Table table) {
         int rows = 0;
         int columns = 0;

         if (table.getRows().getCount() > 0) {
             rows = table.getRows().getCount();
             columns = table.getFirstRow().getCount();
         }

         indentAndAppendLine("[Table start] Size: " + rows + "x" + columns);
         mDocTraversalDepth++;
         mVisitorIsInsideTable = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Table node have been visited.
     /// 
     public int visitTableEnd(final Table table) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Table end]");
         mVisitorIsInsideTable = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Row node is encountered in the document.
     /// 
     public int visitRowStart(final Row row) {
         String rowContents = row.getText().replaceAll("\\u0007", ", ").replaceAll(", , ", "");
         int rowWidth = row.indexOf(row.getLastCell()) + 1;
         int rowIndex = row.getParentTable().indexOf(row);
         String rowStatusInTable = row.isFirstRow() && row.isLastRow() ? "only" : row.isFirstRow() ? "first" : row.isLastRow() ? "last" : "";
         if (!"".equals(rowStatusInTable)) {
             rowStatusInTable = MessageFormat.format(", the {0} row in this table,", rowStatusInTable);
         }

         indentAndAppendLine(MessageFormat.format("[Row start] Row #{0}{1} width {2}, \"{3}\"", ++rowIndex, rowStatusInTable, rowWidth, rowContents));
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Row node have been visited.
     /// 
     public int visitRowEnd(final Row row) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Row end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Cell node is encountered in the document.
     /// 
     public int visitCellStart(final Cell cell) {
         Row row = cell.getParentRow();
         Table table = row.getParentTable();
         String cellStatusInRow = cell.isFirstCell() && cell.isLastCell() ? "only" : cell.isFirstCell() ? "first" : cell.isLastCell() ? "last" : "";
         if (!"".equals(cellStatusInRow)) {
             cellStatusInRow = MessageFormat.format(", the {0} cell in this row", cellStatusInRow);
         }

         indentAndAppendLine(MessageFormat.format("[Cell start] Row {0}, Col {1}{2}", table.indexOf(row) + 1, row.indexOf(cell) + 1, cellStatusInRow));
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Cell node have been visited.
     /// 
     public int visitCellEnd(final Cell cell) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Cell end]");
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is
     /// into the current table's tree of child nodes.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mVisitedTables.append("|  ");
         }

         mVisitedTables.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideTable;
     private int mDocTraversalDepth;
     private final  StringBuilder mVisitedTables;
 }
 
```

**Returns:**
[Cell](../../com.aspose.words/cell/) - The last [Cell](../../com.aspose.words/cell/) in the row.
### getLastChild() {#getLastChild}
```
public Node getLastChild()
```


Düğümün son alt öğesini alır.

 **Remarks:** 

Eğer son çocuk düğüm yoksa, bir  null  döndürülür.

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
[Node](../../com.aspose.words/node/) - The last child of the node.
### getNextMatchingNode(Node curNode) {#getNextMatchingNode-com.aspose.words.Node}
```
public Node getNextMatchingNode(Node curNode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node/) |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### getNextRow() {#getNextRow}
```
public Row getNextRow()
```


Sonraki [Row](../../com.aspose.words/row/) düğümünü alır.

 **Remarks:** 

Bu yöntem, tablo satırlarına tipli erişime ihtiyaç duyduğunuzda kullanılabilir. Eğer bir tabloda satır yerine bir [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) düğümü bulunursa, otomatik olarak içinde bulunan bir satır elde edilmek üzere gezilir.

 **Examples:** 

Tüm tablo hücrelerini nasıl döngüyle gezileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Tables.docx");
 Table table = doc.getFirstSection().getBody().getTables().get(0);

 // Enumerate through all cells of the table.
 for (Row row = table.getFirstRow(); row != null; row = row.getNextRow())
 {
     for (Cell cell = row.getFirstCell(); cell != null; cell = cell.getNextCell())
     {
         System.out.println(cell.getText());
     }
 }
 
```

**Returns:**
[Row](../../com.aspose.words/row/) - The next [Row](../../com.aspose.words/row/) node.
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


Döndürür [NodeType.ROW](../../com.aspose.words/nodetype/\#ROW).

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
int - [NodeType.ROW](../../com.aspose.words/nodetype/\#ROW). Döndürülen değer, [NodeType](../../com.aspose.words/nodetype/) sabitlerinden biridir.
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
### getParentTable() {#getParentTable}
```
public Table getParentTable()
```


Satırın doğrudan üst tabloyu döndürür.

 **Examples:** 

Bir belgedeki her tablonun düğüm yapısını nasıl yazdıracağınızı gösterir.

```

 public void tableToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     TableStructurePrinter visitor = new TableStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered Table nodes and their children.
 /// 
 public static class TableStructurePrinter extends DocumentVisitor {
     public TableStructurePrinter() {
         mVisitedTables = new StringBuilder();
         mVisitorIsInsideTable = false;
     }

     public String getText() {
         return mVisitedTables.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// Runs that are not within tables are not recorded.
     /// 
     public int visitRun(Run run) {
         if (mVisitorIsInsideTable) indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Table is encountered in the document.
     /// 
     public int visitTableStart(final Table table) {
         int rows = 0;
         int columns = 0;

         if (table.getRows().getCount() > 0) {
             rows = table.getRows().getCount();
             columns = table.getFirstRow().getCount();
         }

         indentAndAppendLine("[Table start] Size: " + rows + "x" + columns);
         mDocTraversalDepth++;
         mVisitorIsInsideTable = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Table node have been visited.
     /// 
     public int visitTableEnd(final Table table) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Table end]");
         mVisitorIsInsideTable = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Row node is encountered in the document.
     /// 
     public int visitRowStart(final Row row) {
         String rowContents = row.getText().replaceAll("\\u0007", ", ").replaceAll(", , ", "");
         int rowWidth = row.indexOf(row.getLastCell()) + 1;
         int rowIndex = row.getParentTable().indexOf(row);
         String rowStatusInTable = row.isFirstRow() && row.isLastRow() ? "only" : row.isFirstRow() ? "first" : row.isLastRow() ? "last" : "";
         if (!"".equals(rowStatusInTable)) {
             rowStatusInTable = MessageFormat.format(", the {0} row in this table,", rowStatusInTable);
         }

         indentAndAppendLine(MessageFormat.format("[Row start] Row #{0}{1} width {2}, \"{3}\"", ++rowIndex, rowStatusInTable, rowWidth, rowContents));
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Row node have been visited.
     /// 
     public int visitRowEnd(final Row row) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Row end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Cell node is encountered in the document.
     /// 
     public int visitCellStart(final Cell cell) {
         Row row = cell.getParentRow();
         Table table = row.getParentTable();
         String cellStatusInRow = cell.isFirstCell() && cell.isLastCell() ? "only" : cell.isFirstCell() ? "first" : cell.isLastCell() ? "last" : "";
         if (!"".equals(cellStatusInRow)) {
             cellStatusInRow = MessageFormat.format(", the {0} cell in this row", cellStatusInRow);
         }

         indentAndAppendLine(MessageFormat.format("[Cell start] Row {0}, Col {1}{2}", table.indexOf(row) + 1, row.indexOf(cell) + 1, cellStatusInRow));
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Cell node have been visited.
     /// 
     public int visitCellEnd(final Cell cell) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Cell end]");
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is
     /// into the current table's tree of child nodes.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mVisitedTables.append("|  ");
         }

         mVisitedTables.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideTable;
     private int mDocTraversalDepth;
     private final  StringBuilder mVisitedTables;
 }
 
```

**Returns:**
[Table](../../com.aspose.words/table/) - The immediate parent table of the row.
### getPreviousRow() {#getPreviousRow}
```
public Row getPreviousRow()
```


Önceki [Row](../../com.aspose.words/row/) düğümünü alır.

 **Remarks:** 

Bu yöntem, tablo satırlarına tipli erişime ihtiyaç duyduğunuzda kullanılabilir. Eğer bir tabloda satır yerine bir [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) düğümü bulunursa, otomatik olarak içinde bulunan bir satır elde edilmek üzere gezilir.

 **Examples:** 

Tüm tablo hücrelerini nasıl döngüyle gezileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Tables.docx");
 Table table = doc.getFirstSection().getBody().getTables().get(0);

 // Enumerate through all cells of the table.
 for (Row row = table.getFirstRow(); row != null; row = row.getNextRow())
 {
     for (Cell cell = row.getFirstCell(); cell != null; cell = cell.getNextCell())
     {
         System.out.println(cell.getText());
     }
 }
 
```

**Returns:**
[Row](../../com.aspose.words/row/) - The previous [Row](../../com.aspose.words/row/) node.
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
### getRowFormat() {#getRowFormat}
```
public RowFormat getRowFormat()
```


Satırın biçimlendirme özelliklerine erişim sağlar.

 **Examples:** 

Bir tablo içindeki satır ve hücrelerin biçimini değiştirmeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("City");
 builder.insertCell();
 builder.write("Country");
 builder.endRow();
 builder.insertCell();
 builder.write("London");
 builder.insertCell();
 builder.write("U.K.");
 builder.endTable();

 // Use the first row's "RowFormat" property to modify the formatting
 // of the contents of all cells in this row.
 RowFormat rowFormat = table.getFirstRow().getRowFormat();
 rowFormat.setHeight(25.0);
 rowFormat.getBorders().getByBorderType(BorderType.BOTTOM).setColor(Color.RED);

 // Use the "CellFormat" property of the first cell in the last row to modify the formatting of that cell's contents.
 CellFormat cellFormat = table.getLastRow().getFirstCell().getCellFormat();
 cellFormat.setWidth(100.0);
 cellFormat.getShading().setBackgroundPatternColor(Color.ORANGE);

 doc.save(getArtifactsDir() + "Table.RowCellFormat.docx");
 
```

Bir tablo satırının biçimlendirmesini değiştirmeyi gösterir.

```

 Document doc = new Document(getMyDir() + "Tables.docx");
 Table table = doc.getFirstSection().getBody().getTables().get(0);

 // Use the first row's "RowFormat" property to set formatting that modifies that entire row's appearance.
 Row firstRow = table.getFirstRow();
 firstRow.getRowFormat().getBorders().setLineStyle(LineStyle.NONE);
 firstRow.getRowFormat().setHeightRule(HeightRule.AUTO);
 firstRow.getRowFormat().setAllowBreakAcrossPages(true);

 doc.save(getArtifactsDir() + "Table.RowFormat.docx");
 
```

**Returns:**
[RowFormat](../../com.aspose.words/rowformat/) - The corresponding [RowFormat](../../com.aspose.words/rowformat/) value.
### getText() {#getText}
```
public String getText()
```


Bu satırdaki tüm hücrelerin metnini, satır sonu karakteri dahil olmak üzere alır.

 **Remarks:** 

Tüm çocuk düğümlerin birleştirilmiş metnini, satır sonu karakteri [ControlChar.CELL](../../com.aspose.words/controlchar/\#CELL) sonuna eklenmiş olarak döndürür.

Döndürülen dize, [ControlChar](../../com.aspose.words/controlchar/) içinde açıklandığı gibi tüm kontrol ve özel karakterleri içerir.

 **Examples:** 

Bir belgedeki her tablonun düğüm yapısını nasıl yazdıracağınızı gösterir.

```

 public void tableToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     TableStructurePrinter visitor = new TableStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered Table nodes and their children.
 /// 
 public static class TableStructurePrinter extends DocumentVisitor {
     public TableStructurePrinter() {
         mVisitedTables = new StringBuilder();
         mVisitorIsInsideTable = false;
     }

     public String getText() {
         return mVisitedTables.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// Runs that are not within tables are not recorded.
     /// 
     public int visitRun(Run run) {
         if (mVisitorIsInsideTable) indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Table is encountered in the document.
     /// 
     public int visitTableStart(final Table table) {
         int rows = 0;
         int columns = 0;

         if (table.getRows().getCount() > 0) {
             rows = table.getRows().getCount();
             columns = table.getFirstRow().getCount();
         }

         indentAndAppendLine("[Table start] Size: " + rows + "x" + columns);
         mDocTraversalDepth++;
         mVisitorIsInsideTable = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Table node have been visited.
     /// 
     public int visitTableEnd(final Table table) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Table end]");
         mVisitorIsInsideTable = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Row node is encountered in the document.
     /// 
     public int visitRowStart(final Row row) {
         String rowContents = row.getText().replaceAll("\\u0007", ", ").replaceAll(", , ", "");
         int rowWidth = row.indexOf(row.getLastCell()) + 1;
         int rowIndex = row.getParentTable().indexOf(row);
         String rowStatusInTable = row.isFirstRow() && row.isLastRow() ? "only" : row.isFirstRow() ? "first" : row.isLastRow() ? "last" : "";
         if (!"".equals(rowStatusInTable)) {
             rowStatusInTable = MessageFormat.format(", the {0} row in this table,", rowStatusInTable);
         }

         indentAndAppendLine(MessageFormat.format("[Row start] Row #{0}{1} width {2}, \"{3}\"", ++rowIndex, rowStatusInTable, rowWidth, rowContents));
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Row node have been visited.
     /// 
     public int visitRowEnd(final Row row) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Row end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Cell node is encountered in the document.
     /// 
     public int visitCellStart(final Cell cell) {
         Row row = cell.getParentRow();
         Table table = row.getParentTable();
         String cellStatusInRow = cell.isFirstCell() && cell.isLastCell() ? "only" : cell.isFirstCell() ? "first" : cell.isLastCell() ? "last" : "";
         if (!"".equals(cellStatusInRow)) {
             cellStatusInRow = MessageFormat.format(", the {0} cell in this row", cellStatusInRow);
         }

         indentAndAppendLine(MessageFormat.format("[Cell start] Row {0}, Col {1}{2}", table.indexOf(row) + 1, row.indexOf(cell) + 1, cellStatusInRow));
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Cell node have been visited.
     /// 
     public int visitCellEnd(final Cell cell) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Cell end]");
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is
     /// into the current table's tree of child nodes.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mVisitedTables.append("|  ");
         }

         mVisitedTables.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideTable;
     private int mDocTraversalDepth;
     private final  StringBuilder mVisitedTables;
 }
 
```

**Returns:**
java.lang.String
### hasChildNodes() {#hasChildNodes}
```
public boolean hasChildNodes()
```


Bu düğümün herhangi bir alt düğümü varsa  true  döndürür.

 **Examples:** 

İki tablodan satırların nasıl birleştirilerek tek bir tablo haline getirileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 // Below are two ways of getting a table from a document.
 // 1 -  From the "Tables" collection of a Body node:
 Table firstTable = doc.getFirstSection().getBody().getTables().get(0);

 // 2 -  Using the "GetChild" method:
 Table secondTable = (Table) doc.getChild(NodeType.TABLE, 1, true);

 // Append all rows from the current table to the next.
 while (secondTable.hasChildNodes())
     firstTable.getRows().add(secondTable.getFirstRow());

 // Remove the empty table container.
 secondTable.remove();

 doc.save(getArtifactsDir() + "Table.CombineTables.docx");
 
```

**Returns:**
boolean -  true  bu düğümün herhangi bir çocuk düğümü varsa.
### indexOf(Node child) {#indexOf-com.aspose.words.Node}
```
public int indexOf(Node child)
```


Belirtilen alt düğümün alt düğüm dizisindeki dizinini döndürür.

 **Remarks:** 

Düğüm çocuk düğümler içinde bulunamazsa -1 döndürür.

 **Examples:** 

Verilen bir çocuk düğümün ebeveyninden indeksinin nasıl alınacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 Body body = doc.getFirstSection().getBody();

 // Retrieve the index of the last paragraph in the body of the first section.
 Assert.assertEquals(24, body.getChildNodes(NodeType.ANY, false).indexOf(body.getLastParagraph()));
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| child | [Node](../../com.aspose.words/node/) |  |

**Returns:**
int
### insertAfter(Node newChild, Node refChild) {#insertAfter-com.aspose.words.Node-com.aspose.words.Node}
```
public Node insertAfter(Node newChild, Node refChild)
```


Belirtilen düğümü, belirtilen referans düğümünden hemen sonra ekler.

 **Remarks:** 

Eğer  refChild  null ise,  newChild  çocuk düğüm listesinin başına eklenir.

Eğer  newChild  zaten ağaçta ise, önce kaldırılır.

Eğer eklenen düğüm başka bir belgeden oluşturulmuşsa, düğümü geçerli belgeye aktarmak için **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** kullanmalısınız. Aktarılan düğüm daha sonra geçerli belgeye eklenebilir.

 **Examples:** 

CompositeNode'un çocuk koleksiyonuna alt düğüm ekleme, güncelleme ve silme işlemlerinin nasıl yapılacağını gösterir.

```

 Document doc = new Document();

 // An empty document, by default, has one paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getParagraphs().getCount());

 // Composite nodes such as our paragraph can contain other composite and inline nodes as children.
 Paragraph paragraph = doc.getFirstSection().getBody().getFirstParagraph();
 Run paragraphText = new Run(doc, "Initial text. ");
 paragraph.appendChild(paragraphText);

 // Create three more run nodes.
 Run run1 = new Run(doc, "Run 1. ");
 Run run2 = new Run(doc, "Run 2. ");
 Run run3 = new Run(doc, "Run 3. ");

 // The document body will not display these runs until we insert them into a composite node
 // that itself is a part of the document's node tree, as we did with the first run.
 // We can determine where the text contents of nodes that we insert
 // appears in the document by specifying an insertion location relative to another node in the paragraph.
 Assert.assertEquals("Initial text.", paragraph.getText().trim());

 // Insert the second run into the paragraph in front of the initial run.
 paragraph.insertBefore(run2, paragraphText);

 Assert.assertEquals("Run 2. Initial text.", paragraph.getText().trim());

 // Insert the third run after the initial run.
 paragraph.insertAfter(run3, paragraphText);

 Assert.assertEquals("Run 2. Initial text. Run 3.", paragraph.getText().trim());

 // Insert the first run to the start of the paragraph's child nodes collection.
 paragraph.prependChild(run1);

 Assert.assertEquals("Run 1. Run 2. Initial text. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(4, paragraph.getChildNodes(NodeType.ANY, true).getCount());

 // We can modify the contents of the run by editing and deleting existing child nodes.
 ((Run) paragraph.getChildNodes(NodeType.RUN, true).get(1)).setText("Updated run 2. ");
 paragraph.getChildNodes(NodeType.RUN, true).remove(paragraphText);

 Assert.assertEquals("Run 1. Updated run 2. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, true).getCount());
 
```

Tüm metin kutusu şekillerinin nasıl görüntü şekilleriyle değiştirileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Textboxes in drawing canvas.docx");

 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(3, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.TEXT_BOX));
 Assert.assertEquals(1, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.IMAGE));

 for (Shape shape : shapeList) {
     if (((shape.getShapeType()) == (ShapeType.TEXT_BOX))) {
         Shape replacementShape = new Shape(doc, ShapeType.IMAGE);
         replacementShape.getImageData().setImage(getImageDir() + "Logo.jpg");
         replacementShape.setLeft(shape.getLeft());
         replacementShape.setTop(shape.getTop());
         replacementShape.setWidth(shape.getWidth());
         replacementShape.setHeight(shape.getHeight());
         replacementShape.setRelativeHorizontalPosition(shape.getRelativeHorizontalPosition());
         replacementShape.setRelativeVerticalPosition(shape.getRelativeVerticalPosition());
         replacementShape.setHorizontalAlignment(shape.getHorizontalAlignment());
         replacementShape.setVerticalAlignment(shape.getVerticalAlignment());
         replacementShape.setWrapType(shape.getWrapType());
         replacementShape.setWrapSide(shape.getWrapSide());

         shape.getParentNode().insertAfter(replacementShape, shape);
         shape.remove();
     }
 }

 shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(0, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.TEXT_BOX));
 Assert.assertEquals(4, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.IMAGE));

 doc.save(getArtifactsDir() + "Shape.ReplaceTextboxesWithImages.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | Eklenecek [Node](../../com.aspose.words/node/). |
| refChild | [Node](../../com.aspose.words/node/) | Referans düğüm olan [Node](../../com.aspose.words/node/).  newChild  ,  refChild  sonrasına yerleştirilir. |

**Returns:**
[Node](../../com.aspose.words/node/) - The inserted node.
### insertBefore(Node newChild, Node refChild) {#insertBefore-com.aspose.words.Node-com.aspose.words.Node}
```
public Node insertBefore(Node newChild, Node refChild)
```


Belirtilen düğümü, belirtilen referans düğümünden hemen önce ekler.

 **Remarks:** 

Eğer  refChild  null ise,  newChild  çocuk düğüm listesinin sonuna eklenir.

Eğer  newChild  zaten ağaçta ise, önce kaldırılır.

Eğer eklenen düğüm başka bir belgeden oluşturulmuşsa, düğümü geçerli belgeye aktarmak için **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** kullanmalısınız. Aktarılan düğüm daha sonra geçerli belgeye eklenebilir.

 **Examples:** 

CompositeNode'un çocuk koleksiyonuna alt düğüm ekleme, güncelleme ve silme işlemlerinin nasıl yapılacağını gösterir.

```

 Document doc = new Document();

 // An empty document, by default, has one paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getParagraphs().getCount());

 // Composite nodes such as our paragraph can contain other composite and inline nodes as children.
 Paragraph paragraph = doc.getFirstSection().getBody().getFirstParagraph();
 Run paragraphText = new Run(doc, "Initial text. ");
 paragraph.appendChild(paragraphText);

 // Create three more run nodes.
 Run run1 = new Run(doc, "Run 1. ");
 Run run2 = new Run(doc, "Run 2. ");
 Run run3 = new Run(doc, "Run 3. ");

 // The document body will not display these runs until we insert them into a composite node
 // that itself is a part of the document's node tree, as we did with the first run.
 // We can determine where the text contents of nodes that we insert
 // appears in the document by specifying an insertion location relative to another node in the paragraph.
 Assert.assertEquals("Initial text.", paragraph.getText().trim());

 // Insert the second run into the paragraph in front of the initial run.
 paragraph.insertBefore(run2, paragraphText);

 Assert.assertEquals("Run 2. Initial text.", paragraph.getText().trim());

 // Insert the third run after the initial run.
 paragraph.insertAfter(run3, paragraphText);

 Assert.assertEquals("Run 2. Initial text. Run 3.", paragraph.getText().trim());

 // Insert the first run to the start of the paragraph's child nodes collection.
 paragraph.prependChild(run1);

 Assert.assertEquals("Run 1. Run 2. Initial text. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(4, paragraph.getChildNodes(NodeType.ANY, true).getCount());

 // We can modify the contents of the run by editing and deleting existing child nodes.
 ((Run) paragraph.getChildNodes(NodeType.RUN, true).get(1)).setText("Updated run 2. ");
 paragraph.getChildNodes(NodeType.RUN, true).remove(paragraphText);

 Assert.assertEquals("Run 1. Updated run 2. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, true).getCount());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | Eklenecek [Node](../../com.aspose.words/node/). |
| refChild | [Node](../../com.aspose.words/node/) | Referans düğüm olan [Node](../../com.aspose.words/node/).  newChild  bu düğümün önüne yerleştirilir. |

**Returns:**
[Node](../../com.aspose.words/node/) - The inserted node.
### isComposite() {#isComposite}
```
public boolean isComposite()
```


Bu düğümün alt düğüm alabileceği için  true  döndürür.

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
boolean -  true  çünkü bu düğümün alt düğümleri olabilir.
### isFirstRow() {#isFirstRow}
```
public boolean isFirstRow()
```


Bir tabloda bu ilk satırsa true; aksi takdirde false.

 **Examples:** 

Bir belgedeki her tablonun düğüm yapısını nasıl yazdıracağınızı gösterir.

```

 public void tableToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     TableStructurePrinter visitor = new TableStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered Table nodes and their children.
 /// 
 public static class TableStructurePrinter extends DocumentVisitor {
     public TableStructurePrinter() {
         mVisitedTables = new StringBuilder();
         mVisitorIsInsideTable = false;
     }

     public String getText() {
         return mVisitedTables.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// Runs that are not within tables are not recorded.
     /// 
     public int visitRun(Run run) {
         if (mVisitorIsInsideTable) indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Table is encountered in the document.
     /// 
     public int visitTableStart(final Table table) {
         int rows = 0;
         int columns = 0;

         if (table.getRows().getCount() > 0) {
             rows = table.getRows().getCount();
             columns = table.getFirstRow().getCount();
         }

         indentAndAppendLine("[Table start] Size: " + rows + "x" + columns);
         mDocTraversalDepth++;
         mVisitorIsInsideTable = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Table node have been visited.
     /// 
     public int visitTableEnd(final Table table) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Table end]");
         mVisitorIsInsideTable = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Row node is encountered in the document.
     /// 
     public int visitRowStart(final Row row) {
         String rowContents = row.getText().replaceAll("\\u0007", ", ").replaceAll(", , ", "");
         int rowWidth = row.indexOf(row.getLastCell()) + 1;
         int rowIndex = row.getParentTable().indexOf(row);
         String rowStatusInTable = row.isFirstRow() && row.isLastRow() ? "only" : row.isFirstRow() ? "first" : row.isLastRow() ? "last" : "";
         if (!"".equals(rowStatusInTable)) {
             rowStatusInTable = MessageFormat.format(", the {0} row in this table,", rowStatusInTable);
         }

         indentAndAppendLine(MessageFormat.format("[Row start] Row #{0}{1} width {2}, \"{3}\"", ++rowIndex, rowStatusInTable, rowWidth, rowContents));
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Row node have been visited.
     /// 
     public int visitRowEnd(final Row row) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Row end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Cell node is encountered in the document.
     /// 
     public int visitCellStart(final Cell cell) {
         Row row = cell.getParentRow();
         Table table = row.getParentTable();
         String cellStatusInRow = cell.isFirstCell() && cell.isLastCell() ? "only" : cell.isFirstCell() ? "first" : cell.isLastCell() ? "last" : "";
         if (!"".equals(cellStatusInRow)) {
             cellStatusInRow = MessageFormat.format(", the {0} cell in this row", cellStatusInRow);
         }

         indentAndAppendLine(MessageFormat.format("[Cell start] Row {0}, Col {1}{2}", table.indexOf(row) + 1, row.indexOf(cell) + 1, cellStatusInRow));
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Cell node have been visited.
     /// 
     public int visitCellEnd(final Cell cell) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Cell end]");
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is
     /// into the current table's tree of child nodes.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mVisitedTables.append("|  ");
         }

         mVisitedTables.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideTable;
     private int mDocTraversalDepth;
     private final  StringBuilder mVisitedTables;
 }
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### isLastRow() {#isLastRow}
```
public boolean isLastRow()
```


Bir tabloda bu son satırsa true; aksi takdirde false.

 **Examples:** 

Bir tablonun aynı sayfada birlikte kalmasını nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Table spanning two pages.docx");
 Table table = doc.getFirstSection().getBody().getTables().get(0);

 // Enabling KeepWithNext for every paragraph in the table except for the
 // last ones in the last row will prevent the table from splitting across multiple pages.
 for (Cell cell : (Iterable) table.getChildNodes(NodeType.CELL, true))
     for (Paragraph para : cell.getParagraphs()) {
         Assert.assertTrue(para.isInCell());

         if (!(cell.getParentRow().isLastRow() && para.isEndOfCell()))
             para.getParagraphFormat().setKeepWithNext(true);
     }

 doc.save(getArtifactsDir() + "Table.KeepTableTogether.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### iterator() {#iterator}
```
public Iterator iterator()
```


Bu düğümün alt düğümleri üzerinde foreach tarzı yineleme desteği sağlar.

 **Examples:** 

Bir belgenin tüm yorumlarını ve yanıtlarını nasıl yazdıracağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Comments.docx");

 NodeCollection comments = doc.getChildNodes(NodeType.COMMENT, true);
 // If a comment has no ancestor, it is a "top-level" comment as opposed to a reply-type comment.
 // Print all top-level comments along with any replies they may have.
 for (Comment comment : (Iterable) comments) {
     if (comment.getAncestor() == null) {
         System.out.println("Top-level comment:");
         System.out.println("\t\"{comment.GetText().Trim()}\", by {comment.Author}");
         System.out.println("Has {comment.Replies.Count} replies");
         for (Comment commentReply : comment.getReplies()) {
             System.out.println("\t\"{commentReply.GetText().Trim()}\", by {commentReply.Author}");
         }
         System.out.println();
     }
 }
 
```

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
### prependChild(Node newChild) {#prependChild-com.aspose.words.Node}
```
public Node prependChild(Node newChild)
```


Belirtilen düğümü, bu düğümün alt düğüm listesinin başına ekler.

 **Remarks:** 

Eğer  newChild  zaten ağaçta ise, önce kaldırılır.

Eğer eklenen düğüm başka bir belgeden oluşturulmuşsa, düğümü geçerli belgeye aktarmak için **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** kullanmalısınız. Aktarılan düğüm daha sonra geçerli belgeye eklenebilir.

 **Examples:** 

CompositeNode'un çocuk koleksiyonuna alt düğüm ekleme, güncelleme ve silme işlemlerinin nasıl yapılacağını gösterir.

```

 Document doc = new Document();

 // An empty document, by default, has one paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getParagraphs().getCount());

 // Composite nodes such as our paragraph can contain other composite and inline nodes as children.
 Paragraph paragraph = doc.getFirstSection().getBody().getFirstParagraph();
 Run paragraphText = new Run(doc, "Initial text. ");
 paragraph.appendChild(paragraphText);

 // Create three more run nodes.
 Run run1 = new Run(doc, "Run 1. ");
 Run run2 = new Run(doc, "Run 2. ");
 Run run3 = new Run(doc, "Run 3. ");

 // The document body will not display these runs until we insert them into a composite node
 // that itself is a part of the document's node tree, as we did with the first run.
 // We can determine where the text contents of nodes that we insert
 // appears in the document by specifying an insertion location relative to another node in the paragraph.
 Assert.assertEquals("Initial text.", paragraph.getText().trim());

 // Insert the second run into the paragraph in front of the initial run.
 paragraph.insertBefore(run2, paragraphText);

 Assert.assertEquals("Run 2. Initial text.", paragraph.getText().trim());

 // Insert the third run after the initial run.
 paragraph.insertAfter(run3, paragraphText);

 Assert.assertEquals("Run 2. Initial text. Run 3.", paragraph.getText().trim());

 // Insert the first run to the start of the paragraph's child nodes collection.
 paragraph.prependChild(run1);

 Assert.assertEquals("Run 1. Run 2. Initial text. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(4, paragraph.getChildNodes(NodeType.ANY, true).getCount());

 // We can modify the contents of the run by editing and deleting existing child nodes.
 ((Run) paragraph.getChildNodes(NodeType.RUN, true).get(1)).setText("Updated run 2. ");
 paragraph.getChildNodes(NodeType.RUN, true).remove(paragraphText);

 Assert.assertEquals("Run 1. Updated run 2. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, true).getCount());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | Eklenecek düğüm. |

**Returns:**
[Node](../../com.aspose.words/node/) - The node added.
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


Geçerli düğümün tüm alt düğümlerini kaldırır.

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

### removeChild(Node oldChild) {#removeChild-com.aspose.words.Node}
```
public Node removeChild(Node oldChild)
```


Belirtilen alt düğümü kaldırır.

 **Remarks:** 

Düğüm kaldırıldıktan sonra  oldChild  öğesinin üst öğesi  null  olarak ayarlanır.

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| oldChild | [Node](../../com.aspose.words/node/) | Kaldırılacak düğüm. |

**Returns:**
[Node](../../com.aspose.words/node/) - The removed node.
### removeMoveRevisions() {#removeMoveRevisions}
```
public void removeMoveRevisions()
```




### removeSmartTags() {#removeSmartTags}
```
public void removeSmartTags()
```


Geçerli düğümün tüm [SmartTag](../../com.aspose.words/smarttag/) alt düğümlerini kaldırır.

 **Remarks:** 

Bu yöntem akıllı etiketlerin içeriğini kaldırmaz.

 **Examples:** 

Bir birleşik düğümün alt düğümlerinden tüm akıllı etiketleri kaldırır.

```

 Document doc = new Document(getMyDir() + "Smart tags.doc");

 Assert.assertEquals(8, doc.getChildNodes(NodeType.SMART_TAG, true).getCount());

 doc.removeSmartTags();

 Assert.assertEquals(0, doc.getChildNodes(NodeType.SMART_TAG, true).getCount());
 
```

Akıllı etiketlerin nasıl oluşturulacağını gösterir.

```

 public void create() throws Exception {
     Document doc = new Document();

     // A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
     // such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
     SmartTag smartTag = new SmartTag(doc);

     // Smart tags are composite nodes that contain their recognized text in its entirety.
     // Add contents to this smart tag manually.
     smartTag.appendChild(new Run(doc, "May 29, 2019"));

     // Microsoft Word may recognize the above contents as being a date.
     // Smart tags use the "Element" property to reflect the type of data they contain.
     smartTag.setElement("date");

     // Some smart tag types process their contents further into custom XML properties.
     smartTag.getProperties().add(new CustomXmlProperty("Day", "", "29"));
     smartTag.getProperties().add(new CustomXmlProperty("Month", "", "5"));
     smartTag.getProperties().add(new CustomXmlProperty("Year", "", "2019"));

     // Set the smart tag's URI to the default value.
     smartTag.setUri("urn:schemas-microsoft-com:office:smarttags");

     doc.getFirstSection().getBody().getFirstParagraph().appendChild(smartTag);
     doc.getFirstSection().getBody().getFirstParagraph().appendChild(new Run(doc, " is a date. "));

     // Create another smart tag for a stock ticker.
     smartTag = new SmartTag(doc);
     smartTag.setElement("stockticker");
     smartTag.setUri("urn:schemas-microsoft-com:office:smarttags");

     smartTag.appendChild(new Run(doc, "MSFT"));

     doc.getFirstSection().getBody().getFirstParagraph().appendChild(smartTag);
     doc.getFirstSection().getBody().getFirstParagraph().appendChild(new Run(doc, " is a stock ticker."));

     // Print all the smart tags in our document using a document visitor.
     doc.accept(new SmartTagPrinter());

     // Older versions of Microsoft Word support smart tags.
     doc.save(getArtifactsDir() + "SmartTag.Create.doc");

     // Use the "RemoveSmartTags" method to remove all smart tags from a document.
     Assert.assertEquals(2, doc.getChildNodes(NodeType.SMART_TAG, true).getCount());

     doc.removeSmartTags();

     Assert.assertEquals(0, doc.getChildNodes(NodeType.SMART_TAG, true).getCount());
 }

 /// 
 /// Prints visited smart tags and their contents.
 /// 
 private static class SmartTagPrinter extends DocumentVisitor {
     /// 
     /// Called when a SmartTag node is encountered in the document.
     /// 
     public int visitSmartTagStart(SmartTag smartTag) {
         System.out.println("Smart tag type: {smartTag.Element}");
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when the visiting of a SmartTag node is ended.
     /// 
     public int visitSmartTagEnd(SmartTag smartTag) {
         System.out.println("\tContents: \"{smartTag.ToString(SaveFormat.Text)}\"");

         if (smartTag.getProperties().getCount() == 0) {
             System.out.println("\tContains no properties");
         } else {
             System.out.println("\tProperties: ");
             String[] properties = new String[smartTag.getProperties().getCount()];
             int index = 0;

             for (CustomXmlProperty cxp : smartTag.getProperties())
                 properties[index++] = MessageFormat.format("\"{0}\" = \"{1}\"", cxp.getName(), cxp.getValue());

             System.out.println(StringUtils.join(properties, ", "));
         }

         return VisitorAction.CONTINUE;
     }
 }
 
```

### resetToDefaultAttrs() {#resetToDefaultAttrs}
```
public void resetToDefaultAttrs()
```




### selectNodes(String xpath) {#selectNodes-java.lang.String}
```
public NodeList selectNodes(String xpath)
```


XPath ifadesiyle eşleşen düğüm listesini seçer.

 **Remarks:** 

Şu anda yalnızca öğe adları içeren ifadeler desteklenir. Öznitelik adları kullanan ifadeler desteklenmez.

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

Bir düğümün bir alan içinde olup olmadığını test etmek için XPath ifadesinin nasıl kullanılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Mail merge destination - Northwind employees.docx");

 // The NodeList that results from this XPath expression will contain all nodes we find inside a field.
 // However, FieldStart and FieldEnd nodes can be on the list if there are nested fields in the path.
 // Currently does not find rare fields in which the FieldCode or FieldResult spans across multiple paragraphs.
 NodeList resultList =
         doc.selectNodes("//FieldStart/following-sibling::node()[following-sibling::FieldEnd]");
 Run[] runs = Arrays.stream(resultList.toArray()).filter(n -> n.getNodeType() == NodeType.RUN).toArray(Run[]::new);
 Run run = runs[0];

 // Check if the specified run is one of the nodes that are inside the field.
 System.out.println(MessageFormat.format("Contents of the first Run node that''s part of a field: {0}", run.getText().trim()));
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| xpath | java.lang.String | XPath ifadesi. |

**Returns:**
[NodeList](../../com.aspose.words/nodelist/) - A list of nodes matching the XPath query.
### selectSingleNode(String xpath) {#selectSingleNode-java.lang.String}
```
public Node selectSingleNode(String xpath)
```


XPath ifadesiyle eşleşen ilk [Node](../../com.aspose.words/node/) öğesini seçer.

 **Remarks:** 

Şu anda yalnızca öğe adları içeren ifadeler desteklenir. Öznitelik adları kullanan ifadeler desteklenmez.

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| xpath | java.lang.String | XPath ifadesi. |

**Returns:**
[Node](../../com.aspose.words/node/) - The first [Node](../../com.aspose.words/node/) that matches the XPath query or  null  if no matching node is found.
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

### setHidden(boolean value) {#setHidden-boolean}
```
public void setHidden(boolean value)
```


Bu satırın gizli olup olmadığını belirten bir bayrak ayarlar.

 **Remarks:** 

Gizli satır, WordML ve ODT belgeleri için desteklenmez.

 **Examples:** 

Bir tablo satırının nasıl gizleneceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 Row row = doc.getFirstSection().getBody().getTables().get(0).getFirstRow();
 row.setHidden(true);

 doc.save(getArtifactsDir() + "Table.HiddenRow.docx");

 doc = new Document(getArtifactsDir() + "Table.HiddenRow.docx");

 row = doc.getFirstSection().getBody().getTables().get(0).getFirstRow();
 Assert.assertTrue(row.getHidden());

 for (Cell cell : row.getCells())
 {
     for (Paragraph para : cell.getParagraphs())
     {
         for (Run run : para.getRuns())
             Assert.assertTrue(run.getFont().getHidden());
     }
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Bu satırın gizli olup olmadığını gösteren bir işaret. |

### setRowAttr(int key, Object value) {#setRowAttr-int-java.lang.Object}
```
public void setRowAttr(int key, Object value)
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
