---
title: "ImlRenderingMode"
linktitle: "ImlRenderingMode"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie Ink‑InkML‑Objekte in Java in feste Seitenformate gerendert werden."
type: docs
weight: 399
url: /de/java/com.aspose.words/imlrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class ImlRenderingMode
```

Gibt an, wie Tintenobjekte (InkML) in feste Seitenformate gerendert werden.

 **Examples:** 

Zeigt, wie ein Ink‑Objekt gerendert wird.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [FALLBACK](#FALLBACK) | Wenn für das Ink‑(InkML)‑Objekt eine Ersatzform verfügbar ist, rendert Aspose.Words die Ersatzform anstelle des InkML. |
| [INK_ML](#INK-ML) | Aspose.Words ignoriert die Ersatzform des Ink‑(InkML)‑Objekts und rendert das InkML selbst. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String imlRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int imlRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int imlRenderingMode)](#toString-int) |  |
### FALLBACK {#FALLBACK}
```
public static int FALLBACK
```


Wenn für das Ink‑(InkML)‑Objekt eine Ersatzform verfügbar ist, rendert Aspose.Words die Ersatzform anstelle des InkML.

 **Remarks:** 

Bitte beachten Sie, dass nach dem Speichern eines Dokuments in ein festes Seitenformat mit dem Ersatz‑Rendermodus InkML‑Objekte im AW‑Dokumentenmodell dauerhaft durch ihre Ersatzgegenstücke ersetzt werden. Infolgedessen wird beim erneuten Speichern desselben Dokuments stets die Ersatzform verwendet, selbst wenn [ImlRenderingMode](../../com.aspose.words/imlrenderingmode/) auf [INK\\_ML](../../com.aspose.words/imlrenderingmode/\\#INK-ML) gesetzt ist.

### INK_ML {#INK-ML}
```
public static int INK_ML
```


Aspose.Words ignoriert die Ersatzform des Ink‑(InkML)‑Objekts und rendert das InkML selbst. Dies ist der Standardmodus.

### length {#length}
```
public static int length
```


### fromName(String imlRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String imlRenderingModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| imlRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int imlRenderingMode) {#getName-int}
```
public static String getName(int imlRenderingMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| imlRenderingMode | int |  |

**Returns:**
java.lang.String
