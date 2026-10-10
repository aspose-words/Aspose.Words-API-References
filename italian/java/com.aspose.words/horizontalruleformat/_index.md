---
title: "HorizontalRuleFormat"
linktitle: "HorizontalRuleFormat"
second_title: "Aspose.Words per Java"
description: "Rappresenta la formattazione della linea orizzontale in Java."
type: docs
weight: 376
url: /it/java/com.aspose.words/horizontalruleformat/
---

**Inheritance:**
java.lang.Object
```
public class HorizontalRuleFormat
```

Rappresenta la formattazione della regola orizzontale.

Per saperne di più, visita l'articolo di documentazione [ Working with Shapes ][Working with Shapes].

 **Examples:** 

Mostra come inserire una forma di regola orizzontale e personalizzare la sua formattazione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```


[Working with Shapes]: https://docs.aspose.com/words/java/working-with-shapes/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getAlignment()](#getAlignment) | Restituisce l'allineamento della linea orizzontale. |
| [getColor()](#getColor) | Restituisce il colore del pennello che riempie la linea orizzontale. |
| [getHeight()](#getHeight) | Restituisce l'altezza della linea orizzontale. |
| [getNoShade()](#getNoShade) | Indica la presenza di ombreggiatura 3D per la linea orizzontale. |
| [getWidthPercent()](#getWidthPercent) | Restituisce la lunghezza della linea orizzontale specificata espressa come percentuale della larghezza della finestra. |
| [setAlignment(int value)](#setAlignment-int) | Imposta l'allineamento della linea orizzontale. |
| [setColor(Color value)](#setColor-java.awt.Color) | Imposta il colore del pennello che riempie la linea orizzontale. |
| [setHeight(double value)](#setHeight-double) | Imposta l'altezza della linea orizzontale. |
| [setNoShade(boolean value)](#setNoShade-boolean) | Indica la presenza di ombreggiatura 3D per la linea orizzontale. |
| [setWidthPercent(double value)](#setWidthPercent-double) | Imposta la lunghezza della linea orizzontale specificata espressa come percentuale della larghezza della finestra. |
### getAlignment() {#getAlignment}
```
public int getAlignment()
```


Restituisce l'allineamento della linea orizzontale.

 **Remarks:** 

Il valore predefinito è [HorizontalRuleAlignment.LEFT](../../com.aspose.words/horizontalrulealignment/\#LEFT).

 **Examples:** 

Mostra come inserire una forma di regola orizzontale e personalizzare la sua formattazione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Returns:**
int - L'allineamento della linea orizzontale. Il valore restituito è uno dei costanti [HorizontalRuleAlignment](../../com.aspose.words/horizontalrulealignment/).
### getColor() {#getColor}
```
public Color getColor()
```


Restituisce il colore del pennello che riempie la linea orizzontale.

 **Remarks:** 

Questo è un collegamento rapido alla proprietà [Fill.getColor()](../../com.aspose.words/fill/\#getColor) / [Fill.setColor(java.awt.Color)](../../com.aspose.words/fill/\#setColor-java.awt.Color).

Il valore predefinito è java.awt.Color\#getGray().getGray().

 **Examples:** 

Mostra come inserire una forma di regola orizzontale e personalizzare la sua formattazione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Returns:**
java.awt.Color - Il colore del pennello che riempie la linea orizzontale.
### getHeight() {#getHeight}
```
public double getHeight()
```


Restituisce l'altezza della linea orizzontale.

**Returns:**
double - L'altezza della linea orizzontale.
### getNoShade() {#getNoShade}
```
public boolean getNoShade()
```


Indica la presenza di ombreggiatura 3D per la linea orizzontale. Se  true , allora la linea orizzontale è senza ombreggiatura 3D e viene usato un colore solido.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come inserire una forma di regola orizzontale e personalizzare la sua formattazione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getWidthPercent() {#getWidthPercent}
```
public double getWidthPercent()
```


Restituisce la lunghezza della linea orizzontale specificata espressa come percentuale della larghezza della finestra.

**Returns:**
double - La lunghezza della linea orizzontale specificata espressa come percentuale della larghezza della finestra.
### setAlignment(int value) {#setAlignment-int}
```
public void setAlignment(int value)
```


Imposta l'allineamento della linea orizzontale.

 **Remarks:** 

Il valore predefinito è [HorizontalRuleAlignment.LEFT](../../com.aspose.words/horizontalrulealignment/\#LEFT).

 **Examples:** 

Mostra come inserire una forma di regola orizzontale e personalizzare la sua formattazione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | L'allineamento della regola orizzontale. Il valore deve essere uno dei costanti di [HorizontalRuleAlignment](../../com.aspose.words/horizontalrulealignment/). |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Imposta il colore del pennello che riempie la linea orizzontale.

 **Remarks:** 

Questo è un collegamento rapido alla proprietà [Fill.getColor()](../../com.aspose.words/fill/\#getColor) / [Fill.setColor(java.awt.Color)](../../com.aspose.words/fill/\#setColor-java.awt.Color).

Il valore predefinito è java.awt.Color\#getGray().getGray().

 **Examples:** 

Mostra come inserire una forma di regola orizzontale e personalizzare la sua formattazione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.awt.Color | Il colore del pennello che riempie la regola orizzontale. |

### setHeight(double value) {#setHeight-double}
```
public void setHeight(double value)
```


Imposta l'altezza della linea orizzontale.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | L'altezza della regola orizzontale. |

### setNoShade(boolean value) {#setNoShade-boolean}
```
public void setNoShade(boolean value)
```


Indica la presenza di ombreggiatura 3D per la linea orizzontale. Se  true , allora la linea orizzontale è senza ombreggiatura 3D e viene usato un colore solido.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come inserire una forma di regola orizzontale e personalizzare la sua formattazione.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setWidthPercent(double value) {#setWidthPercent-double}
```
public void setWidthPercent(double value)
```


Imposta la lunghezza della linea orizzontale specificata espressa come percentuale della larghezza della finestra.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | double | La lunghezza della regola orizzontale specificata espressa come percentuale della larghezza della finestra. |

