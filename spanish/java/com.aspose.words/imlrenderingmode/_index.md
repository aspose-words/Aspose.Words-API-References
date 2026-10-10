---
title: "ImlRenderingMode"
linktitle: "ImlRenderingMode"
second_title: "Aspose.Words para Java"
description: "Especifica cómo se renderizan los objetos de tinta InkML a formatos de página fija en Java."
type: docs
weight: 399
url: /es/java/com.aspose.words/imlrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class ImlRenderingMode
```

Especifica cómo se renderizan los objetos de tinta (InkML) a formatos de página fija.

 **Examples:** 

Muestra cómo renderizar el objeto Ink.

```

 Document doc = new Document(getMyDir() + "Ink object.docx");

 // Set 'ImlRenderingMode.InkML' ignores fall-back shape of ink (InkML) object and renders InkML itself.
 // If the rendering result is unsatisfactory,
 // please use 'ImlRenderingMode.Fallback' to get a result similar to previous versions.
 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.JPEG);
 {
     saveOptions.setImlRenderingMode(ImlRenderingMode.INK_ML);
 }

 doc.save(getArtifactsDir() + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [FALLBACK](#FALLBACK) | Si hay una forma de respaldo disponible para el objeto de tinta (InkML), Aspose.Words renderiza la forma de respaldo en lugar del InkML. |
| [INK_ML](#INK-ML) | Aspose.Words ignora la forma de respaldo del objeto de tinta (InkML) y renderiza el propio InkML. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String imlRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int imlRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int imlRenderingMode)](#toString-int) |  |
### FALLBACK {#FALLBACK}
```
public static int FALLBACK
```


Si hay una forma de respaldo disponible para el objeto de tinta (InkML), Aspose.Words renderiza la forma de respaldo en lugar del InkML.

 **Remarks:** 

Tenga en cuenta que después de guardar un documento en un formato de página fija con el modo de renderizado de respaldo, los objetos InkML en el modelo de documento de AW se reemplazan permanentemente por sus contrapartes de respaldo. Como resultado, al guardar el mismo documento nuevamente siempre se usarán las formas de respaldo, incluso si [ImlRenderingMode](../../com.aspose.words/imlrenderingmode/) está configurado a [INK\_ML](../../com.aspose.words/imlrenderingmode/\#INK-ML).

### INK_ML {#INK-ML}
```
public static int INK_ML
```


Aspose.Words ignora la forma de respaldo del objeto de tinta (InkML) y renderiza el propio InkML. Este es el modo predeterminado.

### length {#length}
```
public static int length
```


### fromName(String imlRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String imlRenderingModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| imlRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int imlRenderingMode) {#getName-int}
```
public static String getName(int imlRenderingMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| imlRenderingMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int imlRenderingMode) {#toString-int}
```
public static String toString(int imlRenderingMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| imlRenderingMode | int |  |

**Returns:**
java.lang.String
