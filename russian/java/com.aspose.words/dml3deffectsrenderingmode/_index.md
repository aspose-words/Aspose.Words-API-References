---
title: "Dml3DEffectsRenderingMode"
linktitle: "Dml3DEffectsRenderingMode"
second_title: "Aspose.Words для Java"
description: "Указывает, как визуализируются 3D-эффекты фигур в Java."
type: docs
weight: 156
url: /ru/java/com.aspose.words/dml3deffectsrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class Dml3DEffectsRenderingMode
```

Указывает, как отображаются эффекты 3D‑форм.

 **Examples:** 

Показывает, как визуализируются 3D-эффекты.

```

 Document doc = new Document(getMyDir() + "DrawingML shape 3D effects.docx");

 RenderCallback warningCallback = new RenderCallback();
 doc.setWarningCallback(warningCallback);

 PdfSaveOptions saveOptions = new PdfSaveOptions();
 saveOptions.setDml3DEffectsRenderingMode(Dml3DEffectsRenderingMode.ADVANCED);

 doc.save(getArtifactsDir() + "PdfSaveOptions.Dml3DEffectsRenderingModeTest.pdf", saveOptions);
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [ADVANCED](#ADVANCED) | Визуализация расширенного списка специальных эффектов, включая продвинутые 3D-эффекты, такие как фаски, освещение и материалы. |
| [BASIC](#BASIC) | Лёгкая и стабильная визуализация, основанная на внутреннем движке, но продвинутые эффекты, такие как освещение, материалы и другие дополнительные эффекты, не отображаются при использовании этого режима. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String dml3DEffectsRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int dml3DEffectsRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int dml3DEffectsRenderingMode)](#toString-int) |  |
### ADVANCED {#ADVANCED}
```
public static int ADVANCED
```


Визуализация расширенного списка специальных эффектов, включая продвинутые 3D-эффекты, такие как фаски, освещение и материалы.

 **Remarks:** 

Текущая реализация использует OpenGL. Пожалуйста, убедитесь, что библиотека OpenGL версии 1.1 или выше установлена в вашей системе перед использованием. Этот режим всё ещё находится в разработке, и некоторые функции могут не поддерживаться, поэтому рекомендуется использовать режим [BASIC](../../com.aspose.words/dml3deffectsrenderingmode/\#BASIC), если результат визуализации неудовлетворителен. Пожалуйста, см. документацию для подробностей.

### BASIC {#BASIC}
```
public static int BASIC
```


Лёгкая и стабильная визуализация, основанная на внутреннем движке, но продвинутые эффекты, такие как освещение, материалы и другие дополнительные эффекты, не отображаются при использовании этого режима. Пожалуйста, см. документацию для подробностей.

### length {#length}
```
public static int length
```


### fromName(String dml3DEffectsRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String dml3DEffectsRenderingModeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| dml3DEffectsRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int dml3DEffectsRenderingMode) {#getName-int}
```
public static String getName(int dml3DEffectsRenderingMode)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| dml3DEffectsRenderingMode | int |  |

**Returns:**
java.lang.String
