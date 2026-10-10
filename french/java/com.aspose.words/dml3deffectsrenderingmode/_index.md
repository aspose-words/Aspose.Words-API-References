---
title: "Dml3DEffectsRenderingMode"
linktitle: "Dml3DEffectsRenderingMode"
second_title: "Aspose.Words pour Java"
description: "Spécifie comment les effets de forme 3D sont rendus en Java."
type: docs
weight: 156
url: /fr/java/com.aspose.words/dml3deffectsrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class Dml3DEffectsRenderingMode
```

Spécifie comment les effets des formes 3D sont rendus.

 **Examples:** 

Montre comment les effets 3D sont rendus.

```

 Document doc = new Document(getMyDir() + "DrawingML shape 3D effects.docx");

 RenderCallback warningCallback = new RenderCallback();
 doc.setWarningCallback(warningCallback);

 PdfSaveOptions saveOptions = new PdfSaveOptions();
 saveOptions.setDml3DEffectsRenderingMode(Dml3DEffectsRenderingMode.ADVANCED);

 doc.save(getArtifactsDir() + "PdfSaveOptions.Dml3DEffectsRenderingModeTest.pdf", saveOptions);
 
```
## Champs

| Champ | Description |
| --- | --- |
| [ADVANCED](#ADVANCED) | Rendu d'une liste étendue d'effets spéciaux incluant des effets 3D avancés tels que les biseaux, l'éclairage et les matériaux. |
| [BASIC](#BASIC) | Un rendu léger et stable, basé sur le moteur interne, mais les effets avancés tels que l'éclairage, les matériaux et d'autres effets supplémentaires ne sont pas affichés lors de l'utilisation de ce mode. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String dml3DEffectsRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int dml3DEffectsRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int dml3DEffectsRenderingMode)](#toString-int) |  |
### ADVANCED {#ADVANCED}
```
public static int ADVANCED
```


Rendu d'une liste étendue d'effets spéciaux incluant des effets 3D avancés tels que les biseaux, l'éclairage et les matériaux.

 **Remarks:** 

L'implémentation actuelle utilise OpenGL. Veuillez vous assurer que la bibliothèque OpenGL version 1.1 ou supérieure est installée sur votre système avant utilisation. Ce mode est encore en cours de développement, et certaines fonctionnalités peuvent ne pas être prises en charge, il est donc recommandé d'utiliser le mode [BASIC](../../com.aspose.words/dml3deffectsrenderingmode/\#BASIC) si le résultat du rendu n'est pas acceptable. Veuillez consulter la documentation pour plus de détails.

### BASIC {#BASIC}
```
public static int BASIC
```


Un rendu léger et stable, basé sur le moteur interne, mais les effets avancés tels que l'éclairage, les matériaux et d'autres effets supplémentaires ne sont pas affichés lors de l'utilisation de ce mode. Veuillez consulter la documentation pour plus de détails.

### length {#length}
```
public static int length
```


### fromName(String dml3DEffectsRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String dml3DEffectsRenderingModeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| dml3DEffectsRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int dml3DEffectsRenderingMode) {#getName-int}
```
public static String getName(int dml3DEffectsRenderingMode)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| dml3DEffectsRenderingMode | int |  |

**Returns:**
java.lang.String
