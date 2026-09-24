---
title: "FontInfoCollection"
linktitle: "FontInfoCollection"
second_title: "Aspose.Words para Java"
description: "Representa una colección de fuentes utilizadas en un documento en Java."
type: docs
weight: 327
url: /es/java/com.aspose.words/fontinfocollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class FontInfoCollection implements Iterable
```

Representa una colección de fuentes utilizadas en un documento.

Para obtener más información, visite el artículo de documentación [ Working with Fonts ][Working with Fonts].

 **Remarks:** 

Los elementos son objetos [FontInfo](../../com.aspose.words/fontinfo/).

No crea instancias de esta clase directamente. Use la propiedad [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos) para acceder a la colección de fuentes definidas en el documento.

 **Examples:** 

Muestra cómo imprimir los detalles de las fuentes presentes en un documento.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 FontInfoCollection allFonts = doc.getFontInfos();
 // Print all the used and unused fonts in the document.
 for (int i = 0; i < allFonts.getCount(); i++) {
     System.out.println("Font index #{i}");
     System.out.println("\tName: {allFonts[i].Name}");
 }
 
```

Muestra cómo guardar un documento con fuentes TrueType incrustadas.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Métodos

| Método | Descripción |
| --- | --- |
| [contains(String name)](#contains-java.lang.String) | Determina si la colección contiene una fuente con el nombre especificado. |
| [get(int index)](#get-int) | Obtiene una fuente en el índice especificado. |
| [get(String name)](#get-java.lang.String) | Proporciona acceso a los elementos de la colección. |
| [getCount()](#getCount) | Obtiene el número de elementos contenidos en la colección. |
| [getEmbedSystemFonts()](#getEmbedSystemFonts) | Especifica si se deben incrustar fuentes del Sistema en el documento. |
| [getEmbedTrueTypeFonts()](#getEmbedTrueTypeFonts) | Especifica si se deben incrustar fuentes TrueType en un documento al guardarlo. |
| [getSaveSubsetFonts()](#getSaveSubsetFonts) | Especifica si se debe guardar un subconjunto de las fuentes TrueType incrustadas con el documento. |
| [iterator()](#iterator) | Devuelve un objeto iterador que puede usarse para iterar sobre todos los elementos de la colección. |
| [setEmbedSystemFonts(boolean value)](#setEmbedSystemFonts-boolean) | Especifica si se deben incrustar fuentes del Sistema en el documento. |
| [setEmbedTrueTypeFonts(boolean value)](#setEmbedTrueTypeFonts-boolean) | Especifica si se deben incrustar fuentes TrueType en un documento al guardarlo. |
| [setSaveSubsetFonts(boolean value)](#setSaveSubsetFonts-boolean) | Especifica si se debe guardar un subconjunto de las fuentes TrueType incrustadas con el documento. |
### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Determina si la colección contiene una fuente con el nombre especificado.

 **Examples:** 

Muestra información sobre las fuentes que están presentes en el documento en blanco.

```

 Document doc = new Document();

 // A blank document contains 3 default fonts. Each font in the document
 // will have a corresponding FontInfo object which contains details about that font.
 Assert.assertEquals(3, doc.getFontInfos().getCount());

 Assert.assertTrue(doc.getFontInfos().contains("Times New Roman"));
 Assert.assertEquals(204, doc.getFontInfos().get("Times New Roman").getCharset());

 Assert.assertTrue(doc.getFontInfos().contains("Symbol"));
 Assert.assertTrue(doc.getFontInfos().contains("Arial"));
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | Nombre de la fuente a localizar, sin distinguir mayúsculas y minúsculas. |

**Returns:**
boolean -  true  si el elemento se encuentra en la colección; de lo contrario,  false .
### get(int index) {#get-int}
```
public FontInfo get(int index)
```


Obtiene una fuente en el índice especificado.

 **Examples:** 

Muestra cómo extraer una fuente incrustada de un documento y guardarla en el sistema de archivos local.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 FontInfo embeddedFont = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift");
 byte[] embeddedFontBytes = embeddedFont.getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR);
 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.ttf"), embeddedFontBytes);

 // Embedded font formats may be different in other formats such as .doc.
 // We need to know the correct format before we can extract the font.
 doc = new Document(getMyDir() + "Embedded font.doc");

 Assert.assertNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR));
 Assert.assertNotNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.EMBEDDED_OPEN_TYPE, EmbeddedFontStyle.REGULAR));

 // Also, we can convert embedded OpenType format, which comes from .doc documents, to OpenType.
 embeddedFontBytes = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFontAsOpenType(EmbeddedFontStyle.REGULAR);

 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.otf"), embeddedFontBytes);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | Índice basado en cero de la fuente. |

**Returns:**
[FontInfo](../../com.aspose.words/fontinfo/) - A font at the specified index.
### get(String name) {#get-java.lang.String}
```
public FontInfo get(String name)
```


Proporciona acceso a los elementos de la colección. Obtiene una fuente con el nombre especificado.

 **Examples:** 

Muestra cómo extraer una fuente incrustada de un documento y guardarla en el sistema de archivos local.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 FontInfo embeddedFont = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift");
 byte[] embeddedFontBytes = embeddedFont.getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR);
 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.ttf"), embeddedFontBytes);

 // Embedded font formats may be different in other formats such as .doc.
 // We need to know the correct format before we can extract the font.
 doc = new Document(getMyDir() + "Embedded font.doc");

 Assert.assertNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.OPEN_TYPE, EmbeddedFontStyle.REGULAR));
 Assert.assertNotNull(doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFont(EmbeddedFontFormat.EMBEDDED_OPEN_TYPE, EmbeddedFontStyle.REGULAR));

 // Also, we can convert embedded OpenType format, which comes from .doc documents, to OpenType.
 embeddedFontBytes = doc.getFontInfos().get("Alte DIN 1451 Mittelschrift").getEmbeddedFontAsOpenType(EmbeddedFontStyle.REGULAR);

 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "Alte DIN 1451 Mittelschrift.otf"), embeddedFontBytes);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | Nombre de la fuente a localizar, sin distinguir mayúsculas y minúsculas. |

**Returns:**
[FontInfo](../../com.aspose.words/fontinfo/) - The corresponding [FontInfo](../../com.aspose.words/fontinfo/) value.
### getCount() {#getCount}
```
public int getCount()
```


Obtiene el número de elementos contenidos en la colección.

 **Examples:** 

Muestra información sobre las fuentes que están presentes en el documento en blanco.

```

 Document doc = new Document();

 // A blank document contains 3 default fonts. Each font in the document
 // will have a corresponding FontInfo object which contains details about that font.
 Assert.assertEquals(3, doc.getFontInfos().getCount());

 Assert.assertTrue(doc.getFontInfos().contains("Times New Roman"));
 Assert.assertEquals(204, doc.getFontInfos().get("Times New Roman").getCharset());

 Assert.assertTrue(doc.getFontInfos().contains("Symbol"));
 Assert.assertTrue(doc.getFontInfos().contains("Arial"));
 
```

**Returns:**
int - El número de elementos contenidos en la colección.
### getEmbedSystemFonts() {#getEmbedSystemFonts}
```
public boolean getEmbedSystemFonts()
```


Especifica si se deben incrustar fuentes del Sistema en el documento. El valor predeterminado de esta propiedad es false.

Esta opción funciona solo cuando la opción [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) está establecida en true.

 **Remarks:** 

Establecer esta propiedad en true es útil si el usuario está en un sistema de Asia Oriental y desea crear un documento que sea legible para otros que no tengan fuentes para ese idioma en su sistema. Por ejemplo, un usuario en un sistema japonés podría optar por incrustar las fuentes en un documento para que el documento japonés sea legible en todos los sistemas.

Esta opción funciona solo para los formatos DOC, DOCX y RTF.

 **Examples:** 

Muestra cómo guardar un documento con fuentes TrueType incrustadas.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getEmbedTrueTypeFonts() {#getEmbedTrueTypeFonts}
```
public boolean getEmbedTrueTypeFonts()
```


Especifica si se deben incrustar fuentes TrueType en un documento al guardarlo. El valor predeterminado de esta propiedad es false.

 **Remarks:** 

Incrustar fuentes TrueType permite a otros ver el documento con las mismas fuentes que se usaron para crearlo, pero puede aumentar sustancialmente el tamaño del documento.

Esta opción funciona solo para los formatos DOC, DOCX y RTF.

 **Examples:** 

Muestra cómo guardar un documento con fuentes TrueType incrustadas.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getSaveSubsetFonts() {#getSaveSubsetFonts}
```
public boolean getSaveSubsetFonts()
```


Especifica si se debe guardar un subconjunto de las fuentes TrueType incrustadas con el documento. El valor predeterminado de esta propiedad es false.

Esta opción funciona solo cuando la propiedad [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) está establecida en true.

 **Remarks:** 

Esta opción funciona solo para los formatos DOC, DOCX y RTF.

 **Examples:** 

Muestra cómo guardar un documento con fuentes TrueType incrustadas.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### iterator() {#iterator}
```
public Iterator iterator()
```


Devuelve un objeto iterador que puede usarse para iterar sobre todos los elementos de la colección.

 **Examples:** 

Muestra cómo acceder e imprimir los detalles de cada fuente en un documento.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 Iterator fontCollectionEnumerator = doc.getFontInfos().iterator();
 while (fontCollectionEnumerator.hasNext()) {
     FontInfo fontInfo = fontCollectionEnumerator.next();
     if (fontInfo != null) {
         System.out.println("Font name: " + fontInfo.getName());

         // Alt names are usually blank.
         System.out.println("Alt name: " + fontInfo.getAltName());
         System.out.println("\t- Family: " + fontInfo.getFamily());
         System.out.println("\t- " + (fontInfo.isTrueType() ? "Is TrueType" : "Is not TrueType"));
         System.out.println("\t- Pitch: " + fontInfo.getPitch());
         System.out.println("\t- Charset: " + fontInfo.getCharset());
         System.out.println("\t- Panose:");
         System.out.println("\t\tFamily Kind: " + (fontInfo.getPanose()[0] & 0xFF));
         System.out.println("\t\tSerif Style: " + (fontInfo.getPanose()[1] & 0xFF));
         System.out.println("\t\tWeight: " + (fontInfo.getPanose()[2] & 0xFF));
         System.out.println("\t\tProportion: " + (fontInfo.getPanose()[3] & 0xFF));
         System.out.println("\t\tContrast: " + (fontInfo.getPanose()[4] & 0xFF));
         System.out.println("\t\tStroke Variation: " + (fontInfo.getPanose()[5] & 0xFF));
         System.out.println("\t\tArm Style: " + (fontInfo.getPanose()[6] & 0xFF));
         System.out.println("\t\tLetterform: " + (fontInfo.getPanose()[7] & 0xFF));
         System.out.println("\t\tMidline: " + (fontInfo.getPanose()[8] & 0xFF));
         System.out.println("\t\tX-Height: " + (fontInfo.getPanose()[9] & 0xFF));
     }
 }
 
```

**Returns:**
java.util.Iterator
### setEmbedSystemFonts(boolean value) {#setEmbedSystemFonts-boolean}
```
public void setEmbedSystemFonts(boolean value)
```


Especifica si se deben incrustar fuentes del Sistema en el documento. El valor predeterminado de esta propiedad es false.

Esta opción funciona solo cuando la opción [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) está establecida en true.

 **Remarks:** 

Establecer esta propiedad en true es útil si el usuario está en un sistema de Asia Oriental y desea crear un documento que sea legible para otros que no tengan fuentes para ese idioma en su sistema. Por ejemplo, un usuario en un sistema japonés podría optar por incrustar las fuentes en un documento para que el documento japonés sea legible en todos los sistemas.

Esta opción funciona solo para los formatos DOC, DOCX y RTF.

 **Examples:** 

Muestra cómo guardar un documento con fuentes TrueType incrustadas.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setEmbedTrueTypeFonts(boolean value) {#setEmbedTrueTypeFonts-boolean}
```
public void setEmbedTrueTypeFonts(boolean value)
```


Especifica si se deben incrustar fuentes TrueType en un documento al guardarlo. El valor predeterminado de esta propiedad es false.

 **Remarks:** 

Incrustar fuentes TrueType permite a otros ver el documento con las mismas fuentes que se usaron para crearlo, pero puede aumentar sustancialmente el tamaño del documento.

Esta opción funciona solo para los formatos DOC, DOCX y RTF.

 **Examples:** 

Muestra cómo guardar un documento con fuentes TrueType incrustadas.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setSaveSubsetFonts(boolean value) {#setSaveSubsetFonts-boolean}
```
public void setSaveSubsetFonts(boolean value)
```


Especifica si se debe guardar un subconjunto de las fuentes TrueType incrustadas con el documento. El valor predeterminado de esta propiedad es false.

Esta opción funciona solo cuando la propiedad [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) está establecida en true.

 **Remarks:** 

Esta opción funciona solo para los formatos DOC, DOCX y RTF.

 **Examples:** 

Muestra cómo guardar un documento con fuentes TrueType incrustadas.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

