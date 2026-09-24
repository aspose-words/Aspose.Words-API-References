---
title: "Dml3DEffectsRenderingMode"
linktitle: "Dml3DEffectsRenderingMode"
second_title: "Aspose.Words Java için"
description: "Java'da 3D şekil efektlerinin nasıl işleneceğini belirtir."
type: docs
weight: 156
url: /tr/java/com.aspose.words/dml3deffectsrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class Dml3DEffectsRenderingMode
```

3B şekil efektlerinin nasıl işleneceğini belirtir.

 **Examples:** 

3D efektlerin nasıl işlendiğini gösterir.

```

 Document doc = new Document(getMyDir() + "DrawingML shape 3D effects.docx");

 RenderCallback warningCallback = new RenderCallback();
 doc.setWarningCallback(warningCallback);

 PdfSaveOptions saveOptions = new PdfSaveOptions();
 saveOptions.setDml3DEffectsRenderingMode(Dml3DEffectsRenderingMode.ADVANCED);

 doc.save(getArtifactsDir() + "PdfSaveOptions.Dml3DEffectsRenderingModeTest.pdf", saveOptions);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [ADVANCED](#ADVANCED) | Gelişmiş 3D efektler (örneğin kenar yuvarlamalar, aydınlatma ve malzemeler) dahil olmak üzere genişletilmiş bir özel efekt listesi işlenir. |
| [BASIC](#BASIC) | Dahili motor tabanlı hafif ve kararlı bir işleme, ancak bu modu kullanırken aydınlatma, malzemeler ve diğer ek efektler gibi gelişmiş efektler gösterilmez. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String dml3DEffectsRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int dml3DEffectsRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int dml3DEffectsRenderingMode)](#toString-int) |  |
### ADVANCED {#ADVANCED}
```
public static int ADVANCED
```


Gelişmiş 3D efektler (örneğin kenar yuvarlamalar, aydınlatma ve malzemeler) dahil olmak üzere genişletilmiş bir özel efekt listesi işlenir.

 **Remarks:** 

Mevcut uygulama OpenGL kullanıyor. Kullanımdan önce sisteminizde OpenGL kütüphanesi sürüm 1.1 veya daha yüksek bir sürümünün yüklü olduğundan emin olun. Bu mod hâlâ geliştirme aşamasındadır ve bazı özellikler desteklenmeyebilir, bu nedenle işleme sonucu kabul edilemezse [BASIC](../../com.aspose.words/dml3deffectsrenderingmode/\#BASIC) modunu kullanmanız önerilir. Ayrıntılar için lütfen belgeleri inceleyin.

### BASIC {#BASIC}
```
public static int BASIC
```


Dahili motor tabanlı hafif ve kararlı bir işleme, ancak bu modu kullanırken aydınlatma, malzemeler ve diğer ek efektler gibi gelişmiş efektler gösterilmez. Ayrıntılar için lütfen belgeleri inceleyin.

### length {#length}
```
public static int length
```


### fromName(String dml3DEffectsRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String dml3DEffectsRenderingModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| dml3DEffectsRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int dml3DEffectsRenderingMode) {#getName-int}
```
public static String getName(int dml3DEffectsRenderingMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| dml3DEffectsRenderingMode | int |  |

**Returns:**
java.lang.String
