---
title: "FrameFormat"
linktitle: "FrameFormat"
second_title: "Aspose.Words für Java"
description: "Stellt die rahmenbezogene Formatierung für einen Absatz in Java dar."
type: docs
weight: 352
url: /de/java/com.aspose.words/frameformat/
---

**Inheritance:**
java.lang.Object
```
public class FrameFormat
```

Stellt die rahmenbezogene Formatierung für einen Absatz dar.

 **Remarks:** 

Dieses Objekt wird immer erstellt. Wenn ein Absatz ein Frame ist, enthalten alle Eigenschaften die jeweiligen Werte, andernfalls werden alle Eigenschaften auf ihre Standardwerte gesetzt.

Verwenden Sie [isFrame()](../../com.aspose.words/frameformat/\#isFrame), um zu prüfen, ob der Absatz ein Frame ist.

 **Examples:** 

Zeigt, wie Informationen zu Formatierungseigenschaften von Absätzen, die Frames sind, abgerufen werden.

```

 Document doc = new Document(getMyDir() + "Paragraph frame.docx");

 Paragraph paragraphFrame = IterableUtils.find(doc.getFirstSection().getBody().getParagraphs(), p -> p.getFrameFormat().isFrame());

 Assert.assertEquals(233.3d, paragraphFrame.getFrameFormat().getWidth());
 Assert.assertEquals(138.8d, paragraphFrame.getFrameFormat().getHeight());
 Assert.assertEquals(HeightRule.AT_LEAST, paragraphFrame.getFrameFormat().getHeightRule());
 Assert.assertEquals(HorizontalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getHorizontalAlignment());
 Assert.assertEquals(VerticalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getVerticalAlignment());
 Assert.assertEquals(34.05d, paragraphFrame.getFrameFormat().getHorizontalPosition());
 Assert.assertEquals(RelativeHorizontalPosition.PAGE, paragraphFrame.getFrameFormat().getRelativeHorizontalPosition());
 Assert.assertEquals(9.0d, paragraphFrame.getFrameFormat().getHorizontalDistanceFromText());
 Assert.assertEquals(20.5d, paragraphFrame.getFrameFormat().getVerticalPosition());
 Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, paragraphFrame.getFrameFormat().getRelativeVerticalPosition());
 Assert.assertEquals(0.0d, paragraphFrame.getFrameFormat().getVerticalDistanceFromText());
 
```
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getHeight()](#getHeight) | Liefert die Höhe des angegebenen Frames. |
| [getHeightRule()](#getHeightRule) | Liefert die Regel zur Bestimmung der Höhe des angegebenen Frames. |
| [getHorizontalAlignment()](#getHorizontalAlignment) | Liefert die horizontale Ausrichtung des angegebenen Frames. |
| [getHorizontalDistanceFromText()](#getHorizontalDistanceFromText) | Liefert den horizontalen Abstand zwischen einem Frame und dem umgebenden Text in Punkten. |
| [getHorizontalPosition()](#getHorizontalPosition) | Liefert den horizontalen Abstand zwischen dem Rand des Frames und dem durch die [getRelativeHorizontalPosition()](../../com.aspose.words/frameformat/\#getRelativeHorizontalPosition)‑Eigenschaft angegebenen Element. |
| [getRelativeHorizontalPosition()](#getRelativeHorizontalPosition) | Liefert die relative horizontale Position eines Frames. |
| [getRelativeVerticalPosition()](#getRelativeVerticalPosition) | Liefert die relative vertikale Position eines Frames. |
| [getVerticalAlignment()](#getVerticalAlignment) | Liefert die vertikale Ausrichtung des angegebenen Frames. |
| [getVerticalDistanceFromText()](#getVerticalDistanceFromText) | Gibt den vertikalen Abstand (in Punkten) zwischen einem Frame und dem umgebenden Text an. |
| [getVerticalPosition()](#getVerticalPosition) | Ermittelt den vertikalen Abstand zwischen dem Rand des Rahmens und dem durch die [getRelativeVerticalPosition()](../../com.aspose.words/frameformat/\#getRelativeVerticalPosition) Eigenschaft angegebenen Element. |
| [getWidth()](#getWidth) | Ermittelt die Breite des angegebenen Rahmens in Punkten. |
| [isFrame()](#isFrame) | Gibt  true  zurück, wenn der Absatz ein Rahmen ist. |
### getHeight() {#getHeight}
```
public double getHeight()
```


Liefert die Höhe des angegebenen Frames.

 **Examples:** 

Zeigt, wie Informationen zu Formatierungseigenschaften von Absätzen, die Frames sind, abgerufen werden.

```

 Document doc = new Document(getMyDir() + "Paragraph frame.docx");

 Paragraph paragraphFrame = IterableUtils.find(doc.getFirstSection().getBody().getParagraphs(), p -> p.getFrameFormat().isFrame());

 Assert.assertEquals(233.3d, paragraphFrame.getFrameFormat().getWidth());
 Assert.assertEquals(138.8d, paragraphFrame.getFrameFormat().getHeight());
 Assert.assertEquals(HeightRule.AT_LEAST, paragraphFrame.getFrameFormat().getHeightRule());
 Assert.assertEquals(HorizontalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getHorizontalAlignment());
 Assert.assertEquals(VerticalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getVerticalAlignment());
 Assert.assertEquals(34.05d, paragraphFrame.getFrameFormat().getHorizontalPosition());
 Assert.assertEquals(RelativeHorizontalPosition.PAGE, paragraphFrame.getFrameFormat().getRelativeHorizontalPosition());
 Assert.assertEquals(9.0d, paragraphFrame.getFrameFormat().getHorizontalDistanceFromText());
 Assert.assertEquals(20.5d, paragraphFrame.getFrameFormat().getVerticalPosition());
 Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, paragraphFrame.getFrameFormat().getRelativeVerticalPosition());
 Assert.assertEquals(0.0d, paragraphFrame.getFrameFormat().getVerticalDistanceFromText());
 
```

**Returns:**
double - Die Höhe des angegebenen Rahmens.
### getHeightRule() {#getHeightRule}
```
public int getHeightRule()
```


Liefert die Regel zur Bestimmung der Höhe des angegebenen Frames.

 **Examples:** 

Zeigt, wie Informationen zu Formatierungseigenschaften von Absätzen, die Frames sind, abgerufen werden.

```

 Document doc = new Document(getMyDir() + "Paragraph frame.docx");

 Paragraph paragraphFrame = IterableUtils.find(doc.getFirstSection().getBody().getParagraphs(), p -> p.getFrameFormat().isFrame());

 Assert.assertEquals(233.3d, paragraphFrame.getFrameFormat().getWidth());
 Assert.assertEquals(138.8d, paragraphFrame.getFrameFormat().getHeight());
 Assert.assertEquals(HeightRule.AT_LEAST, paragraphFrame.getFrameFormat().getHeightRule());
 Assert.assertEquals(HorizontalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getHorizontalAlignment());
 Assert.assertEquals(VerticalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getVerticalAlignment());
 Assert.assertEquals(34.05d, paragraphFrame.getFrameFormat().getHorizontalPosition());
 Assert.assertEquals(RelativeHorizontalPosition.PAGE, paragraphFrame.getFrameFormat().getRelativeHorizontalPosition());
 Assert.assertEquals(9.0d, paragraphFrame.getFrameFormat().getHorizontalDistanceFromText());
 Assert.assertEquals(20.5d, paragraphFrame.getFrameFormat().getVerticalPosition());
 Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, paragraphFrame.getFrameFormat().getRelativeVerticalPosition());
 Assert.assertEquals(0.0d, paragraphFrame.getFrameFormat().getVerticalDistanceFromText());
 
```

**Returns:**
int - Die Regel zur Bestimmung der Höhe des angegebenen Rahmens. Der zurückgegebene Wert ist einer der Konstanten von [HeightRule](../../com.aspose.words/heightrule/).
### getHorizontalAlignment() {#getHorizontalAlignment}
```
public int getHorizontalAlignment()
```


Liefert die horizontale Ausrichtung des angegebenen Frames.

 **Examples:** 

Zeigt, wie Informationen zu Formatierungseigenschaften von Absätzen, die Frames sind, abgerufen werden.

```

 Document doc = new Document(getMyDir() + "Paragraph frame.docx");

 Paragraph paragraphFrame = IterableUtils.find(doc.getFirstSection().getBody().getParagraphs(), p -> p.getFrameFormat().isFrame());

 Assert.assertEquals(233.3d, paragraphFrame.getFrameFormat().getWidth());
 Assert.assertEquals(138.8d, paragraphFrame.getFrameFormat().getHeight());
 Assert.assertEquals(HeightRule.AT_LEAST, paragraphFrame.getFrameFormat().getHeightRule());
 Assert.assertEquals(HorizontalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getHorizontalAlignment());
 Assert.assertEquals(VerticalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getVerticalAlignment());
 Assert.assertEquals(34.05d, paragraphFrame.getFrameFormat().getHorizontalPosition());
 Assert.assertEquals(RelativeHorizontalPosition.PAGE, paragraphFrame.getFrameFormat().getRelativeHorizontalPosition());
 Assert.assertEquals(9.0d, paragraphFrame.getFrameFormat().getHorizontalDistanceFromText());
 Assert.assertEquals(20.5d, paragraphFrame.getFrameFormat().getVerticalPosition());
 Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, paragraphFrame.getFrameFormat().getRelativeVerticalPosition());
 Assert.assertEquals(0.0d, paragraphFrame.getFrameFormat().getVerticalDistanceFromText());
 
```

**Returns:**
int - Horizontale Ausrichtung des angegebenen Rahmens. Der zurückgegebene Wert ist einer der Konstanten von [HorizontalAlignment](../../com.aspose.words/horizontalalignment/).
### getHorizontalDistanceFromText() {#getHorizontalDistanceFromText}
```
public double getHorizontalDistanceFromText()
```


Liefert den horizontalen Abstand zwischen einem Frame und dem umgebenden Text in Punkten.

 **Examples:** 

Zeigt, wie Informationen zu Formatierungseigenschaften von Absätzen, die Frames sind, abgerufen werden.

```

 Document doc = new Document(getMyDir() + "Paragraph frame.docx");

 Paragraph paragraphFrame = IterableUtils.find(doc.getFirstSection().getBody().getParagraphs(), p -> p.getFrameFormat().isFrame());

 Assert.assertEquals(233.3d, paragraphFrame.getFrameFormat().getWidth());
 Assert.assertEquals(138.8d, paragraphFrame.getFrameFormat().getHeight());
 Assert.assertEquals(HeightRule.AT_LEAST, paragraphFrame.getFrameFormat().getHeightRule());
 Assert.assertEquals(HorizontalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getHorizontalAlignment());
 Assert.assertEquals(VerticalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getVerticalAlignment());
 Assert.assertEquals(34.05d, paragraphFrame.getFrameFormat().getHorizontalPosition());
 Assert.assertEquals(RelativeHorizontalPosition.PAGE, paragraphFrame.getFrameFormat().getRelativeHorizontalPosition());
 Assert.assertEquals(9.0d, paragraphFrame.getFrameFormat().getHorizontalDistanceFromText());
 Assert.assertEquals(20.5d, paragraphFrame.getFrameFormat().getVerticalPosition());
 Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, paragraphFrame.getFrameFormat().getRelativeVerticalPosition());
 Assert.assertEquals(0.0d, paragraphFrame.getFrameFormat().getVerticalDistanceFromText());
 
```

**Returns:**
double - Horizontaler Abstand zwischen einem Rahmen und dem umgebenden Text, in Punkten.
### getHorizontalPosition() {#getHorizontalPosition}
```
public double getHorizontalPosition()
```


Liefert den horizontalen Abstand zwischen dem Rand des Frames und dem durch die [getRelativeHorizontalPosition()](../../com.aspose.words/frameformat/\#getRelativeHorizontalPosition)‑Eigenschaft angegebenen Element.

 **Examples:** 

Zeigt, wie Informationen zu Formatierungseigenschaften von Absätzen, die Frames sind, abgerufen werden.

```

 Document doc = new Document(getMyDir() + "Paragraph frame.docx");

 Paragraph paragraphFrame = IterableUtils.find(doc.getFirstSection().getBody().getParagraphs(), p -> p.getFrameFormat().isFrame());

 Assert.assertEquals(233.3d, paragraphFrame.getFrameFormat().getWidth());
 Assert.assertEquals(138.8d, paragraphFrame.getFrameFormat().getHeight());
 Assert.assertEquals(HeightRule.AT_LEAST, paragraphFrame.getFrameFormat().getHeightRule());
 Assert.assertEquals(HorizontalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getHorizontalAlignment());
 Assert.assertEquals(VerticalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getVerticalAlignment());
 Assert.assertEquals(34.05d, paragraphFrame.getFrameFormat().getHorizontalPosition());
 Assert.assertEquals(RelativeHorizontalPosition.PAGE, paragraphFrame.getFrameFormat().getRelativeHorizontalPosition());
 Assert.assertEquals(9.0d, paragraphFrame.getFrameFormat().getHorizontalDistanceFromText());
 Assert.assertEquals(20.5d, paragraphFrame.getFrameFormat().getVerticalPosition());
 Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, paragraphFrame.getFrameFormat().getRelativeVerticalPosition());
 Assert.assertEquals(0.0d, paragraphFrame.getFrameFormat().getVerticalDistanceFromText());
 
```

**Returns:**
double - Horizontaler Abstand zwischen dem Rand des Rahmens und dem durch die [getRelativeHorizontalPosition()](../../com.aspose.words/frameformat/\#getRelativeHorizontalPosition) Eigenschaft angegebenen Element.
### getRelativeHorizontalPosition() {#getRelativeHorizontalPosition}
```
public int getRelativeHorizontalPosition()
```


Liefert die relative horizontale Position eines Frames.

 **Examples:** 

Zeigt, wie Informationen zu Formatierungseigenschaften von Absätzen, die Frames sind, abgerufen werden.

```

 Document doc = new Document(getMyDir() + "Paragraph frame.docx");

 Paragraph paragraphFrame = IterableUtils.find(doc.getFirstSection().getBody().getParagraphs(), p -> p.getFrameFormat().isFrame());

 Assert.assertEquals(233.3d, paragraphFrame.getFrameFormat().getWidth());
 Assert.assertEquals(138.8d, paragraphFrame.getFrameFormat().getHeight());
 Assert.assertEquals(HeightRule.AT_LEAST, paragraphFrame.getFrameFormat().getHeightRule());
 Assert.assertEquals(HorizontalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getHorizontalAlignment());
 Assert.assertEquals(VerticalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getVerticalAlignment());
 Assert.assertEquals(34.05d, paragraphFrame.getFrameFormat().getHorizontalPosition());
 Assert.assertEquals(RelativeHorizontalPosition.PAGE, paragraphFrame.getFrameFormat().getRelativeHorizontalPosition());
 Assert.assertEquals(9.0d, paragraphFrame.getFrameFormat().getHorizontalDistanceFromText());
 Assert.assertEquals(20.5d, paragraphFrame.getFrameFormat().getVerticalPosition());
 Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, paragraphFrame.getFrameFormat().getRelativeVerticalPosition());
 Assert.assertEquals(0.0d, paragraphFrame.getFrameFormat().getVerticalDistanceFromText());
 
```

**Returns:**
int - Die relative horizontale Position eines Rahmens. Der zurückgegebene Wert ist einer der Konstanten von [RelativeHorizontalPosition](../../com.aspose.words/relativehorizontalposition/).
### getRelativeVerticalPosition() {#getRelativeVerticalPosition}
```
public int getRelativeVerticalPosition()
```


Liefert die relative vertikale Position eines Frames.

 **Examples:** 

Zeigt, wie Informationen zu Formatierungseigenschaften von Absätzen, die Frames sind, abgerufen werden.

```

 Document doc = new Document(getMyDir() + "Paragraph frame.docx");

 Paragraph paragraphFrame = IterableUtils.find(doc.getFirstSection().getBody().getParagraphs(), p -> p.getFrameFormat().isFrame());

 Assert.assertEquals(233.3d, paragraphFrame.getFrameFormat().getWidth());
 Assert.assertEquals(138.8d, paragraphFrame.getFrameFormat().getHeight());
 Assert.assertEquals(HeightRule.AT_LEAST, paragraphFrame.getFrameFormat().getHeightRule());
 Assert.assertEquals(HorizontalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getHorizontalAlignment());
 Assert.assertEquals(VerticalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getVerticalAlignment());
 Assert.assertEquals(34.05d, paragraphFrame.getFrameFormat().getHorizontalPosition());
 Assert.assertEquals(RelativeHorizontalPosition.PAGE, paragraphFrame.getFrameFormat().getRelativeHorizontalPosition());
 Assert.assertEquals(9.0d, paragraphFrame.getFrameFormat().getHorizontalDistanceFromText());
 Assert.assertEquals(20.5d, paragraphFrame.getFrameFormat().getVerticalPosition());
 Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, paragraphFrame.getFrameFormat().getRelativeVerticalPosition());
 Assert.assertEquals(0.0d, paragraphFrame.getFrameFormat().getVerticalDistanceFromText());
 
```

**Returns:**
int - Die relative vertikale Position eines Rahmens. Der zurückgegebene Wert ist einer der Konstanten von [RelativeVerticalPosition](../../com.aspose.words/relativeverticalposition/).
### getVerticalAlignment() {#getVerticalAlignment}
```
public int getVerticalAlignment()
```


Liefert die vertikale Ausrichtung des angegebenen Frames.

 **Examples:** 

Zeigt, wie Informationen zu Formatierungseigenschaften von Absätzen, die Frames sind, abgerufen werden.

```

 Document doc = new Document(getMyDir() + "Paragraph frame.docx");

 Paragraph paragraphFrame = IterableUtils.find(doc.getFirstSection().getBody().getParagraphs(), p -> p.getFrameFormat().isFrame());

 Assert.assertEquals(233.3d, paragraphFrame.getFrameFormat().getWidth());
 Assert.assertEquals(138.8d, paragraphFrame.getFrameFormat().getHeight());
 Assert.assertEquals(HeightRule.AT_LEAST, paragraphFrame.getFrameFormat().getHeightRule());
 Assert.assertEquals(HorizontalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getHorizontalAlignment());
 Assert.assertEquals(VerticalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getVerticalAlignment());
 Assert.assertEquals(34.05d, paragraphFrame.getFrameFormat().getHorizontalPosition());
 Assert.assertEquals(RelativeHorizontalPosition.PAGE, paragraphFrame.getFrameFormat().getRelativeHorizontalPosition());
 Assert.assertEquals(9.0d, paragraphFrame.getFrameFormat().getHorizontalDistanceFromText());
 Assert.assertEquals(20.5d, paragraphFrame.getFrameFormat().getVerticalPosition());
 Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, paragraphFrame.getFrameFormat().getRelativeVerticalPosition());
 Assert.assertEquals(0.0d, paragraphFrame.getFrameFormat().getVerticalDistanceFromText());
 
```

**Returns:**
int - Vertikale Ausrichtung des angegebenen Rahmens. Der zurückgegebene Wert ist einer der Konstanten von [VerticalAlignment](../../com.aspose.words/verticalalignment/).
### getVerticalDistanceFromText() {#getVerticalDistanceFromText}
```
public double getVerticalDistanceFromText()
```


Gibt den vertikalen Abstand (in Punkten) zwischen einem Frame und dem umgebenden Text an.

 **Examples:** 

Zeigt, wie Informationen zu Formatierungseigenschaften von Absätzen, die Frames sind, abgerufen werden.

```

 Document doc = new Document(getMyDir() + "Paragraph frame.docx");

 Paragraph paragraphFrame = IterableUtils.find(doc.getFirstSection().getBody().getParagraphs(), p -> p.getFrameFormat().isFrame());

 Assert.assertEquals(233.3d, paragraphFrame.getFrameFormat().getWidth());
 Assert.assertEquals(138.8d, paragraphFrame.getFrameFormat().getHeight());
 Assert.assertEquals(HeightRule.AT_LEAST, paragraphFrame.getFrameFormat().getHeightRule());
 Assert.assertEquals(HorizontalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getHorizontalAlignment());
 Assert.assertEquals(VerticalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getVerticalAlignment());
 Assert.assertEquals(34.05d, paragraphFrame.getFrameFormat().getHorizontalPosition());
 Assert.assertEquals(RelativeHorizontalPosition.PAGE, paragraphFrame.getFrameFormat().getRelativeHorizontalPosition());
 Assert.assertEquals(9.0d, paragraphFrame.getFrameFormat().getHorizontalDistanceFromText());
 Assert.assertEquals(20.5d, paragraphFrame.getFrameFormat().getVerticalPosition());
 Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, paragraphFrame.getFrameFormat().getRelativeVerticalPosition());
 Assert.assertEquals(0.0d, paragraphFrame.getFrameFormat().getVerticalDistanceFromText());
 
```

**Returns:**
double - Der entsprechende  double  Wert.
### getVerticalPosition() {#getVerticalPosition}
```
public double getVerticalPosition()
```


Ermittelt den vertikalen Abstand zwischen dem Rand des Rahmens und dem durch die [getRelativeVerticalPosition()](../../com.aspose.words/frameformat/\#getRelativeVerticalPosition) Eigenschaft angegebenen Element.

 **Examples:** 

Zeigt, wie Informationen zu Formatierungseigenschaften von Absätzen, die Frames sind, abgerufen werden.

```

 Document doc = new Document(getMyDir() + "Paragraph frame.docx");

 Paragraph paragraphFrame = IterableUtils.find(doc.getFirstSection().getBody().getParagraphs(), p -> p.getFrameFormat().isFrame());

 Assert.assertEquals(233.3d, paragraphFrame.getFrameFormat().getWidth());
 Assert.assertEquals(138.8d, paragraphFrame.getFrameFormat().getHeight());
 Assert.assertEquals(HeightRule.AT_LEAST, paragraphFrame.getFrameFormat().getHeightRule());
 Assert.assertEquals(HorizontalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getHorizontalAlignment());
 Assert.assertEquals(VerticalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getVerticalAlignment());
 Assert.assertEquals(34.05d, paragraphFrame.getFrameFormat().getHorizontalPosition());
 Assert.assertEquals(RelativeHorizontalPosition.PAGE, paragraphFrame.getFrameFormat().getRelativeHorizontalPosition());
 Assert.assertEquals(9.0d, paragraphFrame.getFrameFormat().getHorizontalDistanceFromText());
 Assert.assertEquals(20.5d, paragraphFrame.getFrameFormat().getVerticalPosition());
 Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, paragraphFrame.getFrameFormat().getRelativeVerticalPosition());
 Assert.assertEquals(0.0d, paragraphFrame.getFrameFormat().getVerticalDistanceFromText());
 
```

**Returns:**
double - Vertikaler Abstand zwischen dem Rand des Rahmens und dem durch die [getRelativeVerticalPosition()](../../com.aspose.words/frameformat/\#getRelativeVerticalPosition) Eigenschaft angegebenen Element.
### getWidth() {#getWidth}
```
public double getWidth()
```


Ermittelt die Breite des angegebenen Rahmens in Punkten.

 **Examples:** 

Zeigt, wie Informationen zu Formatierungseigenschaften von Absätzen, die Frames sind, abgerufen werden.

```

 Document doc = new Document(getMyDir() + "Paragraph frame.docx");

 Paragraph paragraphFrame = IterableUtils.find(doc.getFirstSection().getBody().getParagraphs(), p -> p.getFrameFormat().isFrame());

 Assert.assertEquals(233.3d, paragraphFrame.getFrameFormat().getWidth());
 Assert.assertEquals(138.8d, paragraphFrame.getFrameFormat().getHeight());
 Assert.assertEquals(HeightRule.AT_LEAST, paragraphFrame.getFrameFormat().getHeightRule());
 Assert.assertEquals(HorizontalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getHorizontalAlignment());
 Assert.assertEquals(VerticalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getVerticalAlignment());
 Assert.assertEquals(34.05d, paragraphFrame.getFrameFormat().getHorizontalPosition());
 Assert.assertEquals(RelativeHorizontalPosition.PAGE, paragraphFrame.getFrameFormat().getRelativeHorizontalPosition());
 Assert.assertEquals(9.0d, paragraphFrame.getFrameFormat().getHorizontalDistanceFromText());
 Assert.assertEquals(20.5d, paragraphFrame.getFrameFormat().getVerticalPosition());
 Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, paragraphFrame.getFrameFormat().getRelativeVerticalPosition());
 Assert.assertEquals(0.0d, paragraphFrame.getFrameFormat().getVerticalDistanceFromText());
 
```

**Returns:**
double - Die Breite des angegebenen Rahmens, in Punkten.
### isFrame() {#isFrame}
```
public boolean isFrame()
```


Gibt  true  zurück, wenn der Absatz ein Rahmen ist.

 **Examples:** 

Zeigt, wie Informationen zu Formatierungseigenschaften von Absätzen, die Frames sind, abgerufen werden.

```

 Document doc = new Document(getMyDir() + "Paragraph frame.docx");

 Paragraph paragraphFrame = IterableUtils.find(doc.getFirstSection().getBody().getParagraphs(), p -> p.getFrameFormat().isFrame());

 Assert.assertEquals(233.3d, paragraphFrame.getFrameFormat().getWidth());
 Assert.assertEquals(138.8d, paragraphFrame.getFrameFormat().getHeight());
 Assert.assertEquals(HeightRule.AT_LEAST, paragraphFrame.getFrameFormat().getHeightRule());
 Assert.assertEquals(HorizontalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getHorizontalAlignment());
 Assert.assertEquals(VerticalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getVerticalAlignment());
 Assert.assertEquals(34.05d, paragraphFrame.getFrameFormat().getHorizontalPosition());
 Assert.assertEquals(RelativeHorizontalPosition.PAGE, paragraphFrame.getFrameFormat().getRelativeHorizontalPosition());
 Assert.assertEquals(9.0d, paragraphFrame.getFrameFormat().getHorizontalDistanceFromText());
 Assert.assertEquals(20.5d, paragraphFrame.getFrameFormat().getVerticalPosition());
 Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, paragraphFrame.getFrameFormat().getRelativeVerticalPosition());
 Assert.assertEquals(0.0d, paragraphFrame.getFrameFormat().getVerticalDistanceFromText());
 
```

**Returns:**
boolean -  true  wenn der Absatz ein Rahmen ist.
