---
title: "NumSpacing"
linktitle: "NumSpacing"
second_title: "Aspose.Words для Java"
description: "Указывает возможные значения, в которых может отображаться интервал цифр в Java."
type: docs
weight: 484
url: /ru/java/com.aspose.words/numspacing/
---

**Inheritance:**
java.lang.Object
```
public class NumSpacing
```

Указывает возможные значения, в которых может отображаться интервал между цифрами.

 **Examples:** 

Показывает, как установить тип интервала цифр.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // This effect is only supported in newer versions of MS Word.
 doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2019);

 builder.write("1 ");
 builder.write("This is an example");

 Run run = doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0);
 if (run.getFont().getNumberSpacing() == NumSpacing.DEFAULT)
     run.getFont().setNumberSpacing(NumSpacing.PROPORTIONAL);

 doc.save(getArtifactsDir() + "Fonts.NumberSpacing.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [DEFAULT](#DEFAULT) | Указывает, что цифры отображаются в стандартной форме шрифта\\u2019s. |
| [PROPORTIONAL](#PROPORTIONAL) | Указывает, что формы цифр, разработанные как пропорционально распределённые, отображаются, если это поддерживается шрифтом. |
| [TABULAR](#TABULAR) | Указывает, что формы цифр, разработанные как табличные, отображаются, если это поддерживается шрифтом. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String numSpacingName)](#fromName-java.lang.String) |  |
| [getName(int numSpacing)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int numSpacing)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Указывает, что цифры отображаются в стандартной форме шрифта\\u2019s.

### PROPORTIONAL {#PROPORTIONAL}
```
public static int PROPORTIONAL
```


Указывает, что формы цифр, разработанные как пропорционально распределённые, отображаются, если это поддерживается шрифтом.

### TABULAR {#TABULAR}
```
public static int TABULAR
```


Указывает, что формы цифр, разработанные как табличные, отображаются, если это поддерживается шрифтом.

### length {#length}
```
public static int length
```


### fromName(String numSpacingName) {#fromName-java.lang.String}
```
public static int fromName(String numSpacingName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| numSpacingName | java.lang.String |  |

**Returns:**
int
### getName(int numSpacing) {#getName-int}
```
public static String getName(int numSpacing)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| numSpacing | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int numSpacing) {#toString-int}
```
public static String toString(int numSpacing)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| numSpacing | int |  |

**Returns:**
java.lang.String
