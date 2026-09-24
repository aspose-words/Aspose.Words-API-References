---
title: "Dml3DEffectsRenderingMode"
linktitle: "Dml3DEffectsRenderingMode"
second_title: "Aspose.Words para Java"
description: "Especifica cómo se renderizan los efectos de forma 3D en Java."
type: docs
weight: 156
url: /es/java/com.aspose.words/dml3deffectsrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class Dml3DEffectsRenderingMode
```

Especifica cómo se renderizan los efectos de forma 3D.

 **Examples:** 

Muestra cómo se renderizan los efectos 3D.

```

 Document doc = new Document(getMyDir() + "DrawingML shape 3D effects.docx");

 RenderCallback warningCallback = new RenderCallback();
 doc.setWarningCallback(warningCallback);

 PdfSaveOptions saveOptions = new PdfSaveOptions();
 saveOptions.setDml3DEffectsRenderingMode(Dml3DEffectsRenderingMode.ADVANCED);

 doc.save(getArtifactsDir() + "PdfSaveOptions.Dml3DEffectsRenderingModeTest.pdf", saveOptions);
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [ADVANCED](#ADVANCED) | Renderizado de una lista ampliada de efectos especiales que incluye efectos 3D avanzados como biseles, iluminación y materiales. |
| [BASIC](#BASIC) | Un renderizado ligero y estable, basado en el motor interno, pero los efectos avanzados como iluminación, materiales y otros efectos adicionales no se muestran al usar este modo. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String dml3DEffectsRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int dml3DEffectsRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int dml3DEffectsRenderingMode)](#toString-int) |  |
### ADVANCED {#ADVANCED}
```
public static int ADVANCED
```


Renderizado de una lista ampliada de efectos especiales que incluye efectos 3D avanzados como biseles, iluminación y materiales.

 **Remarks:** 

La implementación actual utiliza OpenGL. Por favor, asegúrese de que la biblioteca OpenGL versión 1.1 o superior esté instalada en su sistema antes de usarla. Este modo aún está en desarrollo, y algunas cosas pueden no ser compatibles, por lo que se recomienda usar el modo [BASIC](../../com.aspose.words/dml3deffectsrenderingmode/\#BASIC) si el resultado del renderizado no es aceptable. Consulte la documentación para obtener más detalles.

### BASIC {#BASIC}
```
public static int BASIC
```


Un renderizado ligero y estable, basado en el motor interno, pero los efectos avanzados como iluminación, materiales y otros efectos adicionales no se muestran al usar este modo. Consulte la documentación para obtener más detalles.

### length {#length}
```
public static int length
```


### fromName(String dml3DEffectsRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String dml3DEffectsRenderingModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| dml3DEffectsRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int dml3DEffectsRenderingMode) {#getName-int}
```
public static String getName(int dml3DEffectsRenderingMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| dml3DEffectsRenderingMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int dml3DEffectsRenderingMode) {#toString-int}
```
public static String toString(int dml3DEffectsRenderingMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| dml3DEffectsRenderingMode | int |  |

**Returns:**
java.lang.String
