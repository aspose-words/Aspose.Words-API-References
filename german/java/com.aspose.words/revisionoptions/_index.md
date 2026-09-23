---
title: "RevisionOptions"
linktitle: "RevisionOptions"
second_title: "Aspose.Words für Java"
description: "Ermöglicht die Steuerung, wie Dokumentrevisionen während des Layout‑Vorgangs in Java verarbeitet werden."
type: docs
weight: 584
url: /de/java/com.aspose.words/revisionoptions/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class RevisionOptions implements Cloneable
```

Ermöglicht die Steuerung, wie Dokumentrevisionen während des Layoutvorgangs verarbeitet werden.

Um mehr zu erfahren, besuchen Sie den [ Converting to Fixed-page Format ][Converting to Fixed-page Format] Dokumentationsartikel.

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen in einem gerenderten Ausgabedokument geändert wird.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a revision, then change the color of all revisions to green.
 builder.writeln("This is not a revision.");
 doc.startTrackRevisions("John Doe", new Date());
 builder.writeln("This is a revision.");
 doc.stopTrackRevisions();
 builder.writeln("This is not a revision.");

 // Remove the bar that appears to the left of every revised line.
 doc.getLayoutOptions().getRevisionOptions().setInsertedTextColor(RevisionColor.BRIGHT_GREEN);
 doc.getLayoutOptions().getRevisionOptions().setShowRevisionBars(false);
 doc.getLayoutOptions().getRevisionOptions().setRevisionBarsPosition(HorizontalAlignment.RIGHT);

 doc.save(getArtifactsDir() + "Revision.LayoutOptionsRevisions.pdf");
 
```


