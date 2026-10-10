---
title: "HyphenationOptions"
linktitle: "HyphenationOptions"
second_title: "Aspose.Words para Java"
description: "Permite configurar las opciones de hifenación del documento en Java."
type: docs
weight: 388
url: /es/java/com.aspose.words/hyphenationoptions/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class HyphenationOptions implements Cloneable
```

Permite configurar las opciones de guionado del documento.

Para obtener más información, visite el artículo de documentación [ Working with Hyphenation ][Working with Hyphenation].

 **Examples:** 

Muestra cómo configurar la hifenación automática.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```


[Working with Hyphenation]: https://docs.aspose.com/words/java/working-with-hyphenation/
## Métodos

| Método | Descripción |
| --- | --- |
| [getAutoHyphenation()](#getAutoHyphenation) | Obtiene el valor que determina si la hifenación automática está activada para el documento. |
| [getConsecutiveHyphenLimit()](#getConsecutiveHyphenLimit) | Obtiene el número máximo de líneas consecutivas que pueden terminar con guiones. |
| [getHyphenateCaps()](#getHyphenateCaps) | Obtiene el valor que determina si las palabras escritas en mayúsculas se dividen con guiones. |
| [getHyphenationZone()](#getHyphenationZone) | Obtiene la distancia en 1/20 de punto desde el margen derecho dentro de la cual no desea dividir palabras con guiones. |
| [setAutoHyphenation(boolean value)](#setAutoHyphenation-boolean) | Establece el valor que determina si la hyphenación automática está activada para el documento. |
| [setConsecutiveHyphenLimit(int value)](#setConsecutiveHyphenLimit-int) | Establece el número máximo de líneas consecutivas que pueden terminar con guiones. |
| [setHyphenateCaps(boolean value)](#setHyphenateCaps-boolean) | Establece el valor que determina si las palabras escritas en mayúsculas se dividen con guiones. |
| [setHyphenationZone(int value)](#setHyphenationZone-int) | Establece la distancia en 1/20 de punto desde el margen derecho dentro de la cual no desea dividir palabras con guiones. |
### getAutoHyphenation() {#getAutoHyphenation}
```
public boolean getAutoHyphenation()
```


Obtiene el valor que determina si la hyphenación automática está activada para el documento. El valor predeterminado para esta propiedad es false.

 **Examples:** 

Muestra cómo configurar la hifenación automática.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
boolean - Valor que determina si la hyphenación automática está activada para el documento.
### getConsecutiveHyphenLimit() {#getConsecutiveHyphenLimit}
```
public int getConsecutiveHyphenLimit()
```


Obtiene el número máximo de líneas consecutivas que pueden terminar con guiones. El valor predeterminado para esta propiedad es 0.

 **Remarks:** 

Si el valor de esta propiedad se establece en 0, cualquier número de líneas consecutivas puede terminar con guiones.

La propiedad no tiene efecto al guardar en formatos de página fija, p. ej., PDF.

 **Examples:** 

Muestra cómo configurar la hifenación automática.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
int - El número máximo de líneas consecutivas que pueden terminar con guiones.
### getHyphenateCaps() {#getHyphenateCaps}
```
public boolean getHyphenateCaps()
```


Obtiene el valor que determina si las palabras escritas en mayúsculas se dividen con guiones. El valor predeterminado para esta propiedad es true.

 **Examples:** 

Muestra cómo configurar la hifenación automática.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
boolean - Valor que determina si las palabras escritas en mayúsculas se dividen con guiones.
### getHyphenationZone() {#getHyphenationZone}
```
public int getHyphenationZone()
```


Obtiene la distancia en 1/20 de punto desde el margen derecho dentro de la cual no desea dividir palabras con guiones. El valor predeterminado para esta propiedad es 360 (0.25 pulgada).

 **Examples:** 

Muestra cómo configurar la hifenación automática.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
int - La distancia en 1/20 de punto desde el margen derecho dentro de la cual no desea dividir palabras con guiones.
### setAutoHyphenation(boolean value) {#setAutoHyphenation-boolean}
```
public void setAutoHyphenation(boolean value)
```


Establece el valor que determina si la hyphenación automática está activada para el documento. El valor predeterminado para esta propiedad es false.

 **Examples:** 

Muestra cómo configurar la hifenación automática.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Valor que determina si la hyphenación automática está activada para el documento. |

### setConsecutiveHyphenLimit(int value) {#setConsecutiveHyphenLimit-int}
```
public void setConsecutiveHyphenLimit(int value)
```


Establece el número máximo de líneas consecutivas que pueden terminar con guiones. El valor predeterminado para esta propiedad es 0.

 **Remarks:** 

Si el valor de esta propiedad se establece en 0, cualquier número de líneas consecutivas puede terminar con guiones.

La propiedad no tiene efecto al guardar en formatos de página fija, p. ej., PDF.

 **Examples:** 

Muestra cómo configurar la hifenación automática.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El número máximo de líneas consecutivas que pueden terminar con guiones. |

### setHyphenateCaps(boolean value) {#setHyphenateCaps-boolean}
```
public void setHyphenateCaps(boolean value)
```


Establece el valor que determina si las palabras escritas en mayúsculas se dividen con guiones. El valor predeterminado para esta propiedad es true.

 **Examples:** 

Muestra cómo configurar la hifenación automática.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Valor que determina si las palabras escritas en mayúsculas se dividen con guiones. |

### setHyphenationZone(int value) {#setHyphenationZone-int}
```
public void setHyphenationZone(int value)
```


Establece la distancia en 1/20 de punto desde el margen derecho dentro de la cual no desea dividir palabras con guiones. El valor predeterminado para esta propiedad es 360 (0.25 pulgada).

 **Examples:** 

Muestra cómo configurar la hifenación automática.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | La distancia en 1/20 de punto desde el margen derecho dentro de la cual no desea dividir palabras con guiones. |

