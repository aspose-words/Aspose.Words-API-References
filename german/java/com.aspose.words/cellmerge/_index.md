---
title: "CellMerge"
linktitle: "CellMerge"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie eine Zelle in einer Tabelle in Java mit anderen Zellen zusammengeführt wird."
type: docs
weight: 62
url: /de/java/com.aspose.words/cellmerge/
---

**Inheritance:**
java.lang.Object
```
public class CellMerge
```

Gibt an, wie eine Zelle in einer Tabelle mit anderen Zellen zusammengeführt wird.

 **Examples:** 

Zeigt, wie man Tabellenzellen vertikal zusammenführt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a cell into the first column of the first row.
 // This cell will be the first in a range of vertically merged cells.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.FIRST);
 builder.write("Text in merged cells.");

 // Insert a cell into the second column of the first row, then end the row.
 // Also, configure the builder to disable vertical merging in created cells.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.NONE);
 builder.write("Text in unmerged cell.");
 builder.endRow();

 // Insert a cell into the first column of the second row.
 // Instead of adding text contents, we will merge this cell with the first cell that we added directly above.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.PREVIOUS);

 // Insert another independent cell in the second column of the second row.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.NONE);
 builder.write("Text in unmerged cell.");
 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "CellFormat.VerticalMerge.docx");
 
```

Zeigt, wie Tabellenzellen horizontal zusammengeführt werden.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a cell into the first column of the first row.
 // This cell will be the first in a range of horizontally merged cells.
 builder.insertCell();
 builder.getCellFormat().setHorizontalMerge(CellMerge.FIRST);
 builder.write("Text in merged cells.");

 // Insert a cell into the second column of the first row. Instead of adding text contents,
 // we will merge this cell with the first cell that we added directly to the left.
 builder.insertCell();
 builder.getCellFormat().setHorizontalMerge(CellMerge.PREVIOUS);
 builder.endRow();

 // Insert two more unmerged cells to the second row.
 builder.getCellFormat().setHorizontalMerge(CellMerge.NONE);
 builder.insertCell();
 builder.write("Text in unmerged cell.");
 builder.insertCell();
 builder.write("Text in unmerged cell.");
 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "CellFormat.HorizontalMerge.docx");
 
```

Gibt den horizontalen und vertikalen Zusammenführungs­typ einer Zelle aus.

```

 public void checkCellsMerged() throws Exception {
     Document doc = new Document(getMyDir() + "Table with merged cells.docx");
     Table table = doc.getFirstSection().getBody().getTables().get(0);

     for (Row row : table.getRows()) {
         for (Cell cell : row.getCells()) {
             System.out.println(printCellMergeType(cell));
         }
     }
 }

 public String printCellMergeType(Cell cell) {
     boolean isHorizontallyMerged = cell.getCellFormat().getHorizontalMerge() != CellMerge.NONE;
     boolean isVerticallyMerged = cell.getCellFormat().getVerticalMerge() != CellMerge.NONE;
     String cellLocation =
             MessageFormat.format("R{0}, C{1}", cell.getParentRow().getParentTable().indexOf(cell.getParentRow()) + 1, cell.getParentRow().indexOf(cell) + 1);

     if (isHorizontallyMerged && isVerticallyMerged)
         return MessageFormat.format("The cell at {0} is both horizontally and vertically merged", cellLocation);
     if (isHorizontallyMerged)
         return MessageFormat.format("The cell at {0} is horizontally merged.", cellLocation);

     return isVerticallyMerged ? MessageFormat.format("The cell at {0} is vertically merged", cellLocation) : MessageFormat.format("The cell at {0} is not merged", cellLocation);
 }
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [FIRST](#FIRST) | Die Zelle ist die erste Zelle in einem Bereich zusammengeführter Zellen. |
| [NONE](#NONE) | Die Zelle ist nicht zusammengeführt. |
| [PREVIOUS](#PREVIOUS) | Die Zelle ist horizontal oder vertikal mit der vorherigen Zelle zusammengeführt. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String cellMergeName)](#fromName-java.lang.String) |  |
| [getName(int cellMerge)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int cellMerge)](#toString-int) |  |
### FIRST {#FIRST}
```
public static int FIRST
```


Die Zelle ist die erste Zelle in einem Bereich zusammengeführter Zellen.

### NONE {#NONE}
```
public static int NONE
```


Die Zelle ist nicht zusammengeführt.

### PREVIOUS {#PREVIOUS}
```
public static int PREVIOUS
```


Die Zelle ist horizontal oder vertikal mit der vorherigen Zelle zusammengeführt.

### length {#length}
```
public static int length
```


### fromName(String cellMergeName) {#fromName-java.lang.String}
```
public static int fromName(String cellMergeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| cellMergeName | java.lang.String |  |

**Returns:**
int
### getName(int cellMerge) {#getName-int}
```
public static String getName(int cellMerge)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| cellMerge | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int cellMerge) {#toString-int}
```
public static String toString(int cellMerge)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| cellMerge | int |  |

**Returns:**
java.lang.String
