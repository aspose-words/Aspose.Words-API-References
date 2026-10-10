---
title: "WarningType"
linktitle: "WarningType"
second_title: "Aspose.Words para Java"
description: "Especifica el tipo de advertencia que emite Aspose.Words durante la carga o guardado de documentos en Java."
type: docs
weight: 720
url: /es/java/com.aspose.words/warningtype/
---

**Inheritance:**
java.lang.Object
```
public class WarningType
```

Especifica el tipo de advertencia que emite Aspose.Words durante la carga o guardado del documento.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [DATA_LOSS](#DATA-LOSS) | Pérdida de datos genérica, sin código específico. |
| [DATA_LOSS_CATEGORY](#DATA-LOSS-CATEGORY) | Algún texto/caracter/imagen u otros datos faltarán tanto del árbol del documento después de la carga, como del documento creado después del guardado. |
| [FONT_EMBEDDING](#FONT-EMBEDDING) | Pérdida de información de fuentes incrustadas durante el guardado del documento. |
| [FONT_SUBSTITUTION](#FONT-SUBSTITUTION) | La fuente ha sido sustituida. |
| [HINT](#HINT) | Advierte sobre un problema potencial o sugiere una mejora. |
| [MAJOR_FORMATTING_LOSS](#MAJOR-FORMATTING-LOSS) | Pérdida de formato mayor genérica, sin código específico. |
| [MAJOR_FORMATTING_LOSS_CATEGORY](#MAJOR-FORMATTING-LOSS-CATEGORY) | El documento resultante o una ubicación particular en él podría verse sustancialmente diferente en comparación con el documento original. |
| [MINOR_FORMATTING_LOSS](#MINOR-FORMATTING-LOSS) | Pérdida de formato menor genérica, sin código específico. |
| [MINOR_FORMATTING_LOSS_CATEGORY](#MINOR-FORMATTING-LOSS-CATEGORY) | El documento resultante o una ubicación particular en él podría verse algo diferente en comparación con el documento original. |
| [UNEXPECTED_CONTENT](#UNEXPECTED-CONTENT) | Contenido inesperado genérico, sin código específico. |
| [UNEXPECTED_CONTENT_CATEGORY](#UNEXPECTED-CONTENT-CATEGORY) | Algunos contenidos en el documento fuente no pudieron ser reconocidos (p.ej. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String warningTypeName)](#fromName-java.lang.String) |  |
| [fromNames(Set warningTypeNames)](#fromNames-java.util.Set) |  |
| [getName(int warningType)](#getName-int) |  |
| [getNames(int warningType)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int warningType)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### DATA_LOSS {#DATA-LOSS}
```
public static int DATA_LOSS
```


Pérdida de datos genérica, sin código específico.

### DATA_LOSS_CATEGORY {#DATA-LOSS-CATEGORY}
```
public static int DATA_LOSS_CATEGORY
```


Algún texto/caracter/imagen u otros datos faltarán tanto del árbol del documento después de la carga, como del documento creado después del guardado.

### FONT_EMBEDDING {#FONT-EMBEDDING}
```
public static int FONT_EMBEDDING
```


Pérdida de información de fuentes incrustadas durante el guardado del documento.

### FONT_SUBSTITUTION {#FONT-SUBSTITUTION}
```
public static int FONT_SUBSTITUTION
```


La fuente ha sido sustituida.

### HINT {#HINT}
```
public static int HINT
```


Advierte sobre un problema potencial o sugiere una mejora.

### MAJOR_FORMATTING_LOSS {#MAJOR-FORMATTING-LOSS}
```
public static int MAJOR_FORMATTING_LOSS
```


Pérdida de formato mayor genérica, sin código específico.

### MAJOR_FORMATTING_LOSS_CATEGORY {#MAJOR-FORMATTING-LOSS-CATEGORY}
```
public static int MAJOR_FORMATTING_LOSS_CATEGORY
```


El documento resultante o una ubicación particular en él podría verse sustancialmente diferente en comparación con el documento original.

### MINOR_FORMATTING_LOSS {#MINOR-FORMATTING-LOSS}
```
public static int MINOR_FORMATTING_LOSS
```


Pérdida de formato menor genérica, sin código específico.

### MINOR_FORMATTING_LOSS_CATEGORY {#MINOR-FORMATTING-LOSS-CATEGORY}
```
public static int MINOR_FORMATTING_LOSS_CATEGORY
```


El documento resultante o una ubicación particular en él podría verse algo diferente en comparación con el documento original.

### UNEXPECTED_CONTENT {#UNEXPECTED-CONTENT}
```
public static int UNEXPECTED_CONTENT
```


Contenido inesperado genérico, sin código específico.

### UNEXPECTED_CONTENT_CATEGORY {#UNEXPECTED-CONTENT-CATEGORY}
```
public static int UNEXPECTED_CONTENT_CATEGORY
```


Algunos contenidos en el documento fuente no pudieron ser reconocidos (p.ej. no es compatible), esto puede o no causar problemas o resultar en pérdida de datos/formato.

### length {#length}
```
public static int length
```


### fromName(String warningTypeName) {#fromName-java.lang.String}
```
public static int fromName(String warningTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| warningTypeName | java.lang.String |  |

**Returns:**
int
### fromNames(Set warningTypeNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set warningTypeNames)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| warningTypeNames | java.util.Set |  |

**Returns:**
int
### getName(int warningType) {#getName-int}
```
public static String getName(int warningType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| warningType | int |  |

**Returns:**
java.lang.String
### getNames(int warningType) {#getNames-int}
```
public static Set getNames(int warningType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| warningType | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int warningType) {#toString-int}
```
public static String toString(int warningType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| warningType | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
