---
title: "Zeile"
linktitle: "Zeile"
second_title: "Aspose.Words für Java"
description: "Stellt eine Tabellenzeile in Java dar."
type: docs
weight: 588
url: /de/java/com.aspose.words/row/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node/), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode/)
```
public class Row extends CompositeNode
```

Stellt eine Tabellenzeile dar.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Working with Tables ][Working with Tables].

 **Remarks:** 

[Row](../../com.aspose.words/row/) can only be a child of a [Table](../../com.aspose.words/table/).

[Row](../../com.aspose.words/row/) can contain one or more [Cell](../../com.aspose.words/cell/) nodes.

Eine minimal gültige Zeile muss mindestens eine [Cell](../../com.aspose.words/cell/) enthalten.

 **Examples:** 

Zeigt, wie man eine Tabelle erstellt.

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

Zeigt, wie man durch alle Tabellen im Dokument iteriert und den Inhalt jeder Zelle ausgibt.

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

Zeigt, wie man eine verschachtelte Tabelle erstellt, ohne einen Document Builder zu verwenden.

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
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [Row(DocumentBase doc)](#Row-com.aspose.words.DocumentBase) | Initialisiert eine neue Instanz der Klasse [Row](../../com.aspose.words/row/). |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor) | Akzeptiert einen Besucher. |
| [acceptEnd(DocumentVisitor visitor)](#acceptEnd-com.aspose.words.DocumentVisitor) | Akzeptiert einen Besucher, um das Ende der Zeile zu besuchen. |
| [acceptStart(DocumentVisitor visitor)](#acceptStart-com.aspose.words.DocumentVisitor) | Akzeptiert einen Besucher, um den Anfang der Zeile zu besuchen. |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node) | Fügt den angegebenen Knoten am Ende der Liste von Kindknoten dieses Knotens hinzu. |
| [clearRowAttrs()](#clearRowAttrs) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean) | Erstellt ein Duplikat des Knotens. |
| [ensureMinimum()](#ensureMinimum) | Wenn die [Row](../../com.aspose.words/row/) keine Zellen hat, wird eine [Cell](../../com.aspose.words/cell/) erstellt und angehängt. |
| [fetchInheritedRowAttr(int key)](#fetchInheritedRowAttr-int) |  |
| [fetchRowAttr(int key)](#fetchRowAttr-int) |  |
| [getAncestor(int ancestorType)](#getAncestor-int) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class) | Ermittelt den ersten Vorfahren des angegebenen Objekttyps. |
| [getCells()](#getCells) | Bietet typisierten Zugriff auf die [Cell](../../com.aspose.words/cell/) Kindknoten der Zeile. |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean) |  |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean) |  |
| [getContainer()](#getContainer) |  |
| [getCount()](#getCount) | Ermittelt die Anzahl der unmittelbaren Kindknoten dieses Knotens. |
| [getCurrentNode()](#getCurrentNode) |  |
| [getCustomNodeId()](#getCustomNodeId) | Gibt eine benutzerdefinierte Knotenkennung an. |
| [getDirectRowAttr(int key)](#getDirectRowAttr-int) |  |
| [getDocument()](#getDocument) | Ermittelt das Dokument, zu dem dieser Knoten gehört. |
| [getFirstCell()](#getFirstCell) | Gibt die erste [Cell](../../com.aspose.words/cell/) in der Zeile zurück. |
| [getFirstChild()](#getFirstChild) | Ermittelt das erste Kind des Knotens. |
| [getHidden()](#getHidden) | Ermittelt ein Flag, das angibt, ob diese Zeile ausgeblendet ist oder nicht. |
| [getLastCell()](#getLastCell) | Gibt die letzte [Cell](../../com.aspose.words/cell/) in der Zeile zurück. |
| [getLastChild()](#getLastChild) | Ermittelt das letzte Kind des Knotens. |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node) |  |
| [getNextRow()](#getNextRow) | Ermittelt den nächsten [Row](../../com.aspose.words/row/) Knoten. |
| [getNextSibling()](#getNextSibling) | Ermittelt den Knoten, der unmittelbar auf diesen Knoten folgt. |
| [getNodeType()](#getNodeType) | Gibt [NodeType.ROW](../../com.aspose.words/nodetype/\#ROW) zurück. |
| [getParentNode()](#getParentNode) | Ermittelt den unmittelbaren übergeordneten Knoten dieses Knotens. |
| [getParentTable()](#getParentTable) | Gibt die unmittelbare übergeordnete Tabelle der Zeile zurück. |
| [getPreviousRow()](#getPreviousRow) | Liefert den vorherigen [Row](../../com.aspose.words/row/) Knoten. |
| [getPreviousSibling()](#getPreviousSibling) | Ermittelt den Knoten, der unmittelbar vor diesem Knoten liegt. |
| [getRange()](#getRange) | Gibt ein [Range](../../com.aspose.words/range/)-Objekt zurück, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [getRowFormat()](#getRowFormat) | Stellt Zugriff auf die Formatierungseigenschaften der Zeile bereit. |
| [getText()](#getText) | Liefert den Text aller Zellen in dieser Zeile einschließlich des Zeilenendezeichens. |
| [hasChildNodes()](#hasChildNodes) | Gibt  true  zurück, wenn dieser Knoten Kindknoten hat. |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node) | Gibt den Index des angegebenen Kindknotens im Kindknoten-Array zurück. |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node) | Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein. |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node) | Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein. |
| [isComposite()](#isComposite) | Gibt  true  zurück, da dieser Knoten Kindknoten haben kann. |
| [isFirstRow()](#isFirstRow) | True, wenn dies die erste Zeile in einer Tabelle ist; sonst false. |
| [isLastRow()](#isLastRow) | True, wenn dies die letzte Zeile in einer Tabelle ist; sonst false. |
| [iterator()](#iterator) | Bietet Unterstützung für die foreach‑artige Iteration über die Kindknoten dieses Knotens. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node) | Ermittelt den nächsten Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int) |  |
| [prependChild(Node newChild)](#prependChild-com.aspose.words.Node) | Fügt den angegebenen Knoten am Anfang der Liste der Kindknoten dieses Knotens hinzu. |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node) | Ermittelt den vorherigen Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| [remove()](#remove) | Entfernt sich selbst vom übergeordneten Element. |
| [removeAllChildren()](#removeAllChildren) | Entfernt alle Kindknoten des aktuellen Knotens. |
| [removeChild(Node oldChild)](#removeChild-com.aspose.words.Node) | Entfernt den angegebenen Kindknoten. |
| [removeMoveRevisions()](#removeMoveRevisions) |  |
| [removeSmartTags()](#removeSmartTags) | Entfernt alle [SmartTag](../../com.aspose.words/smarttag/) Nachfahrenknoten des aktuellen Knotens. |
| [resetToDefaultAttrs()](#resetToDefaultAttrs) |  |
| [selectNodes(String xpath)](#selectNodes-java.lang.String) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String) | Wählt den ersten [Node](../../com.aspose.words/node/) aus, der dem XPath-Ausdruck entspricht. |
| [setCustomNodeId(int value)](#setCustomNodeId-int) | Gibt eine benutzerdefinierte Knotenkennung an. |
| [setHidden(boolean value)](#setHidden-boolean) | Setzt ein Flag, das angibt, ob diese Zeile ausgeblendet ist oder nicht. |
| [setRowAttr(int key, Object value)](#setRowAttr-int-java.lang.Object) |  |
| [toString()](#toString) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions) | Exportiert den Inhalt des Knotens in einen String unter Verwendung der angegebenen Speicheroptionen. |
| [toString(int saveFormat)](#toString-int) |  |
### Row(DocumentBase doc) {#Row-com.aspose.words.DocumentBase}
```
public Row(DocumentBase doc)
```


Initialisiert eine neue Instanz der Klasse [Row](../../com.aspose.words/row/).

 **Remarks:** 

Wenn [Row](../../com.aspose.words/row/) erstellt wird, gehört sie zum angegebenen Dokument, ist aber noch nicht Teil des Dokuments und [Node.getParentNode()](../../com.aspose.words/node/\#getParentNode) ist  null .

Um [Row](../../com.aspose.words/row/) an das Dokument anzuhängen, verwenden Sie [CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertAfter-com.aspose.words.Node--com.aspose.words.Node) oder [CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertBefore-com.aspose.words.Node--com.aspose.words.Node) auf der Tabelle, in die Sie die Zeile einfügen möchten.

 **Examples:** 

Zeigt, wie man eine verschachtelte Tabelle erstellt, ohne einen Document Builder zu verwenden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase/) | Das übergeordnete Dokument. |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor}
```
public boolean accept(DocumentVisitor visitor)
```


Akzeptiert einen Besucher.

 **Remarks:** 

Enumeriert diesen Knoten und alle seine Kinder. Jeder Knoten ruft die entsprechende Methode auf [DocumentVisitor](../../com.aspose.words/documentvisitor/).

Weitere Informationen finden Sie im Visitor-Entwurfsmuster.

Ruft [DocumentVisitor.visitRowStart(com.aspose.words.Row)](../../com.aspose.words/documentvisitor/\#visitRowStart-com.aspose.words.Row) auf, dann [Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node/\#accept-com.aspose.words.DocumentVisitor) für alle Kindknoten des Abschnitts und schließlich [DocumentVisitor.visitRowEnd(com.aspose.words.Row)](../../com.aspose.words/documentvisitor/\#visitRowEnd-com.aspose.words.Row) am Ende auf.

 **Examples:** 

Zeigt, wie man die Knotenstruktur jeder Tabelle in einem Dokument ausgibt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | Der Visitor, der die Knoten besuchen wird. |

**Returns:**
boolean - True, wenn alle Knoten besucht wurden; false, wenn [DocumentVisitor](../../com.aspose.words/documentvisitor/) die Operation beendet hat, bevor alle Knoten besucht wurden.
### acceptEnd(DocumentVisitor visitor) {#acceptEnd-com.aspose.words.DocumentVisitor}
```
public int acceptEnd(DocumentVisitor visitor)
```


Akzeptiert einen Besucher, um das Ende der Zeile zu besuchen.

 **Examples:** 

Zeigt, wie man die Knotenstruktur jeder Tabelle in einem Dokument ausgibt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | Der Dokumentbesucher. |

**Returns:**
int - Die vom Besucher auszuführende Aktion. Der zurückgegebene Wert ist einer der Konstanten von [VisitorAction](../../com.aspose.words/visitoraction/).
### acceptStart(DocumentVisitor visitor) {#acceptStart-com.aspose.words.DocumentVisitor}
```
public int acceptStart(DocumentVisitor visitor)
```


Akzeptiert einen Besucher, um den Anfang der Zeile zu besuchen.

 **Examples:** 

Zeigt, wie man die Knotenstruktur jeder Tabelle in einem Dokument ausgibt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | Der Dokumentbesucher. |

**Returns:**
int - Die vom Besucher auszuführende Aktion. Der zurückgegebene Wert ist einer der Konstanten von [VisitorAction](../../com.aspose.words/visitoraction/).
### appendChild(Node newChild) {#appendChild-com.aspose.words.Node}
```
public Node appendChild(Node newChild)
```


Fügt den angegebenen Knoten am Ende der Liste von Kindknoten dieses Knotens hinzu.

 **Remarks:** 

Wenn der  newChild  bereits im Baum ist, wird er zuerst entfernt.

Wenn der einzufügende Knoten aus einem anderen Dokument erstellt wurde, sollten Sie **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** verwenden, um den Knoten in das aktuelle Dokument zu importieren. Der importierte Knoten kann dann in das aktuelle Dokument eingefügt werden.

 **Examples:** 

Zeigt, wie man ein Aspose.Words-Dokument von Hand erstellt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | Der hinzuzufügende Knoten. |

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


Erstellt ein Duplikat des Knotens.

 **Remarks:** 

Diese Methode dient als Kopierkonstruktor für Knoten. Der geklonte Knoten hat keinen übergeordneten Knoten, gehört jedoch zum selben Dokument wie der ursprüngliche Knoten.

Diese Methode führt immer eine tiefe Kopie des Knotens aus. Der Parameter isCloneChildren gibt an, ob ebenfalls alle Kindknoten kopiert werden sollen.

 **Examples:** 

Zeigt, wie ein zusammengesetzter Knoten geklont wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| isCloneChildren | boolean | True, um den Unterbaum unter dem angegebenen Knoten rekursiv zu klonen; false, um nur den Knoten selbst zu klonen. |

**Returns:**
[Node](../../com.aspose.words/node/) - The cloned node.
### ensureMinimum() {#ensureMinimum}
```
public void ensureMinimum()
```


Wenn die [Row](../../com.aspose.words/row/) keine Zellen hat, wird eine [Cell](../../com.aspose.words/cell/) erstellt und angehängt.

 **Examples:** 

Zeigt, wie sichergestellt wird, dass ein Zeilenknoten die Knoten enthält, die wir benötigen, um Inhalte hinzuzufügen.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchRowAttr(int key) {#fetchRowAttr-int}
```
public Object fetchRowAttr(int key)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getAncestor(int ancestorType) {#getAncestor-int}
```
public CompositeNode getAncestor(int ancestorType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| ancestorType | int |  |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/)
### getAncestor(Class ancestorType) {#getAncestor-java.lang.Class}
```
public CompositeNode getAncestor(Class ancestorType)
```


Ermittelt den ersten Vorfahren des angegebenen Objekttyps.

 **Remarks:** 

Der Ancestor-Typ stimmt überein, wenn er gleich ancestorType ist oder von ancestorType abgeleitet ist.

 **Examples:** 

Zeigt, wie man herausfindet, ob Tabellen verschachtelt sind.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| ancestorType | java.lang.Class | Der Objekttyp des abzurufenden Ancestors. |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/) - The ancestor of the specified type or  null  if no ancestor of this type was found.
### getCells() {#getCells}
```
public CellCollection getCells()
```


Bietet typisierten Zugriff auf die [Cell](../../com.aspose.words/cell/) Kindknoten der Zeile.

 **Examples:** 

Zeigt, wie man durch alle Tabellen im Dokument iteriert und den Inhalt jeder Zelle ausgibt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| nodeType | int |  |
| Index | int |  |
| isDeep | boolean |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### getChildNodes(int nodeType, boolean isDeep) {#getChildNodes-int-boolean}
```
public NodeCollection getChildNodes(int nodeType, boolean isDeep)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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


Ermittelt die Anzahl der unmittelbaren Kindknoten dieses Knotens.

 **Examples:** 

Zeigt, wie man Kindknoten in der Sammlung von Kindknoten eines CompositeNode hinzufügt, aktualisiert und löscht.

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
int - Die Anzahl der unmittelbaren Kindknoten dieses Knotens.
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


Gibt eine benutzerdefinierte Knotenkennung an.

 **Remarks:** 

Standardwert ist 0.

Dieser Bezeichner kann beliebig gesetzt und verwendet werden. Zum Beispiel als Schlüssel, um externe Daten abzurufen.

Wichtiger Hinweis: Der angegebene Wert wird nicht in einer Ausgabedatei gespeichert und existiert nur während der Lebensdauer des Knotens.

 **Examples:** 

Zeigt, wie man die Sammlung von Kindknoten eines zusammengesetzten Knotens durchläuft.

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
int - Der entsprechende int-Wert.
### getDirectRowAttr(int key) {#getDirectRowAttr-int}
```
public Object getDirectRowAttr(int key)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Ermittelt das Dokument, zu dem dieser Knoten gehört.

 **Remarks:** 

Der Knoten gehört immer zu einem Dokument, selbst wenn er gerade erst erstellt wurde und noch nicht zum Baum hinzugefügt wurde oder wenn er aus dem Baum entfernt wurde.

 **Examples:** 

Zeigt, wie man einen Knoten erstellt und sein zugehöriges Dokument festlegt.

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


Gibt die erste [Cell](../../com.aspose.words/cell/) in der Zeile zurück.

 **Examples:** 

Zeigt, wie man die Knotenstruktur jeder Tabelle in einem Dokument ausgibt.

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


Ermittelt das erste Kind des Knotens.

 **Remarks:** 

Wenn es keinen ersten Kindknoten gibt, wird ein  null  zurückgegeben.

 **Examples:** 

Zeigt, wie man den Baum von Kindknoten eines zusammengesetzten Knotens durchläuft.

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

Zeigt, wie man die Eigenschaft NextSibling eines Knotens verwendet, um seine unmittelbaren Kinder zu enumerieren.

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


Ermittelt ein Flag, das angibt, ob diese Zeile ausgeblendet ist oder nicht.

 **Remarks:** 

Versteckte Zeilen werden für WordML- und ODT-Dokumente nicht unterstützt.

 **Examples:** 

Zeigt, wie man eine Tabellenzeile ausblendet.

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
boolean - Ein Flag, das angibt, ob diese Zeile ausgeblendet ist oder nicht.
### getLastCell() {#getLastCell}
```
public Cell getLastCell()
```


Gibt die letzte [Cell](../../com.aspose.words/cell/) in der Zeile zurück.

 **Examples:** 

Zeigt, wie man die Knotenstruktur jeder Tabelle in einem Dokument ausgibt.

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


Ermittelt das letzte Kind des Knotens.

 **Remarks:** 

Wenn es keinen letzten Kindknoten gibt, wird ein  null  zurückgegeben.

 **Examples:** 

Zeigt, wie man Methoden von Node und CompositeNode verwendet, um einen Abschnitt vor dem letzten Abschnitt im Dokument zu entfernen.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node/) |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### getNextRow() {#getNextRow}
```
public Row getNextRow()
```


Ermittelt den nächsten [Row](../../com.aspose.words/row/) Knoten.

 **Remarks:** 

Die Methode kann verwendet werden, wenn Sie typisierten Zugriff auf Tabellenzeilen benötigen. Wenn ein [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) Knoten in einer Tabelle anstelle einer Zeile gefunden wird, wird automatisch traversiert, um die enthaltene Zeile zu erhalten.

 **Examples:** 

Zeigt, wie man alle Tabellenzellen enumeriert.

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


Ermittelt den Knoten, der unmittelbar auf diesen Knoten folgt.

 **Remarks:** 

Wenn es keinen nächsten Knoten gibt, wird ein  null  zurückgegeben.

 **Examples:** 

Zeigt, wie man den Baum von Kindknoten eines zusammengesetzten Knotens durchläuft.

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

Zeigt, wie man die Eigenschaft NextSibling eines Knotens verwendet, um seine unmittelbaren Kinder zu enumerieren.

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


Gibt [NodeType.ROW](../../com.aspose.words/nodetype/\#ROW) zurück.

 **Examples:** 

Zeigt, wie man den Baum von Kindknoten eines zusammengesetzten Knotens durchläuft.

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
int - [NodeType.ROW](../../com.aspose.words/nodetype/\#ROW). Der zurückgegebene Wert ist einer der [NodeType](../../com.aspose.words/nodetype/) Konstanten.
### getParentNode() {#getParentNode}
```
public CompositeNode getParentNode()
```


Ermittelt den unmittelbaren übergeordneten Knoten dieses Knotens.

 **Remarks:** 

Wenn ein Knoten gerade erstellt wurde und noch nicht zum Baum hinzugefügt wurde, oder wenn er aus dem Baum entfernt wurde, ist der übergeordnete Knoten  null .

 **Examples:** 

Zeigt, wie man auf den übergeordneten Knoten eines Knotens zugreift.

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

Zeigt, wie man einen Knoten erstellt und sein zugehöriges Dokument festlegt.

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


Gibt die unmittelbare übergeordnete Tabelle der Zeile zurück.

 **Examples:** 

Zeigt, wie man die Knotenstruktur jeder Tabelle in einem Dokument ausgibt.

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


Liefert den vorherigen [Row](../../com.aspose.words/row/) Knoten.

 **Remarks:** 

Die Methode kann verwendet werden, wenn Sie typisierten Zugriff auf Tabellenzeilen benötigen. Wenn ein [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) Knoten in einer Tabelle anstelle einer Zeile gefunden wird, wird automatisch traversiert, um die enthaltene Zeile zu erhalten.

 **Examples:** 

Zeigt, wie man alle Tabellenzellen enumeriert.

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


Ermittelt den Knoten, der unmittelbar vor diesem Knoten liegt.

 **Remarks:** 

Wenn es keinen vorhergehenden Knoten gibt, wird ein  null  zurückgegeben.

 **Examples:** 

Zeigt, wie man Methoden von Node und CompositeNode verwendet, um einen Abschnitt vor dem letzten Abschnitt im Dokument zu entfernen.

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


Gibt ein [Range](../../com.aspose.words/range/)-Objekt zurück, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist.

 **Examples:** 

Zeigt, wie man alle Knoten aus einem Bereich löscht.

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


Stellt Zugriff auf die Formatierungseigenschaften der Zeile bereit.

 **Examples:** 

Zeigt, wie man das Format von Zeilen und Zellen in einer Tabelle ändert.

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

Zeigt, wie man die Formatierung einer Tabellenzeile ändert.

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


Liefert den Text aller Zellen in dieser Zeile einschließlich des Zeilenendezeichens.

 **Remarks:** 

Gibt den zusammengefügten Text aller Kindknoten zurück, wobei das Zeilenendezeichen [ControlChar.CELL](../../com.aspose.words/controlchar/\#CELL) am Ende angehängt wird.

Der zurückgegebene String enthält alle Steuer- und Sonderzeichen, wie in [ControlChar](../../com.aspose.words/controlchar/) beschrieben.

 **Examples:** 

Zeigt, wie man die Knotenstruktur jeder Tabelle in einem Dokument ausgibt.

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


Gibt  true  zurück, wenn dieser Knoten Kindknoten hat.

 **Examples:** 

Zeigt, wie man die Zeilen aus zwei Tabellen zu einer kombiniert.

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
boolean -  true  wenn dieser Knoten Kindknoten hat.
### indexOf(Node child) {#indexOf-com.aspose.words.Node}
```
public int indexOf(Node child)
```


Gibt den Index des angegebenen Kindknotens im Kindknoten-Array zurück.

 **Remarks:** 

Gibt -1 zurück, wenn der Knoten in den Kindknoten nicht gefunden wird.

 **Examples:** 

Zeigt, wie man den Index eines bestimmten Kindknotens vom übergeordneten Knoten erhält.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 Body body = doc.getFirstSection().getBody();

 // Retrieve the index of the last paragraph in the body of the first section.
 Assert.assertEquals(24, body.getChildNodes(NodeType.ANY, false).indexOf(body.getLastParagraph()));
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| child | [Node](../../com.aspose.words/node/) |  |

**Returns:**
int
### insertAfter(Node newChild, Node refChild) {#insertAfter-com.aspose.words.Node-com.aspose.words.Node}
```
public Node insertAfter(Node newChild, Node refChild)
```


Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein.

 **Remarks:** 

Wenn  refChild  null ist, wird  newChild  am Anfang der Liste der Kindknoten eingefügt.

Wenn der  newChild  bereits im Baum ist, wird er zuerst entfernt.

Wenn der einzufügende Knoten aus einem anderen Dokument erstellt wurde, sollten Sie **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** verwenden, um den Knoten in das aktuelle Dokument zu importieren. Der importierte Knoten kann dann in das aktuelle Dokument eingefügt werden.

 **Examples:** 

Zeigt, wie man Kindknoten in der Sammlung von Kindknoten eines CompositeNode hinzufügt, aktualisiert und löscht.

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

Zeigt, wie man alle Textfeldformen durch Bildformen ersetzt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | Der [Node](../../com.aspose.words/node/) zum Einfügen. |
| refChild | [Node](../../com.aspose.words/node/) | Der [Node](../../com.aspose.words/node/), der der Referenzknoten ist. Der  newChild  wird nach dem  refChild  platziert. |

**Returns:**
[Node](../../com.aspose.words/node/) - The inserted node.
### insertBefore(Node newChild, Node refChild) {#insertBefore-com.aspose.words.Node-com.aspose.words.Node}
```
public Node insertBefore(Node newChild, Node refChild)
```


Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein.

 **Remarks:** 

Wenn  refChild  null ist, wird  newChild  am Ende der Liste der Kindknoten eingefügt.

Wenn der  newChild  bereits im Baum ist, wird er zuerst entfernt.

Wenn der einzufügende Knoten aus einem anderen Dokument erstellt wurde, sollten Sie **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** verwenden, um den Knoten in das aktuelle Dokument zu importieren. Der importierte Knoten kann dann in das aktuelle Dokument eingefügt werden.

 **Examples:** 

Zeigt, wie man Kindknoten in der Sammlung von Kindknoten eines CompositeNode hinzufügt, aktualisiert und löscht.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | Der [Node](../../com.aspose.words/node/) zum Einfügen. |
| refChild | [Node](../../com.aspose.words/node/) | Der [Node](../../com.aspose.words/node/), der der Referenzknoten ist. Der  newChild  wird vor diesem Knoten platziert. |

**Returns:**
[Node](../../com.aspose.words/node/) - The inserted node.
### isComposite() {#isComposite}
```
public boolean isComposite()
```


Gibt  true  zurück, da dieser Knoten Kindknoten haben kann.

 **Examples:** 

Zeigt, wie man den Baum von Kindknoten eines zusammengesetzten Knotens durchläuft.

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
boolean -  true  da dieser Knoten Kindknoten haben kann.
### isFirstRow() {#isFirstRow}
```
public boolean isFirstRow()
```


True, wenn dies die erste Zeile in einer Tabelle ist; sonst false.

 **Examples:** 

Zeigt, wie man die Knotenstruktur jeder Tabelle in einem Dokument ausgibt.

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
boolean - Der entsprechende  boolean  Wert.
### isLastRow() {#isLastRow}
```
public boolean isLastRow()
```


True, wenn dies die letzte Zeile in einer Tabelle ist; sonst false.

 **Examples:** 

Zeigt, wie man eine Tabelle so einstellt, dass sie auf derselben Seite zusammenbleibt.

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
boolean - Der entsprechende  boolean  Wert.
### iterator() {#iterator}
```
public Iterator iterator()
```


Bietet Unterstützung für die foreach‑artige Iteration über die Kindknoten dieses Knotens.

 **Examples:** 

Zeigt, wie man alle Kommentare eines Dokuments und deren Antworten ausdruckt.

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


Ermittelt den nächsten Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus.

 **Examples:** 

Zeigt, wie man den Knotbaum des Dokuments mit dem Preorder‑Durchlaufalgorithmus durchläuft und jede gefundene Form mit einem Bild löscht.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node/) | Der oberste Knoten (Grenze) des Durchlaufs. |

**Returns:**
[Node](../../com.aspose.words/node/) - Next node in pre-order order. Null if reached the  rootNode .
### nodeTypeToString(int nodeType) {#nodeTypeToString-int}
```
public static String nodeTypeToString(int nodeType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
### prependChild(Node newChild) {#prependChild-com.aspose.words.Node}
```
public Node prependChild(Node newChild)
```


Fügt den angegebenen Knoten am Anfang der Liste der Kindknoten dieses Knotens hinzu.

 **Remarks:** 

Wenn der  newChild  bereits im Baum ist, wird er zuerst entfernt.

Wenn der einzufügende Knoten aus einem anderen Dokument erstellt wurde, sollten Sie **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** verwenden, um den Knoten in das aktuelle Dokument zu importieren. Der importierte Knoten kann dann in das aktuelle Dokument eingefügt werden.

 **Examples:** 

Zeigt, wie man Kindknoten in der Sammlung von Kindknoten eines CompositeNode hinzufügt, aktualisiert und löscht.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | Der hinzuzufügende Knoten. |

**Returns:**
[Node](../../com.aspose.words/node/) - The node added.
### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node}
```
public Node previousPreOrder(Node rootNode)
```


Ermittelt den vorherigen Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus.

 **Examples:** 

Zeigt, wie man den Knotbaum des Dokuments mit dem Preorder‑Durchlaufalgorithmus durchläuft und jede gefundene Form mit einem Bild löscht.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node/) | Der oberste Knoten (Grenze) des Durchlaufs. |

**Returns:**
[Node](../../com.aspose.words/node/) - Previous node in pre-order order. Null if reached the  rootNode .
### remove() {#remove}
```
public void remove()
```


Entfernt sich selbst vom übergeordneten Element.

 **Examples:** 

Zeigt, wie man alle Formen mit Bildern aus einem Dokument löscht.

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

Zeigt, wie man alle Kindknoten eines bestimmten Typs aus einem zusammengesetzten Knoten entfernt.

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


Entfernt alle Kindknoten des aktuellen Knotens.

 **Examples:** 

Zeigt, wie man ein Aspose.Words-Dokument von Hand erstellt.

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


Entfernt den angegebenen Kindknoten.

 **Remarks:** 

Das übergeordnete Element von  oldChild  wird nach dem Entfernen des Knotens auf  null  gesetzt.

 **Examples:** 

Zeigt, wie man Methoden von Node und CompositeNode verwendet, um einen Abschnitt vor dem letzten Abschnitt im Dokument zu entfernen.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| oldChild | [Node](../../com.aspose.words/node/) | Der zu entfernende Knoten. |

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


Entfernt alle [SmartTag](../../com.aspose.words/smarttag/) Nachfahrenknoten des aktuellen Knotens.

 **Remarks:** 

Diese Methode entfernt nicht den Inhalt der SmartTags.

 **Examples:** 

Entfernt alle SmartTags aus den Nachfolgerknoten eines zusammengesetzten Knotens.

```

 Document doc = new Document(getMyDir() + "Smart tags.doc");

 Assert.assertEquals(8, doc.getChildNodes(NodeType.SMART_TAG, true).getCount());

 doc.removeSmartTags();

 Assert.assertEquals(0, doc.getChildNodes(NodeType.SMART_TAG, true).getCount());
 
```

Zeigt, wie man Smart Tags erstellt.

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


Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen.

 **Remarks:** 

Derzeit werden nur Ausdrücke mit Elementnamen unterstützt. Ausdrücke, die Attributnamen verwenden, werden nicht unterstützt.

 **Examples:** 

Zeigt, wie man bestimmte Knoten mithilfe eines XPath-Ausdrucks auswählt.

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

Zeigt, wie man einen XPath-Ausdruck verwendet, um zu prüfen, ob ein Knoten innerhalb eines Feldes liegt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xpath | java.lang.String | Der XPath-Ausdruck. |

**Returns:**
[NodeList](../../com.aspose.words/nodelist/) - A list of nodes matching the XPath query.
### selectSingleNode(String xpath) {#selectSingleNode-java.lang.String}
```
public Node selectSingleNode(String xpath)
```


Wählt den ersten [Node](../../com.aspose.words/node/) aus, der dem XPath-Ausdruck entspricht.

 **Remarks:** 

Derzeit werden nur Ausdrücke mit Elementnamen unterstützt. Ausdrücke, die Attributnamen verwenden, werden nicht unterstützt.

 **Examples:** 

Zeigt, wie man bestimmte Knoten mithilfe eines XPath-Ausdrucks auswählt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xpath | java.lang.String | Der XPath-Ausdruck. |

**Returns:**
[Node](../../com.aspose.words/node/) - The first [Node](../../com.aspose.words/node/) that matches the XPath query or  null  if no matching node is found.
### setCustomNodeId(int value) {#setCustomNodeId-int}
```
public void setCustomNodeId(int value)
```


Gibt eine benutzerdefinierte Knotenkennung an.

 **Remarks:** 

Standardwert ist 0.

Dieser Bezeichner kann beliebig gesetzt und verwendet werden. Zum Beispiel als Schlüssel, um externe Daten abzurufen.

Wichtiger Hinweis: Der angegebene Wert wird nicht in einer Ausgabedatei gespeichert und existiert nur während der Lebensdauer des Knotens.

 **Examples:** 

Zeigt, wie man die Sammlung von Kindknoten eines zusammengesetzten Knotens durchläuft.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der entsprechende  int  Wert. |

### setHidden(boolean value) {#setHidden-boolean}
```
public void setHidden(boolean value)
```


Setzt ein Flag, das angibt, ob diese Zeile ausgeblendet ist oder nicht.

 **Remarks:** 

Versteckte Zeilen werden für WordML- und ODT-Dokumente nicht unterstützt.

 **Examples:** 

Zeigt, wie man eine Tabellenzeile ausblendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein Flag, das angibt, ob diese Zeile ausgeblendet ist oder nicht. |

### setRowAttr(int key, Object value) {#setRowAttr-int-java.lang.Object}
```
public void setRowAttr(int key, Object value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |
| Wert | java.lang.Object |  |

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


Exportiert den Inhalt des Knotens in einen String unter Verwendung der angegebenen Speicheroptionen.

 **Examples:** 

Exportiert den Inhalt eines Knotens als String im HTML-Format.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Gibt die Optionen an, die steuern, wie der Knoten gespeichert wird. |

**Returns:**
java.lang.String - Der Inhalt des Knotens im angegebenen Format.
### toString(int saveFormat) {#toString-int}
```
public String toString(int saveFormat)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
