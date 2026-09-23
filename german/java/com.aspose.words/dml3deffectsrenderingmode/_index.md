---
title: "Dml3DEffectsRenderingMode"
linktitle: "Dml3DEffectsRenderingMode"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie 3D‑Formeffekte in Java gerendert werden."
type: docs
weight: 156
url: /de/java/com.aspose.words/dml3deffectsrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class Dml3DEffectsRenderingMode
```

Gibt an, wie 3D‑Formeffekte gerendert werden.

 **Examples:** 

Zeigt, wie 3D‑Effekte gerendert werden.

```

 Document doc = new Document(getMyDir() + "DrawingML shape 3D effects.docx");

 RenderCallback warningCallback = new RenderCallback();
 doc.setWarningCallback(warningCallback);

 PdfSaveOptions saveOptions = new PdfSaveOptions();
 saveOptions.setDml3DEffectsRenderingMode(Dml3DEffectsRenderingMode.ADVANCED);

 doc.save(getArtifactsDir() + "PdfSaveOptions.Dml3DEffectsRenderingModeTest.pdf", saveOptions);
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [ADVANCED](#ADVANCED) | Rendern einer erweiterten Liste spezieller Effekte, einschließlich fortgeschrittener 3D‑Effekte wie Abschrägungen, Beleuchtung und Materialien. |
| [BASIC](#BASIC) | Ein leichtgewichtiges und stabiles Rendering, basierend auf der internen Engine, jedoch werden fortgeschrittene Effekte wie Beleuchtung, Materialien und andere zusätzliche Effekte in diesem Modus nicht angezeigt. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String dml3DEffectsRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int dml3DEffectsRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int dml3DEffectsRenderingMode)](#toString-int) |  |
### ADVANCED {#ADVANCED}
```
public static int ADVANCED
```


Rendern einer erweiterten Liste spezieller Effekte, einschließlich fortgeschrittener 3D‑Effekte wie Abschrägungen, Beleuchtung und Materialien.

 **Remarks:** 

Die aktuelle Implementierung verwendet OpenGL. Bitte stellen Sie sicher, dass die OpenGL‑Bibliothek Version 1.1 oder höher auf Ihrem System installiert ist, bevor Sie sie verwenden. Dieser Modus befindet sich noch in der Entwicklung und einige Funktionen werden möglicherweise nicht unterstützt, daher wird empfohlen, den [BASIC](../../com.aspose.words/dml3deffectsrenderingmode/\\#BASIC) Modus zu verwenden, wenn das Rendering‑Ergebnis nicht akzeptabel ist. Bitte lesen Sie die Dokumentation für Details.

### BASIC {#BASIC}
```
public static int BASIC
```


Ein leichtgewichtiges und stabiles Rendering, basierend auf der internen Engine, jedoch werden fortgeschrittene Effekte wie Beleuchtung, Materialien und andere zusätzliche Effekte in diesem Modus nicht angezeigt. Bitte lesen Sie die Dokumentation für Details.

### length {#length}
```
public static int length
```


### fromName(String dml3DEffectsRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String dml3DEffectsRenderingModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dml3DEffectsRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int dml3DEffectsRenderingMode) {#getName-int}
```
public static String getName(int dml3DEffectsRenderingMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dml3DEffectsRenderingMode | int |  |

**Returns:**
java.lang.String
