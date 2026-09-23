---
title: "Dml3DEffectsRenderingMode"
linktitle: "Dml3DEffectsRenderingMode"
second_title: "Aspose.Words per Java"
description: "Specifica come gli effetti delle forme 3D vengono renderizzati in Java."
type: docs
weight: 156
url: /it/java/com.aspose.words/dml3deffectsrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class Dml3DEffectsRenderingMode
```

Specifica come vengono renderizzati gli effetti delle forme 3D.

 **Examples:** 

Mostra come vengono renderizzati gli effetti 3D.

```

 Document doc = new Document(getMyDir() + "DrawingML shape 3D effects.docx");

 RenderCallback warningCallback = new RenderCallback();
 doc.setWarningCallback(warningCallback);

 PdfSaveOptions saveOptions = new PdfSaveOptions();
 saveOptions.setDml3DEffectsRenderingMode(Dml3DEffectsRenderingMode.ADVANCED);

 doc.save(getArtifactsDir() + "PdfSaveOptions.Dml3DEffectsRenderingModeTest.pdf", saveOptions);
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [ADVANCED](#ADVANCED) | Rendering di un elenco esteso di effetti speciali, inclusi effetti 3D avanzati come smussi, illuminazione e materiali. |
| [BASIC](#BASIC) | Un rendering leggero e stabile, basato sul motore interno, ma gli effetti avanzati come illuminazione, materiali e altri effetti aggiuntivi non vengono visualizzati quando si utilizza questa modalità. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String dml3DEffectsRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int dml3DEffectsRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int dml3DEffectsRenderingMode)](#toString-int) |  |
### ADVANCED {#ADVANCED}
```
public static int ADVANCED
```


Rendering di un elenco esteso di effetti speciali, inclusi effetti 3D avanzati come smussi, illuminazione e materiali.

 **Remarks:** 

L'implementazione attuale utilizza OpenGL. Assicurati che la libreria OpenGL versione 1.1 o superiore sia installata sul tuo sistema prima dell'uso. Questa modalità è ancora in sviluppo e alcune funzionalità potrebbero non essere supportate, quindi è consigliato utilizzare la modalità [BASIC](../../com.aspose.words/dml3deffectsrenderingmode/\\#BASIC) se il risultato del rendering non è accettabile. Consulta la documentazione per i dettagli.

### BASIC {#BASIC}
```
public static int BASIC
```


Un rendering leggero e stabile, basato sul motore interno, ma gli effetti avanzati come illuminazione, materiali e altri effetti aggiuntivi non vengono visualizzati quando si utilizza questa modalità. Consulta la documentazione per i dettagli.

### length {#length}
```
public static int length
```


### fromName(String dml3DEffectsRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String dml3DEffectsRenderingModeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dml3DEffectsRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int dml3DEffectsRenderingMode) {#getName-int}
```
public static String getName(int dml3DEffectsRenderingMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dml3DEffectsRenderingMode | int |  |

**Returns:**
java.lang.String
