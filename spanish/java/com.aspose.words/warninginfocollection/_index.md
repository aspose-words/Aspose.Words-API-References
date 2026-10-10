---
title: "WarningInfoCollection"
linktitle: "WarningInfoCollection"
second_title: "Aspose.Words para Java"
description: "Representa una colección tipada de objetos WarningInfo en Java."
type: docs
weight: 718
url: /es/java/com.aspose.words/warninginfocollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.IWarningCallback](../../com.aspose.words/iwarningcallback/), java.lang.Iterable
```
public class WarningInfoCollection implements IWarningCallback, Iterable
```

Representa una colección tipada de objetos [WarningInfo](../../com.aspose.words/warninginfo/).

Para obtener más información, visite el artículo de documentación [ Programming with Documents ][Programming with Documents].

 **Remarks:** 

Puede usar este objeto de colección como la forma más simple de implementación de [IWarningCallback](../../com.aspose.words/iwarningcallback/) para recopilar todas las advertencias que Aspose.Words genera durante una operación de carga o guardado. Cree una instancia de esta clase y asígnela a la propiedad [LoadOptions.getWarningCallback()](../../com.aspose.words/loadoptions/\#getWarningCallback) / [LoadOptions.setWarningCallback(com.aspose.words.IWarningCallback)](../../com.aspose.words/loadoptions/\#setWarningCallback-com.aspose.words.IWarningCallback) o [DocumentBase.getWarningCallback()](../../com.aspose.words/documentbase/\#getWarningCallback) / [DocumentBase.setWarningCallback(com.aspose.words.IWarningCallback)](../../com.aspose.words/documentbase/\#setWarningCallback-com.aspose.words.IWarningCallback).

 **Examples:** 

Muestra cómo establecer la propiedad para encontrar la coincidencia más cercana de una fuente faltante entre las fuentes disponibles.

```

 // Open a document that contains text formatted with a font that does not exist in any of our font sources.
 Document doc = new Document(getMyDir() + "Missing font.docx");

 // Assign a callback for handling font substitution warnings.
 WarningInfoCollection warningCollector = new WarningInfoCollection();
 doc.setWarningCallback(warningCollector);

 // Set a default font name and enable font substitution.
 FontSettings fontSettings = new FontSettings();
 fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
 fontSettings.getSubstitutionSettings().getFontInfoSubstitution().setEnabled(true);

 // Original font metrics should be used after font substitution.
 doc.getLayoutOptions().setKeepOriginalFontMetrics(true);

 // We will get a font substitution warning if we save a document with a missing font.
 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.EnableFontSubstitution.pdf");

 for (WarningInfo info : warningCollector)
 {
     if (info.getWarningType() == WarningType.FONT_SUBSTITUTION)
         System.out.println(info.getDescription());
 }
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Métodos

| Método | Descripción |
| --- | --- |
| [clear()](#clear) | Elimina todos los elementos de la colección. |
| [get(int index)](#get-int) | Obtiene un elemento en el índice especificado. |
| [getCount()](#getCount) | Obtiene el número de elementos contenidos en la colección. |
| [iterator()](#iterator) | Devuelve un objeto iterador que puede usarse para iterar sobre todos los elementos de la colección. |
| [warning(WarningInfo info)](#warning-com.aspose.words.WarningInfo) | Implementa la interfaz [IWarningCallback](../../com.aspose.words/iwarningcallback/). |
### clear() {#clear}
```
public void clear()
```


Elimina todos los elementos de la colección.

 **Examples:** 

Muestra cómo establecer la propiedad para encontrar la coincidencia más cercana de una fuente faltante entre las fuentes disponibles.

```

 // Open a document that contains text formatted with a font that does not exist in any of our font sources.
 Document doc = new Document(getMyDir() + "Missing font.docx");

 // Assign a callback for handling font substitution warnings.
 WarningInfoCollection warningCollector = new WarningInfoCollection();
 doc.setWarningCallback(warningCollector);

 // Set a default font name and enable font substitution.
 FontSettings fontSettings = new FontSettings();
 fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
 fontSettings.getSubstitutionSettings().getFontInfoSubstitution().setEnabled(true);

 // Original font metrics should be used after font substitution.
 doc.getLayoutOptions().setKeepOriginalFontMetrics(true);

 // We will get a font substitution warning if we save a document with a missing font.
 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.EnableFontSubstitution.pdf");

 for (WarningInfo info : warningCollector)
 {
     if (info.getWarningType() == WarningType.FONT_SUBSTITUTION)
         System.out.println(info.getDescription());
 }
 
```

### get(int index) {#get-int}
```
public WarningInfo get(int index)
```


Obtiene un elemento en el índice especificado.

 **Examples:** 

Muestra cómo obtener advertencias sobre formatos no compatibles.

```

 WarningInfoCollection warings = new WarningInfoCollection();
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setWarningCallback(warings);
 Document doc = new Document(getMyDir() + "FB2 document.fb2", loadOptions);

 Assert.assertEquals("The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warings.get(0).getDescription());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | Índice basado en cero del elemento. |

**Returns:**
[WarningInfo](../../com.aspose.words/warninginfo/) - An item at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Obtiene el número de elementos contenidos en la colección.

 **Examples:** 

Muestra cómo obtener advertencias sobre formatos no compatibles.

```

 WarningInfoCollection warings = new WarningInfoCollection();
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setWarningCallback(warings);
 Document doc = new Document(getMyDir() + "FB2 document.fb2", loadOptions);

 Assert.assertEquals("The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document.", warings.get(0).getDescription());
 
```

**Returns:**
int - El número de elementos contenidos en la colección.
### iterator() {#iterator}
```
public Iterator iterator()
```


Devuelve un objeto iterador que puede usarse para iterar sobre todos los elementos de la colección.

**Returns:**
java.util.Iterator
### warning(WarningInfo info) {#warning-com.aspose.words.WarningInfo}
```
public void warning(WarningInfo info)
```


Implementa la interfaz [IWarningCallback](../../com.aspose.words/iwarningcallback/). Añade una advertencia a esta colección.

 **Examples:** 

Muestra cómo establecer la propiedad para encontrar la coincidencia más cercana de una fuente faltante entre las fuentes disponibles.

```

 // Open a document that contains text formatted with a font that does not exist in any of our font sources.
 Document doc = new Document(getMyDir() + "Missing font.docx");

 // Assign a callback for handling font substitution warnings.
 WarningInfoCollection warningCollector = new WarningInfoCollection();
 doc.setWarningCallback(warningCollector);

 // Set a default font name and enable font substitution.
 FontSettings fontSettings = new FontSettings();
 fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
 fontSettings.getSubstitutionSettings().getFontInfoSubstitution().setEnabled(true);

 // Original font metrics should be used after font substitution.
 doc.getLayoutOptions().setKeepOriginalFontMetrics(true);

 // We will get a font substitution warning if we save a document with a missing font.
 doc.setFontSettings(fontSettings);
 doc.save(getArtifactsDir() + "FontSettings.EnableFontSubstitution.pdf");

 for (WarningInfo info : warningCollector)
 {
     if (info.getWarningType() == WarningType.FONT_SUBSTITUTION)
         System.out.println(info.getDescription());
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| info | [WarningInfo](../../com.aspose.words/warninginfo/) |  |

