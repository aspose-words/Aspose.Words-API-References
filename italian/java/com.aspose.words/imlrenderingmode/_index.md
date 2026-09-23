---
title: "ImlRenderingMode"
linktitle: "ImlRenderingMode"
second_title: "Aspose.Words per Java"
description: "Specifica come gli oggetti Ink InkML vengono renderizzati in formati di pagina fissi in Java."
type: docs
weight: 399
url: /it/java/com.aspose.words/imlrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class ImlRenderingMode
```

Specifica come gli oggetti ink (InkML) vengono renderizzati in formati di pagina fissi.

 **Examples:** 

Mostra come renderizzare l'oggetto Ink.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [FALLBACK](#FALLBACK) | Se è disponibile una forma di fallback per l'oggetto ink (InkML), Aspose.Words renderizza la forma di fallback invece dell'InkML. |
| [INK_ML](#INK-ML) | Aspose.Words ignora la forma di fallback dell'oggetto ink (InkML) e renderizza l'InkML stesso. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String imlRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int imlRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int imlRenderingMode)](#toString-int) |  |
### FALLBACK {#FALLBACK}
```
public static int FALLBACK
```


Se è disponibile una forma di fallback per l'oggetto ink (InkML), Aspose.Words renderizza la forma di fallback invece dell'InkML.

 **Remarks:** 

Si prega di notare che dopo aver salvato un documento in un formato di pagina fisso con modalità di rendering di fallback, gli oggetti InkML nel modello di documento AW vengono sostituiti permanentemente con le loro controparti di fallback. Di conseguenza, salvare nuovamente lo stesso documento utilizzerà sempre le forme di fallback, anche se [ImlRenderingMode](../../com.aspose.words/imlrenderingmode/) è impostato su [INK\\_ML](../../com.aspose.words/imlrenderingmode/\\#INK-ML).

### INK_ML {#INK-ML}
```
public static int INK_ML
```


Aspose.Words ignora la forma di fallback dell'oggetto ink (InkML) e renderizza l'InkML stesso. Questa è la modalità predefinita.

### length {#length}
```
public static int length
```


### fromName(String imlRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String imlRenderingModeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| imlRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int imlRenderingMode) {#getName-int}
```
public static String getName(int imlRenderingMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| imlRenderingMode | int |  |

**Returns:**
java.lang.String
