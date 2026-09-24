---
title: "FrameFormat"
linktitle: "FrameFormat"
second_title: "Aspose.Words para Java"
description: "Representa el formato relacionado con frames para un párrafo en Java."
type: docs
weight: 352
url: /es/java/com.aspose.words/frameformat/
---

**Inheritance:**
java.lang.Object
```
public class FrameFormat
```

Representa el formato relacionado con marcos para un párrafo.

 **Remarks:** 

Este objeto siempre se crea. Si un párrafo es un frame, entonces todas las propiedades contendrán los valores correspondientes; de lo contrario, todas las propiedades se establecen en sus valores predeterminados.

Utiliza [isFrame()](../../com.aspose.words/frameformat/\#isFrame) para comprobar si el párrafo es un frame.

 **Examples:** 

Muestra cómo obtener información sobre las propiedades de formato de los párrafos que son frames.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [getHeight()](#getHeight) | Obtiene la altura del frame especificado. |
| [getHeightRule()](#getHeightRule) | Obtiene la regla para determinar la altura del frame especificado. |
| [getHorizontalAlignment()](#getHorizontalAlignment) | Obtiene la alineación horizontal del frame especificado. |
| [getHorizontalDistanceFromText()](#getHorizontalDistanceFromText) | Obtiene la distancia horizontal entre un frame y el texto circundante, en puntos. |
| [getHorizontalPosition()](#getHorizontalPosition) | Obtiene la distancia horizontal entre el borde del frame y el elemento especificado por la propiedad [getRelativeHorizontalPosition()](../../com.aspose.words/frameformat/\#getRelativeHorizontalPosition). |
| [getRelativeHorizontalPosition()](#getRelativeHorizontalPosition) | Obtiene la posición horizontal relativa de un frame. |
| [getRelativeVerticalPosition()](#getRelativeVerticalPosition) | Obtiene la posición vertical relativa de un frame. |
| [getVerticalAlignment()](#getVerticalAlignment) | Obtiene la alineación vertical del frame especificado. |
| [getVerticalDistanceFromText()](#getVerticalDistanceFromText) | Especifica la distancia vertical (en puntos) entre un frame y el texto circundante. |
| [getVerticalPosition()](#getVerticalPosition) | Obtiene la distancia vertical entre el borde del frame y el elemento especificado por la propiedad [getRelativeVerticalPosition()](../../com.aspose.words/frameformat/\#getRelativeVerticalPosition). |
| [getWidth()](#getWidth) | Obtiene el ancho del frame especificado, en puntos. |
| [isFrame()](#isFrame) | Devuelve  true  si el párrafo es un frame. |
### getHeight() {#getHeight}
```
public double getHeight()
```


Obtiene la altura del frame especificado.

 **Examples:** 

Muestra cómo obtener información sobre las propiedades de formato de los párrafos que son frames.

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
double - La altura del frame especificado.
### getHeightRule() {#getHeightRule}
```
public int getHeightRule()
```


Obtiene la regla para determinar la altura del frame especificado.

 **Examples:** 

Muestra cómo obtener información sobre las propiedades de formato de los párrafos que son frames.

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
int - La regla para determinar la altura del frame especificado. El valor devuelto es una de las constantes [HeightRule](../../com.aspose.words/heightrule/).
### getHorizontalAlignment() {#getHorizontalAlignment}
```
public int getHorizontalAlignment()
```


Obtiene la alineación horizontal del frame especificado.

 **Examples:** 

Muestra cómo obtener información sobre las propiedades de formato de los párrafos que son frames.

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
int - Alineación horizontal del frame especificado. El valor devuelto es una de las constantes [HorizontalAlignment](../../com.aspose.words/horizontalalignment/).
### getHorizontalDistanceFromText() {#getHorizontalDistanceFromText}
```
public double getHorizontalDistanceFromText()
```


Obtiene la distancia horizontal entre un frame y el texto circundante, en puntos.

 **Examples:** 

Muestra cómo obtener información sobre las propiedades de formato de los párrafos que son frames.

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
double - Distancia horizontal entre un marco y el texto circundante, en puntos.
### getHorizontalPosition() {#getHorizontalPosition}
```
public double getHorizontalPosition()
```


Obtiene la distancia horizontal entre el borde del frame y el elemento especificado por la propiedad [getRelativeHorizontalPosition()](../../com.aspose.words/frameformat/\#getRelativeHorizontalPosition).

 **Examples:** 

Muestra cómo obtener información sobre las propiedades de formato de los párrafos que son frames.

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
double - Distancia horizontal entre el borde del marco y el elemento especificado por la propiedad [getRelativeHorizontalPosition()](../../com.aspose.words/frameformat/\#getRelativeHorizontalPosition).
### getRelativeHorizontalPosition() {#getRelativeHorizontalPosition}
```
public int getRelativeHorizontalPosition()
```


Obtiene la posición horizontal relativa de un frame.

 **Examples:** 

Muestra cómo obtener información sobre las propiedades de formato de los párrafos que son frames.

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
int - La posición horizontal relativa de un marco. El valor devuelto es una de las constantes [RelativeHorizontalPosition](../../com.aspose.words/relativehorizontalposition/).
### getRelativeVerticalPosition() {#getRelativeVerticalPosition}
```
public int getRelativeVerticalPosition()
```


Obtiene la posición vertical relativa de un frame.

 **Examples:** 

Muestra cómo obtener información sobre las propiedades de formato de los párrafos que son frames.

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
int - La posición vertical relativa de un marco. El valor devuelto es una de las constantes [RelativeVerticalPosition](../../com.aspose.words/relativeverticalposition/).
### getVerticalAlignment() {#getVerticalAlignment}
```
public int getVerticalAlignment()
```


Obtiene la alineación vertical del frame especificado.

 **Examples:** 

Muestra cómo obtener información sobre las propiedades de formato de los párrafos que son frames.

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
int - Alineación vertical del marco especificado. El valor devuelto es una de las constantes [VerticalAlignment](../../com.aspose.words/verticalalignment/).
### getVerticalDistanceFromText() {#getVerticalDistanceFromText}
```
public double getVerticalDistanceFromText()
```


Especifica la distancia vertical (en puntos) entre un frame y el texto circundante.

 **Examples:** 

Muestra cómo obtener información sobre las propiedades de formato de los párrafos que son frames.

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
double - El valor  double  correspondiente.
### getVerticalPosition() {#getVerticalPosition}
```
public double getVerticalPosition()
```


Obtiene la distancia vertical entre el borde del frame y el elemento especificado por la propiedad [getRelativeVerticalPosition()](../../com.aspose.words/frameformat/\#getRelativeVerticalPosition).

 **Examples:** 

Muestra cómo obtener información sobre las propiedades de formato de los párrafos que son frames.

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
double - Distancia vertical entre el borde del marco y el elemento especificado por la propiedad [getRelativeVerticalPosition()](../../com.aspose.words/frameformat/\#getRelativeVerticalPosition).
### getWidth() {#getWidth}
```
public double getWidth()
```


Obtiene el ancho del frame especificado, en puntos.

 **Examples:** 

Muestra cómo obtener información sobre las propiedades de formato de los párrafos que son frames.

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
double - El ancho del marco especificado, en puntos.
### isFrame() {#isFrame}
```
public boolean isFrame()
```


Devuelve  true  si el párrafo es un frame.

 **Examples:** 

Muestra cómo obtener información sobre las propiedades de formato de los párrafos que son frames.

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
boolean -  true  si el párrafo es un marco.
