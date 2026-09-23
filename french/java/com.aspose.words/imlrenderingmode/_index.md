---
title: "ImlRenderingMode"
linktitle: "ImlRenderingMode"
second_title: "Aspose.Words pour Java"
description: "Spécifie comment les objets Ink InkML sont rendus aux formats de page fixes en Java."
type: docs
weight: 399
url: /fr/java/com.aspose.words/imlrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class ImlRenderingMode
```

Spécifie comment les objets d'encre (InkML) sont rendus aux formats de page fixe.

 **Examples:** 

Montre comment rendre l'objet Ink.

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
## Champs

| Champ | Description |
| --- | --- |
| [FALLBACK](#FALLBACK) | Si une forme de secours est disponible pour l'objet ink (InkML), Aspose.Words rend la forme de secours à la place de l'InkML. |
| [INK_ML](#INK-ML) | Aspose.Words ignore la forme de secours de l'objet ink (InkML) et rend l'InkML lui‑même. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String imlRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int imlRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int imlRenderingMode)](#toString-int) |  |
### FALLBACK {#FALLBACK}
```
public static int FALLBACK
```


Si une forme de secours est disponible pour l'objet ink (InkML), Aspose.Words rend la forme de secours à la place de l'InkML.

 **Remarks:** 

Veuillez noter qu'après avoir enregistré un document au format de page fixe avec le mode de rendu de secours, les objets InkML dans le modèle de document AW sont remplacés de façon permanente par leurs homologues de secours. En conséquence, enregistrer à nouveau le même document utilisera toujours les formes de secours, même si [ImlRenderingMode](../../com.aspose.words/imlrenderingmode/) est défini sur [INK\_ML](../../com.aspose.words/imlrenderingmode/\#INK-ML).

### INK_ML {#INK-ML}
```
public static int INK_ML
```


Aspose.Words ignore la forme de secours de l'objet ink (InkML) et rend l'InkML lui‑même. C'est le mode par défaut.

### length {#length}
```
public static int length
```


### fromName(String imlRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String imlRenderingModeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| imlRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int imlRenderingMode) {#getName-int}
```
public static String getName(int imlRenderingMode)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| imlRenderingMode | int |  |

**Returns:**
java.lang.String
