---
title: "SectionLayoutMode"
linktitle: "SectionLayoutMode"
second_title: "Aspose.Words für Java"
description: "Gibt den Layoutmodus für einen Abschnitt an, der es ermöglicht, das Verhalten des Dokumentengitters in Java zu definieren."
type: docs
weight: 607
url: /de/java/com.aspose.words/sectionlayoutmode/
---

**Inheritance:**
java.lang.Object
```
public class SectionLayoutMode
```

Legt den Layout‑Modus für einen Abschnitt fest, der die Definition des Dokument‑Gitternetz‑Verhaltens ermöglicht.

 **Examples:** 

Zeigt, wie man eine Begrenzung für die Anzahl der Zeichen festlegt, die jede Zeile haben darf.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of characters per line in this section.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.GRID);
 builder.getPageSetup().setCharactersPerLine(10);

 // The number of characters also depends on the size of the font.
 doc.getStyles().get("Normal").getFont().setSize(20.0);

 Assert.assertEquals(8, doc.getFirstSection().getPageSetup().getCharactersPerLine());

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "PageSetup.CharactersPerLine.docx");
 
```

Zeigt, wie man ein Limit für die Zeilenanzahl festlegt, die jede Seite haben darf.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Enable pitching, and then use it to set the number of lines per page in this section.
 // A large enough font size will push some lines down onto the next page to avoid overlapping characters.
 builder.getPageSetup().setLayoutMode(SectionLayoutMode.LINE_GRID);
 builder.getPageSetup().setLinesPerPage(15);

 builder.getParagraphFormat().setSnapToGrid(true);

 for (int i = 0; i < 30; i++)
     builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

 doc.save(getArtifactsDir() + "PageSetup.LinesPerPage.docx");
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [DEFAULT](#DEFAULT) | Gibt an, dass kein Dokumentengitter auf den Inhalt des entsprechenden Abschnitts im Dokument angewendet werden soll. |
| [GRID](#GRID) | Gibt an, dass der entsprechende Abschnitt sowohl den zusätzlichen Zeilenabstand als auch den Zeichenabstand zu jeder Zeile und jedem Zeichen innerhalb des Abschnitts hinzufügt, um eine bestimmte Anzahl von Zeilen pro Seite und Zeichen pro Zeile beizubehalten. |
| [LINE_GRID](#LINE-GRID) | Gibt an, dass dem entsprechenden Abschnitt ein zusätzlicher Zeilenabstand zu jeder Zeile innerhalb des Abschnitts hinzugefügt wird, um die angegebene Anzahl von Zeilen pro Seite beizubehalten. |
| [SNAP_TO_CHARS](#SNAP-TO-CHARS) | Gibt an, dass der entsprechende Abschnitt sowohl den zusätzlichen Zeilenabstand als auch den Zeichenabstand zu jeder Zeile und jedem Zeichen innerhalb des Abschnitts hinzufügt, um eine bestimmte Anzahl von Zeilen pro Seite und Zeichen pro Zeile beizubehalten. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String sectionLayoutModeName)](#fromName-java.lang.String) |  |
| [getName(int sectionLayoutMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sectionLayoutMode)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Gibt an, dass kein Dokumentengitter auf den Inhalt des entsprechenden Abschnitts im Dokument angewendet werden soll.

### GRID {#GRID}
```
public static int GRID
```


Gibt an, dass dem entsprechenden Abschnitt sowohl der zusätzliche Zeilenabstand als auch der Zeichenabstand zu jeder Zeile und jedem Zeichen innerhalb des Abschnitts hinzugefügt werden, um eine bestimmte Anzahl von Zeilen pro Seite und Zeichen pro Zeile beizubehalten. Zeichen werden beim Tippen nicht automatisch an den Gitterlinien ausgerichtet.

### LINE_GRID {#LINE-GRID}
```
public static int LINE_GRID
```


Gibt an, dass dem entsprechenden Abschnitt ein zusätzlicher Zeilenabstand zu jeder Zeile innerhalb des Abschnitts hinzugefügt wird, um die angegebene Anzahl von Zeilen pro Seite beizubehalten.

### SNAP_TO_CHARS {#SNAP-TO-CHARS}
```
public static int SNAP_TO_CHARS
```


Gibt an, dass dem entsprechenden Abschnitt sowohl der zusätzliche Zeilenabstand als auch der Zeichenabstand zu jeder Zeile und jedem Zeichen innerhalb des Abschnitts hinzugefügt werden, um eine bestimmte Anzahl von Zeilen pro Seite und Zeichen pro Zeile beizubehalten. Zeichen werden beim Tippen automatisch an den Gitterlinien ausgerichtet.

### length {#length}
```
public static int length
```


### fromName(String sectionLayoutModeName) {#fromName-java.lang.String}
```
public static int fromName(String sectionLayoutModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sectionLayoutModeName | java.lang.String |  |

**Returns:**
int
### getName(int sectionLayoutMode) {#getName-int}
```
public static String getName(int sectionLayoutMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sectionLayoutMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int sectionLayoutMode) {#toString-int}
```
public static String toString(int sectionLayoutMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sectionLayoutMode | int |  |

**Returns:**
java.lang.String
