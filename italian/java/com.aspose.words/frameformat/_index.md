---
title: "FrameFormat"
linktitle: "FrameFormat"
second_title: "Aspose.Words per Java"
description: "Rappresenta la formattazione relativa ai frame per un paragrafo in Java."
type: docs
weight: 352
url: /it/java/com.aspose.words/frameformat/
---

**Inheritance:**
java.lang.Object
```
public class FrameFormat
```

Rappresenta la formattazione relativa ai frame per un paragrafo.

 **Remarks:** 

Questo oggetto è sempre creato. Se un paragrafo è un frame, tutte le proprietà conterranno i valori corrispondenti, altrimenti tutte le proprietà sono impostate sui valori predefiniti.

Usa [isFrame()](../../com.aspose.words/frameformat/\#isFrame) per verificare se il paragrafo è un frame.

 **Examples:** 

Mostra come ottenere informazioni sulle proprietà di formattazione dei paragrafi che sono frame.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getHeight()](#getHeight) | Ottiene l'altezza del frame specificato. |
| [getHeightRule()](#getHeightRule) | Ottiene la regola per determinare l'altezza del frame specificato. |
| [getHorizontalAlignment()](#getHorizontalAlignment) | Ottiene l'allineamento orizzontale del frame specificato. |
| [getHorizontalDistanceFromText()](#getHorizontalDistanceFromText) | Ottiene la distanza orizzontale tra un frame e il testo circostante, in punti. |
| [getHorizontalPosition()](#getHorizontalPosition) | Ottiene la distanza orizzontale tra il bordo del frame e l'elemento specificato dalla proprietà [getRelativeHorizontalPosition()](../../com.aspose.words/frameformat/\#getRelativeHorizontalPosition). |
| [getRelativeHorizontalPosition()](#getRelativeHorizontalPosition) | Ottiene la posizione orizzontale relativa di un frame. |
| [getRelativeVerticalPosition()](#getRelativeVerticalPosition) | Ottiene la posizione verticale relativa di un frame. |
| [getVerticalAlignment()](#getVerticalAlignment) | Ottiene l'allineamento verticale del frame specificato. |
| [getVerticalDistanceFromText()](#getVerticalDistanceFromText) | Specifica la distanza verticale (in punti) tra un frame e il testo circostante. |
| [getVerticalPosition()](#getVerticalPosition) | Ottiene la distanza verticale tra il bordo del frame e l'elemento specificato dalla proprietà [getRelativeVerticalPosition()](../../com.aspose.words/frameformat/\#getRelativeVerticalPosition). |
| [getWidth()](#getWidth) | Ottiene la larghezza del frame specificato, in punti. |
| [isFrame()](#isFrame) | Restituisce  true  se il paragrafo è un frame. |
### getHeight() {#getHeight}
```
public double getHeight()
```


Ottiene l'altezza del frame specificato.

 **Examples:** 

Mostra come ottenere informazioni sulle proprietà di formattazione dei paragrafi che sono frame.

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
double - L'altezza del frame specificato.
### getHeightRule() {#getHeightRule}
```
public int getHeightRule()
```


Ottiene la regola per determinare l'altezza del frame specificato.

 **Examples:** 

Mostra come ottenere informazioni sulle proprietà di formattazione dei paragrafi che sono frame.

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
int - La regola per determinare l'altezza del frame specificato. Il valore restituito è una delle costanti [HeightRule](../../com.aspose.words/heightrule/).
### getHorizontalAlignment() {#getHorizontalAlignment}
```
public int getHorizontalAlignment()
```


Ottiene l'allineamento orizzontale del frame specificato.

 **Examples:** 

Mostra come ottenere informazioni sulle proprietà di formattazione dei paragrafi che sono frame.

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
int - Allineamento orizzontale del frame specificato. Il valore restituito è una delle costanti [HorizontalAlignment](../../com.aspose.words/horizontalalignment/).
### getHorizontalDistanceFromText() {#getHorizontalDistanceFromText}
```
public double getHorizontalDistanceFromText()
```


Ottiene la distanza orizzontale tra un frame e il testo circostante, in punti.

 **Examples:** 

Mostra come ottenere informazioni sulle proprietà di formattazione dei paragrafi che sono frame.

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
double - Distanza orizzontale tra un frame e il testo circostante, in punti.
### getHorizontalPosition() {#getHorizontalPosition}
```
public double getHorizontalPosition()
```


Ottiene la distanza orizzontale tra il bordo del frame e l'elemento specificato dalla proprietà [getRelativeHorizontalPosition()](../../com.aspose.words/frameformat/\#getRelativeHorizontalPosition).

 **Examples:** 

Mostra come ottenere informazioni sulle proprietà di formattazione dei paragrafi che sono frame.

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
double - Distanza orizzontale tra il bordo del frame e l'elemento specificato dalla proprietà [getRelativeHorizontalPosition()](../../com.aspose.words/frameformat/\#getRelativeHorizontalPosition).
### getRelativeHorizontalPosition() {#getRelativeHorizontalPosition}
```
public int getRelativeHorizontalPosition()
```


Ottiene la posizione orizzontale relativa di un frame.

 **Examples:** 

Mostra come ottenere informazioni sulle proprietà di formattazione dei paragrafi che sono frame.

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
int - La posizione orizzontale relativa di un frame. Il valore restituito è una delle costanti [RelativeHorizontalPosition](../../com.aspose.words/relativehorizontalposition/).
### getRelativeVerticalPosition() {#getRelativeVerticalPosition}
```
public int getRelativeVerticalPosition()
```


Ottiene la posizione verticale relativa di un frame.

 **Examples:** 

Mostra come ottenere informazioni sulle proprietà di formattazione dei paragrafi che sono frame.

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
int - La posizione verticale relativa di un frame. Il valore restituito è una delle costanti [RelativeVerticalPosition](../../com.aspose.words/relativeverticalposition/).
### getVerticalAlignment() {#getVerticalAlignment}
```
public int getVerticalAlignment()
```


Ottiene l'allineamento verticale del frame specificato.

 **Examples:** 

Mostra come ottenere informazioni sulle proprietà di formattazione dei paragrafi che sono frame.

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
int - Allineamento verticale del frame specificato. Il valore restituito è una delle costanti [VerticalAlignment](../../com.aspose.words/verticalalignment/).
### getVerticalDistanceFromText() {#getVerticalDistanceFromText}
```
public double getVerticalDistanceFromText()
```


Specifica la distanza verticale (in punti) tra un frame e il testo circostante.

 **Examples:** 

Mostra come ottenere informazioni sulle proprietà di formattazione dei paragrafi che sono frame.

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
double - Il valore double corrispondente.
### getVerticalPosition() {#getVerticalPosition}
```
public double getVerticalPosition()
```


Ottiene la distanza verticale tra il bordo del frame e l'elemento specificato dalla proprietà [getRelativeVerticalPosition()](../../com.aspose.words/frameformat/\#getRelativeVerticalPosition).

 **Examples:** 

Mostra come ottenere informazioni sulle proprietà di formattazione dei paragrafi che sono frame.

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
double - Distanza verticale tra il bordo del frame e l'elemento specificato dalla proprietà [getRelativeVerticalPosition()](../../com.aspose.words/frameformat/\#getRelativeVerticalPosition).
### getWidth() {#getWidth}
```
public double getWidth()
```


Ottiene la larghezza del frame specificato, in punti.

 **Examples:** 

Mostra come ottenere informazioni sulle proprietà di formattazione dei paragrafi che sono frame.

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
double - La larghezza del frame specificato, in punti.
### isFrame() {#isFrame}
```
public boolean isFrame()
```


Restituisce  true  se il paragrafo è un frame.

 **Examples:** 

Mostra come ottenere informazioni sulle proprietà di formattazione dei paragrafi che sono frame.

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
boolean -  true  se il paragrafo è un frame.