[Converting to Fixed-page Format]: https://docs.aspose.com/words/java/converting-to-fixed-page-format/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getCommentColor()](#getCommentColor) | Ermöglicht die Angabe der zu verwendenden Farbe für Kommentare. |
| [getDeleteCellColor()](#getDeleteCellColor) | Ermöglicht die Angabe der zu verwendenden Farbe für gelöschte Zellen [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [getDeletedTextColor()](#getDeletedTextColor) | Ermöglicht die Angabe der zu verwendenden Farbe für gelöschten Inhalt [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [getDeletedTextEffect()](#getDeletedTextEffect) | Ermöglicht die Angabe des Effekts, der auf gelöschten Inhalt angewendet wird [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [getInsertCellColor()](#getInsertCellColor) | Ermöglicht die Angabe der zu verwendenden Farbe für eingefügte Zellen [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [getInsertedTextColor()](#getInsertedTextColor) | Ermöglicht die Angabe der zu verwendenden Farbe für eingefügten Inhalt [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [getInsertedTextEffect()](#getInsertedTextEffect) | Ermöglicht die Angabe des Effekts, der auf eingefügten Inhalt angewendet wird [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [getMeasurementUnit()](#getMeasurementUnit) | Ermöglicht die Angabe der Maßeinheiten für Revisionskommentare. |
| [getMovedFromTextColor()](#getMovedFromTextColor) | Ermöglicht die Angabe der zu verwendenden Farbe für Bereiche, aus denen Inhalt verschoben wurde [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [getMovedFromTextEffect()](#getMovedFromTextEffect) | Ermöglicht die Angabe des Effekts, der auf Bereiche angewendet wird, aus denen Inhalt verschoben wurde [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [getMovedToTextColor()](#getMovedToTextColor) | Ermöglicht die Angabe der zu verwendenden Farbe für Bereiche, in die Inhalt verschoben wurde [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [getMovedToTextEffect()](#getMovedToTextEffect) | Ermöglicht die Angabe des Effekts, der auf Bereiche angewendet wird, in die Inhalt verschoben wurde [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [getRevisedPropertiesColor()](#getRevisedPropertiesColor) | Ermöglicht die Angabe der zu verwendenden Farbe für Inhalte mit Änderungen von Formatierungseigenschaften [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE). Der Standardwert ist [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT). |
| [getRevisedPropertiesEffect()](#getRevisedPropertiesEffect) | Ermöglicht die Angabe des Effekts für Inhaltsbereiche mit Änderungen von Formatierungseigenschaften [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE). Der Standardwert ist [RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect/\#NONE). |
| [getRevisionBarsColor()](#getRevisionBarsColor) | Ermöglicht die Angabe der zu verwendenden Farbe für Seitenleisten, die Dokumentzeilen mit überarbeiteten Informationen kennzeichnen. |
| [getRevisionBarsPosition()](#getRevisionBarsPosition) | Ermittelt die Renderposition der Revisionsbalken. |
| [getRevisionBarsWidth()](#getRevisionBarsWidth) | Ermittelt die Breite der Revisionsbalken in Punkten. |
| [getShowInBalloons()](#getShowInBalloons) | Ermöglicht die Angabe, ob die Revisionen in Ballons dargestellt werden. |
| [getShowOriginalRevision()](#getShowOriginalRevision) | Ermöglicht die Angabe, ob der Originaltext anstelle des überarbeiteten angezeigt werden soll. |
| [getShowRevisionBars()](#getShowRevisionBars) | Ermöglicht die Angabe, ob Revisionsbalken in der Nähe von Zeilen mit überarbeitetem Inhalt gerendert werden sollen. |
| [getShowRevisionMarks()](#getShowRevisionMarks) | Ermöglicht die Angabe, ob Revisionstext mit spezieller Formatierung markiert werden soll. |
| [setCommentColor(int value)](#setCommentColor-int) | Ermöglicht die Angabe der zu verwendenden Farbe für Kommentare. |
| [setDeleteCellColor(int value)](#setDeleteCellColor-int) | Ermöglicht die Angabe der zu verwendenden Farbe für gelöschte Zellen [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [setDeletedTextColor(int value)](#setDeletedTextColor-int) | Ermöglicht die Angabe der zu verwendenden Farbe für gelöschten Inhalt [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [setDeletedTextEffect(int value)](#setDeletedTextEffect-int) | Ermöglicht die Angabe des Effekts, der auf gelöschten Inhalt angewendet wird [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). |
| [setInsertCellColor(int value)](#setInsertCellColor-int) | Ermöglicht die Angabe der zu verwendenden Farbe für eingefügte Zellen [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [setInsertedTextColor(int value)](#setInsertedTextColor-int) | Ermöglicht die Angabe der zu verwendenden Farbe für eingefügten Inhalt [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [setInsertedTextEffect(int value)](#setInsertedTextEffect-int) | Ermöglicht die Angabe des Effekts, der auf eingefügten Inhalt angewendet wird [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). |
| [setMeasurementUnit(int value)](#setMeasurementUnit-int) | Ermöglicht die Angabe der Maßeinheiten für Revisionskommentare. |
| [setMovedFromTextColor(int value)](#setMovedFromTextColor-int) | Ermöglicht die Angabe der zu verwendenden Farbe für Bereiche, aus denen Inhalt verschoben wurde [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [setMovedFromTextEffect(int value)](#setMovedFromTextEffect-int) | Ermöglicht die Angabe des Effekts, der auf Bereiche angewendet wird, aus denen Inhalt verschoben wurde [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [setMovedToTextColor(int value)](#setMovedToTextColor-int) | Ermöglicht die Angabe der zu verwendenden Farbe für Bereiche, in die Inhalt verschoben wurde [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [setMovedToTextEffect(int value)](#setMovedToTextEffect-int) | Ermöglicht die Angabe des Effekts, der auf Bereiche angewendet wird, in die Inhalt verschoben wurde [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). |
| [setRevisedPropertiesColor(int value)](#setRevisedPropertiesColor-int) | Ermöglicht die Angabe der zu verwendenden Farbe für Inhalte mit Änderungen von Formatierungseigenschaften [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE). Der Standardwert ist [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT). |
| [setRevisedPropertiesEffect(int value)](#setRevisedPropertiesEffect-int) | Ermöglicht die Angabe des Effekts für Inhaltsbereiche mit Änderungen von Formatierungseigenschaften [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE). Der Standardwert ist [RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect/\#NONE). |
| [setRevisionBarsColor(int value)](#setRevisionBarsColor-int) | Ermöglicht die Angabe der zu verwendenden Farbe für Seitenleisten, die Dokumentzeilen mit überarbeiteten Informationen kennzeichnen. |
| [setRevisionBarsPosition(int value)](#setRevisionBarsPosition-int) | Legt die Renderposition der Revisionsbalken fest. |
| [setRevisionBarsWidth(float value)](#setRevisionBarsWidth-float) | Legt die Breite der Revisionsbalken in Punkten fest. |
| [setShowInBalloons(int value)](#setShowInBalloons-int) | Ermöglicht die Angabe, ob die Revisionen in Ballons dargestellt werden. |
| [setShowOriginalRevision(boolean value)](#setShowOriginalRevision-boolean) | Ermöglicht die Angabe, ob der Originaltext anstelle des überarbeiteten angezeigt werden soll. |
| [setShowRevisionBars(boolean value)](#setShowRevisionBars-boolean) | Ermöglicht die Angabe, ob Revisionsbalken in der Nähe von Zeilen mit überarbeitetem Inhalt gerendert werden sollen. |
| [setShowRevisionMarks(boolean value)](#setShowRevisionMarks-boolean) | Ermöglicht die Angabe, ob Revisionstext mit spezieller Formatierung markiert werden soll. |
### getCommentColor() {#getCommentColor}
```
public int getCommentColor()
```


Ermöglicht die Angabe der für Kommentare zu verwendenden Farbe. Standardwert ist [RevisionColor.RED](../../com.aspose.words/revisioncolor/\#RED).

 **Remarks:** 

Wenn diese Eigenschaft auf die Werte [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR) oder [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT) gesetzt wird, wird sie als Ergebnis auf die Standardfarbe zurückgesetzt.

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen geändert werden kann.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
int – Der entsprechende int‑Wert. Der zurückgegebene Wert ist einer der Konstanten von [RevisionColor](../../com.aspose.words/revisioncolor/).
### getDeleteCellColor() {#getDeleteCellColor}
```
public int getDeleteCellColor()
```


Ermöglicht die Angabe der für gelöschte Zellen zu verwendenden Farbe [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). Standardwert ist [RevisionColor.PINK](../../com.aspose.words/revisioncolor/\#PINK).

 **Examples:** 

Zeigt, wie man mit Einfüge‑/Lösch‑Zell‑Revisionsfarbe arbeitet.

```

 Document doc = new Document(getMyDir() + "Cell revisions.docx");

 doc.getLayoutOptions().getRevisionOptions().setInsertCellColor(RevisionColor.BLUE);
 doc.getLayoutOptions().getRevisionOptions().setDeleteCellColor(RevisionColor.DARK_RED);

 doc.save(getArtifactsDir() + "Revision.RevisionCellColor.pdf");
 
```

**Returns:**
int – Der entsprechende int‑Wert. Der zurückgegebene Wert ist einer der Konstanten von [RevisionColor](../../com.aspose.words/revisioncolor/).
### getDeletedTextColor() {#getDeletedTextColor}
```
public int getDeletedTextColor()
```


Ermöglicht die Angabe der für gelöschten Inhalt zu verwendenden Farbe [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). Standardwert ist [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen geändert werden kann.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
int – Der entsprechende int‑Wert. Der zurückgegebene Wert ist einer der Konstanten von [RevisionColor](../../com.aspose.words/revisioncolor/).
### getDeletedTextEffect() {#getDeletedTextEffect}
```
public int getDeletedTextEffect()
```


Ermöglicht die Angabe des Effekts, der auf gelöschten Inhalt angewendet werden soll [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). Standardwert ist [RevisionTextEffect.STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect/\#STRIKE-THROUGH).

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen geändert werden kann.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
int – Der entsprechende int‑Wert. Der zurückgegebene Wert ist einer der Konstanten von [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/).
### getInsertCellColor() {#getInsertCellColor}
```
public int getInsertCellColor()
```


Ermöglicht die Angabe der für eingefügte Zellen zu verwendenden Farbe [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). Standardwert ist [RevisionColor.BLUE](../../com.aspose.words/revisioncolor/\#BLUE).

 **Examples:** 

Zeigt, wie man mit Einfüge‑/Lösch‑Zell‑Revisionsfarbe arbeitet.

```

 Document doc = new Document(getMyDir() + "Cell revisions.docx");

 doc.getLayoutOptions().getRevisionOptions().setInsertCellColor(RevisionColor.BLUE);
 doc.getLayoutOptions().getRevisionOptions().setDeleteCellColor(RevisionColor.DARK_RED);

 doc.save(getArtifactsDir() + "Revision.RevisionCellColor.pdf");
 
```

**Returns:**
int – Der entsprechende int‑Wert. Der zurückgegebene Wert ist einer der Konstanten von [RevisionColor](../../com.aspose.words/revisioncolor/).
### getInsertedTextColor() {#getInsertedTextColor}
```
public int getInsertedTextColor()
```


Ermöglicht die Angabe der für eingefügten Inhalt zu verwendenden Farbe [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). Standardwert ist [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen in einem gerenderten Ausgabedokument geändert wird.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a revision, then change the color of all revisions to green.
 builder.writeln("This is not a revision.");
 doc.startTrackRevisions("John Doe", new Date());
 builder.writeln("This is a revision.");
 doc.stopTrackRevisions();
 builder.writeln("This is not a revision.");

 // Remove the bar that appears to the left of every revised line.
 doc.getLayoutOptions().getRevisionOptions().setInsertedTextColor(RevisionColor.BRIGHT_GREEN);
 doc.getLayoutOptions().getRevisionOptions().setShowRevisionBars(false);
 doc.getLayoutOptions().getRevisionOptions().setRevisionBarsPosition(HorizontalAlignment.RIGHT);

 doc.save(getArtifactsDir() + "Revision.LayoutOptionsRevisions.pdf");
 
```

**Returns:**
int – Der entsprechende int‑Wert. Der zurückgegebene Wert ist einer der Konstanten von [RevisionColor](../../com.aspose.words/revisioncolor/).
### getInsertedTextEffect() {#getInsertedTextEffect}
```
public int getInsertedTextEffect()
```


Ermöglicht die Angabe des Effekts, der auf eingefügten Inhalt angewendet werden soll [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). Standardwert ist [RevisionTextEffect.UNDERLINE](../../com.aspose.words/revisiontexteffect/\#UNDERLINE).

**Returns:**
int – Der entsprechende int‑Wert. Der zurückgegebene Wert ist einer der Konstanten von [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/).
### getMeasurementUnit() {#getMeasurementUnit}
```
public int getMeasurementUnit()
```


Ermöglicht die Angabe der Maßeinheiten für Revisionskommentare. Standardwert ist [MeasurementUnits.CENTIMETERS](../../com.aspose.words/measurementunits/\#CENTIMETERS).

**Returns:**
int – Der entsprechende int‑Wert. Der zurückgegebene Wert ist einer der Konstanten von [MeasurementUnits](../../com.aspose.words/measurementunits/).
### getMovedFromTextColor() {#getMovedFromTextColor}
```
public int getMovedFromTextColor()
```


Ermöglicht die Angabe der für Bereiche, aus denen Inhalt verschoben wurde, zu verwendenden Farbe [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Standardwert ist [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen geändert werden kann.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
int – Der entsprechende int‑Wert. Der zurückgegebene Wert ist einer der Konstanten von [RevisionColor](../../com.aspose.words/revisioncolor/).
### getMovedFromTextEffect() {#getMovedFromTextEffect}
```
public int getMovedFromTextEffect()
```


Ermöglicht die Angabe des Effekts, der auf die Bereiche angewendet wird, aus denen Inhalt verschoben wurde [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Der Standardwert ist [RevisionTextEffect.DOUBLE\_STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect/\#DOUBLE-STRIKE-THROUGH)

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen geändert werden kann.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
int – Der entsprechende int‑Wert. Der zurückgegebene Wert ist einer der Konstanten von [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/).
### getMovedToTextColor() {#getMovedToTextColor}
```
public int getMovedToTextColor()
```


Ermöglicht die Angabe der Farbe, die für die Bereiche verwendet wird, zu denen Inhalt verschoben wurde [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Der Standardwert ist [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen geändert werden kann.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
int – Der entsprechende int‑Wert. Der zurückgegebene Wert ist einer der Konstanten von [RevisionColor](../../com.aspose.words/revisioncolor/).
### getMovedToTextEffect() {#getMovedToTextEffect}
```
public int getMovedToTextEffect()
```


Ermöglicht die Angabe des Effekts, der auf die Bereiche angewendet wird, zu denen Inhalt verschoben wurde [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Der Standardwert ist [RevisionTextEffect.DOUBLE\_UNDERLINE](../../com.aspose.words/revisiontexteffect/\#DOUBLE-UNDERLINE)

**Returns:**
int – Der entsprechende int‑Wert. Der zurückgegebene Wert ist einer der Konstanten von [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/).
### getRevisedPropertiesColor() {#getRevisedPropertiesColor}
```
public int getRevisedPropertiesColor()
```


Ermöglicht die Angabe der zu verwendenden Farbe für Inhalte mit Änderungen von Formatierungseigenschaften [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE). Der Standardwert ist [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT).

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen geändert werden kann.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
int – Der entsprechende int‑Wert. Der zurückgegebene Wert ist einer der Konstanten von [RevisionColor](../../com.aspose.words/revisioncolor/).
### getRevisedPropertiesEffect() {#getRevisedPropertiesEffect}
```
public int getRevisedPropertiesEffect()
```


Ermöglicht die Angabe des Effekts für Inhaltsbereiche mit Änderungen von Formatierungseigenschaften [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE). Der Standardwert ist [RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect/\#NONE).

**Returns:**
int – Der entsprechende int‑Wert. Der zurückgegebene Wert ist einer der Konstanten von [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/).
### getRevisionBarsColor() {#getRevisionBarsColor}
```
public int getRevisionBarsColor()
```


Ermöglicht die Angabe der Farbe, die für Seitenleisten verwendet wird, die Dokumentzeilen mit überarbeiteten Informationen kennzeichnen. Der Standardwert ist [RevisionColor.RED](../../com.aspose.words/revisioncolor/\#RED).

 **Remarks:** 

Das Setzen dieser Eigenschaft auf die Werte [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR) oder [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT) führt dazu, dass Revisionsbalken im Layout ausgeblendet werden.

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen geändert werden kann.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
int – Der entsprechende int‑Wert. Der zurückgegebene Wert ist einer der Konstanten von [RevisionColor](../../com.aspose.words/revisioncolor/).
### getRevisionBarsPosition() {#getRevisionBarsPosition}
```
public int getRevisionBarsPosition()
```


Ermittelt die Renderposition der Revisionsbalken. Der Standardwert ist [HorizontalAlignment.OUTSIDE](../../com.aspose.words/horizontalalignment/\#OUTSIDE).

**Returns:**
int - Renderposition der Revisionsbalken. Der zurückgegebene Wert ist einer der Konstanten von [HorizontalAlignment](../../com.aspose.words/horizontalalignment/).
### getRevisionBarsWidth() {#getRevisionBarsWidth}
```
public float getRevisionBarsWidth()
```


Ermittelt die Breite der Revisionsbalken in Punkten.

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen geändert werden kann.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
float - Breite der Revisionsbalken, Punkte.
### getShowInBalloons() {#getShowInBalloons}
```
public int getShowInBalloons()
```


Ermöglicht die Angabe, ob die Revisionen in den Ballons dargestellt werden. Der Standardwert ist [ShowInBalloons.NONE](../../com.aspose.words/showinballoons/\#NONE).

 **Remarks:** 

Beachten Sie, dass Revisionen für [CommentDisplayMode.SHOW\_IN\_ANNOTATIONS](../../com.aspose.words/commentdisplaymode/\#SHOW-IN-ANNOTATIONS) nicht in Ballons dargestellt werden.

 **Examples:** 

Zeigt, wie Revisionen in Ballons angezeigt werden.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // By default, text that is a revision has a different color to differentiate it from the other non-revision text.
 // Set a revision option to show more details about each revision in a balloon on the page's right margin.
 doc.getLayoutOptions().getRevisionOptions().setShowInBalloons(ShowInBalloons.FORMAT_AND_DELETE);
 doc.save(getArtifactsDir() + "Revision.ShowRevisionBalloons.pdf");
 
```

Zeigt, wie das Erscheinungsbild von Revisionen geändert werden kann.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
int - Der entsprechende int‑Wert. Der zurückgegebene Wert ist einer der Konstanten von [ShowInBalloons](../../com.aspose.words/showinballoons/).
### getShowOriginalRevision() {#getShowOriginalRevision}
```
public boolean getShowOriginalRevision()
```


Ermöglicht die Angabe, ob der Originaltext anstelle des überarbeiteten angezeigt werden soll. Der Standardwert ist false.

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen geändert werden kann.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getShowRevisionBars() {#getShowRevisionBars}
```
public boolean getShowRevisionBars()
```


Ermöglicht die Angabe, ob Revisionsbalken in der Nähe von Zeilen mit überarbeitetem Inhalt dargestellt werden sollen. Der Standardwert ist true.

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen in einem gerenderten Ausgabedokument geändert wird.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a revision, then change the color of all revisions to green.
 builder.writeln("This is not a revision.");
 doc.startTrackRevisions("John Doe", new Date());
 builder.writeln("This is a revision.");
 doc.stopTrackRevisions();
 builder.writeln("This is not a revision.");

 // Remove the bar that appears to the left of every revised line.
 doc.getLayoutOptions().getRevisionOptions().setInsertedTextColor(RevisionColor.BRIGHT_GREEN);
 doc.getLayoutOptions().getRevisionOptions().setShowRevisionBars(false);
 doc.getLayoutOptions().getRevisionOptions().setRevisionBarsPosition(HorizontalAlignment.RIGHT);

 doc.save(getArtifactsDir() + "Revision.LayoutOptionsRevisions.pdf");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getShowRevisionMarks() {#getShowRevisionMarks}
```
public boolean getShowRevisionMarks()
```


Ermöglicht die Angabe, ob Revisionstext mit spezieller Formatierungsmarkierung gekennzeichnet werden soll. Der Standardwert ist true.

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen geändert werden kann.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### setCommentColor(int value) {#setCommentColor-int}
```
public void setCommentColor(int value)
```


Ermöglicht die Angabe der für Kommentare zu verwendenden Farbe. Standardwert ist [RevisionColor.RED](../../com.aspose.words/revisioncolor/\#RED).

 **Remarks:** 

Wenn diese Eigenschaft auf die Werte [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR) oder [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT) gesetzt wird, wird sie als Ergebnis auf die Standardfarbe zurückgesetzt.

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen geändert werden kann.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende int‑Wert. Der Wert muss einer der Konstanten von [RevisionColor](../../com.aspose.words/revisioncolor/) sein. |

### setDeleteCellColor(int value) {#setDeleteCellColor-int}
```
public void setDeleteCellColor(int value)
```


Ermöglicht die Angabe der für gelöschte Zellen zu verwendenden Farbe [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). Standardwert ist [RevisionColor.PINK](../../com.aspose.words/revisioncolor/\#PINK).

 **Examples:** 

Zeigt, wie man mit Einfüge‑/Lösch‑Zell‑Revisionsfarbe arbeitet.

```

 Document doc = new Document(getMyDir() + "Cell revisions.docx");

 doc.getLayoutOptions().getRevisionOptions().setInsertCellColor(RevisionColor.BLUE);
 doc.getLayoutOptions().getRevisionOptions().setDeleteCellColor(RevisionColor.DARK_RED);

 doc.save(getArtifactsDir() + "Revision.RevisionCellColor.pdf");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende int‑Wert. Der Wert muss einer der Konstanten von [RevisionColor](../../com.aspose.words/revisioncolor/) sein. |

### setDeletedTextColor(int value) {#setDeletedTextColor-int}
```
public void setDeletedTextColor(int value)
```


Ermöglicht die Angabe der für gelöschten Inhalt zu verwendenden Farbe [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). Standardwert ist [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen geändert werden kann.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende int‑Wert. Der Wert muss einer der Konstanten von [RevisionColor](../../com.aspose.words/revisioncolor/) sein. |

### setDeletedTextEffect(int value) {#setDeletedTextEffect-int}
```
public void setDeletedTextEffect(int value)
```


Ermöglicht die Angabe des Effekts, der auf gelöschten Inhalt angewendet werden soll [RevisionType.DELETION](../../com.aspose.words/revisiontype/\#DELETION). Standardwert ist [RevisionTextEffect.STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect/\#STRIKE-THROUGH).

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen geändert werden kann.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende int‑Wert. Der Wert muss einer der Konstanten von [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/) sein. |

### setInsertCellColor(int value) {#setInsertCellColor-int}
```
public void setInsertCellColor(int value)
```


Ermöglicht die Angabe der für eingefügte Zellen zu verwendenden Farbe [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). Standardwert ist [RevisionColor.BLUE](../../com.aspose.words/revisioncolor/\#BLUE).

 **Examples:** 

Zeigt, wie man mit Einfüge‑/Lösch‑Zell‑Revisionsfarbe arbeitet.

```

 Document doc = new Document(getMyDir() + "Cell revisions.docx");

 doc.getLayoutOptions().getRevisionOptions().setInsertCellColor(RevisionColor.BLUE);
 doc.getLayoutOptions().getRevisionOptions().setDeleteCellColor(RevisionColor.DARK_RED);

 doc.save(getArtifactsDir() + "Revision.RevisionCellColor.pdf");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende int‑Wert. Der Wert muss einer der Konstanten von [RevisionColor](../../com.aspose.words/revisioncolor/) sein. |

### setInsertedTextColor(int value) {#setInsertedTextColor-int}
```
public void setInsertedTextColor(int value)
```


Ermöglicht die Angabe der für eingefügten Inhalt zu verwendenden Farbe [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). Standardwert ist [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen in einem gerenderten Ausgabedokument geändert wird.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a revision, then change the color of all revisions to green.
 builder.writeln("This is not a revision.");
 doc.startTrackRevisions("John Doe", new Date());
 builder.writeln("This is a revision.");
 doc.stopTrackRevisions();
 builder.writeln("This is not a revision.");

 // Remove the bar that appears to the left of every revised line.
 doc.getLayoutOptions().getRevisionOptions().setInsertedTextColor(RevisionColor.BRIGHT_GREEN);
 doc.getLayoutOptions().getRevisionOptions().setShowRevisionBars(false);
 doc.getLayoutOptions().getRevisionOptions().setRevisionBarsPosition(HorizontalAlignment.RIGHT);

 doc.save(getArtifactsDir() + "Revision.LayoutOptionsRevisions.pdf");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende int‑Wert. Der Wert muss einer der Konstanten von [RevisionColor](../../com.aspose.words/revisioncolor/) sein. |

### setInsertedTextEffect(int value) {#setInsertedTextEffect-int}
```
public void setInsertedTextEffect(int value)
```


Ermöglicht die Angabe des Effekts, der auf eingefügten Inhalt angewendet werden soll [RevisionType.INSERTION](../../com.aspose.words/revisiontype/\#INSERTION). Standardwert ist [RevisionTextEffect.UNDERLINE](../../com.aspose.words/revisiontexteffect/\#UNDERLINE).

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende int‑Wert. Der Wert muss einer der Konstanten von [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/) sein. |

### setMeasurementUnit(int value) {#setMeasurementUnit-int}
```
public void setMeasurementUnit(int value)
```


Ermöglicht die Angabe der Maßeinheiten für Revisionskommentare. Standardwert ist [MeasurementUnits.CENTIMETERS](../../com.aspose.words/measurementunits/\#CENTIMETERS).

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende int‑Wert. Der Wert muss einer der Konstanten von [MeasurementUnits](../../com.aspose.words/measurementunits/) sein. |

### setMovedFromTextColor(int value) {#setMovedFromTextColor-int}
```
public void setMovedFromTextColor(int value)
```


Ermöglicht die Angabe der für Bereiche, aus denen Inhalt verschoben wurde, zu verwendenden Farbe [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Standardwert ist [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen geändert werden kann.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende int‑Wert. Der Wert muss einer der Konstanten von [RevisionColor](../../com.aspose.words/revisioncolor/) sein. |

### setMovedFromTextEffect(int value) {#setMovedFromTextEffect-int}
```
public void setMovedFromTextEffect(int value)
```


Ermöglicht die Angabe des Effekts, der auf die Bereiche angewendet wird, aus denen Inhalt verschoben wurde [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Der Standardwert ist [RevisionTextEffect.DOUBLE\_STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect/\#DOUBLE-STRIKE-THROUGH)

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen geändert werden kann.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende int‑Wert. Der Wert muss einer der Konstanten von [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/) sein. |

### setMovedToTextColor(int value) {#setMovedToTextColor-int}
```
public void setMovedToTextColor(int value)
```


Ermöglicht die Angabe der Farbe, die für die Bereiche verwendet wird, zu denen Inhalt verschoben wurde [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Der Standardwert ist [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR).

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen geändert werden kann.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende int‑Wert. Der Wert muss einer der Konstanten von [RevisionColor](../../com.aspose.words/revisioncolor/) sein. |

### setMovedToTextEffect(int value) {#setMovedToTextEffect-int}
```
public void setMovedToTextEffect(int value)
```


Ermöglicht die Angabe des Effekts, der auf die Bereiche angewendet wird, zu denen Inhalt verschoben wurde [RevisionType.MOVING](../../com.aspose.words/revisiontype/\#MOVING). Der Standardwert ist [RevisionTextEffect.DOUBLE\_UNDERLINE](../../com.aspose.words/revisiontexteffect/\#DOUBLE-UNDERLINE)

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende int‑Wert. Der Wert muss einer der Konstanten von [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/) sein. |

### setRevisedPropertiesColor(int value) {#setRevisedPropertiesColor-int}
```
public void setRevisedPropertiesColor(int value)
```


Ermöglicht die Angabe der zu verwendenden Farbe für Inhalte mit Änderungen von Formatierungseigenschaften [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE). Der Standardwert ist [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT).

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen geändert werden kann.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende int‑Wert. Der Wert muss einer der Konstanten von [RevisionColor](../../com.aspose.words/revisioncolor/) sein. |

### setRevisedPropertiesEffect(int value) {#setRevisedPropertiesEffect-int}
```
public void setRevisedPropertiesEffect(int value)
```


Ermöglicht die Angabe des Effekts für Inhaltsbereiche mit Änderungen von Formatierungseigenschaften [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype/\#FORMAT-CHANGE). Der Standardwert ist [RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect/\#NONE).

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende int‑Wert. Der Wert muss einer der Konstanten von [RevisionTextEffect](../../com.aspose.words/revisiontexteffect/) sein. |

### setRevisionBarsColor(int value) {#setRevisionBarsColor-int}
```
public void setRevisionBarsColor(int value)
```


Ermöglicht die Angabe der Farbe, die für Seitenleisten verwendet wird, die Dokumentzeilen mit überarbeiteten Informationen kennzeichnen. Der Standardwert ist [RevisionColor.RED](../../com.aspose.words/revisioncolor/\#RED).

 **Remarks:** 

Das Setzen dieser Eigenschaft auf die Werte [RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor/\#BY-AUTHOR) oder [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor/\#NO-HIGHLIGHT) führt dazu, dass Revisionsbalken im Layout ausgeblendet werden.

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen geändert werden kann.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende int‑Wert. Der Wert muss einer der Konstanten von [RevisionColor](../../com.aspose.words/revisioncolor/) sein. |

### setRevisionBarsPosition(int value) {#setRevisionBarsPosition-int}
```
public void setRevisionBarsPosition(int value)
```


Legt die Renderposition der Revisionsbalken fest. Der Standardwert ist [HorizontalAlignment.OUTSIDE](../../com.aspose.words/horizontalalignment/\#OUTSIDE).

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Renderposition der Revisionsbalken. Der Wert muss einer der [HorizontalAlignment](../../com.aspose.words/horizontalalignment/) Konstanten sein. |

### setRevisionBarsWidth(float value) {#setRevisionBarsWidth-float}
```
public void setRevisionBarsWidth(float value)
```


Legt die Breite der Revisionsbalken in Punkten fest.

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen geändert werden kann.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | float | Breite der Revisionsbalken, Punkte. |

### setShowInBalloons(int value) {#setShowInBalloons-int}
```
public void setShowInBalloons(int value)
```


Ermöglicht die Angabe, ob die Revisionen in den Ballons dargestellt werden. Der Standardwert ist [ShowInBalloons.NONE](../../com.aspose.words/showinballoons/\#NONE).

 **Remarks:** 

Beachten Sie, dass Revisionen für [CommentDisplayMode.SHOW\_IN\_ANNOTATIONS](../../com.aspose.words/commentdisplaymode/\#SHOW-IN-ANNOTATIONS) nicht in Ballons dargestellt werden.

 **Examples:** 

Zeigt, wie Revisionen in Ballons angezeigt werden.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // By default, text that is a revision has a different color to differentiate it from the other non-revision text.
 // Set a revision option to show more details about each revision in a balloon on the page's right margin.
 doc.getLayoutOptions().getRevisionOptions().setShowInBalloons(ShowInBalloons.FORMAT_AND_DELETE);
 doc.save(getArtifactsDir() + "Revision.ShowRevisionBalloons.pdf");
 
```

Zeigt, wie das Erscheinungsbild von Revisionen geändert werden kann.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende  int  Wert. Der Wert muss einer der [ShowInBalloons](../../com.aspose.words/showinballoons/) Konstanten sein. |

### setShowOriginalRevision(boolean value) {#setShowOriginalRevision-boolean}
```
public void setShowOriginalRevision(boolean value)
```


Ermöglicht die Angabe, ob der Originaltext anstelle des überarbeiteten angezeigt werden soll. Der Standardwert ist false.

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen geändert werden kann.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setShowRevisionBars(boolean value) {#setShowRevisionBars-boolean}
```
public void setShowRevisionBars(boolean value)
```


Ermöglicht die Angabe, ob Revisionsbalken in der Nähe von Zeilen mit überarbeitetem Inhalt dargestellt werden sollen. Der Standardwert ist true.

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen in einem gerenderten Ausgabedokument geändert wird.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a revision, then change the color of all revisions to green.
 builder.writeln("This is not a revision.");
 doc.startTrackRevisions("John Doe", new Date());
 builder.writeln("This is a revision.");
 doc.stopTrackRevisions();
 builder.writeln("This is not a revision.");

 // Remove the bar that appears to the left of every revised line.
 doc.getLayoutOptions().getRevisionOptions().setInsertedTextColor(RevisionColor.BRIGHT_GREEN);
 doc.getLayoutOptions().getRevisionOptions().setShowRevisionBars(false);
 doc.getLayoutOptions().getRevisionOptions().setRevisionBarsPosition(HorizontalAlignment.RIGHT);

 doc.save(getArtifactsDir() + "Revision.LayoutOptionsRevisions.pdf");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setShowRevisionMarks(boolean value) {#setShowRevisionMarks-boolean}
```
public void setShowRevisionMarks(boolean value)
```


Ermöglicht die Angabe, ob Revisionstext mit spezieller Formatierungsmarkierung gekennzeichnet werden soll. Der Standardwert ist true.

 **Examples:** 

Zeigt, wie das Erscheinungsbild von Revisionen geändert werden kann.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // Get the RevisionOptions object that controls the appearance of revisions.
 RevisionOptions revisionOptions = doc.getLayoutOptions().getRevisionOptions();

 // Render insertion revisions in green and italic.
 revisionOptions.setInsertedTextColor(RevisionColor.GREEN);
 revisionOptions.setInsertedTextEffect(RevisionTextEffect.ITALIC);

 // Render deletion revisions in red and bold.
 revisionOptions.setDeletedTextColor(RevisionColor.RED);
 revisionOptions.setDeletedTextEffect(RevisionTextEffect.BOLD);

 // The same text will appear twice in a movement revision:
 // once at the departure point and once at the arrival destination.
 // Render the text at the moved-from revision yellow with a double strike through
 // and double-underlined blue at the moved-to revision.
 revisionOptions.setMovedFromTextColor(RevisionColor.YELLOW);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_STRIKE_THROUGH);
 revisionOptions.setMovedToTextColor(RevisionColor.CLASSIC_BLUE);
 revisionOptions.setMovedFromTextEffect(RevisionTextEffect.DOUBLE_UNDERLINE);

 // Render format revisions in dark red and bold.
 revisionOptions.setRevisedPropertiesColor(RevisionColor.DARK_RED);
 revisionOptions.setRevisedPropertiesEffect(RevisionTextEffect.BOLD);

 // Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
 revisionOptions.setRevisionBarsColor(RevisionColor.DARK_BLUE);
 revisionOptions.setRevisionBarsWidth(15.0f);

 // Show revision marks and original text.
 revisionOptions.setShowOriginalRevision(true);
 revisionOptions.setShowRevisionMarks(true);

 // Get movement, deletion, formatting revisions, and comments to show up in green balloons
 // on the right side of the page.
 revisionOptions.setShowInBalloons(ShowInBalloons.FORMAT);
 revisionOptions.setCommentColor(RevisionColor.BRIGHT_GREEN);

 // These features are only applicable to formats such as .pdf or .jpg.
 doc.save(getArtifactsDir() + "Revision.RevisionOptions.pdf");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

