---
title: "JoinRunsOptions"
linktitle: "JoinRunsOptions"
second_title: "Aspose.Words для Java"
description: "Предоставляет флаги конфигурации для операции объединения диапазонов в Java."
type: docs
weight: 406
url: /ru/java/com.aspose.words/joinrunsoptions/
---

**Inheritance:**
java.lang.Object
```
public class JoinRunsOptions
```

Предоставляет флаги конфигурации для операции объединения пробегов.

 **Examples:** 

Показывает, как объединять диапазоны с одинаковым форматированием, игнорируя избыточные и незначительные атрибуты.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create runs with identical visible formatting but some internal differences.
 builder.getFont().setName("Arial");
 builder.getFont().setSize(12.0);
 builder.write("Hello ");
 builder.write("world");

 // Verify runs before join.
 Assert.assertEquals(2, doc.getFirstSection().getBody().getFirstParagraph().getRuns().getCount());
 Assert.assertEquals("Hello ", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).getText());
 Assert.assertEquals("world", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(1).getText());

 // Configure options to ignore redundant and insignificant attributes during join.
 JoinRunsOptions options = new JoinRunsOptions();
 options.setIgnoreRedundant(true); // Ignore redundant run properties that don't affect appearance.
 options.setIgnoreInsignificant(true); // Ignore insignificant differences like whitespace-only runs.

 // Join runs that have the same visible formatting using the extended options.
 doc.getFirstSection().getBody().getFirstParagraph().joinRunsWithSameFormatting(options);

 // Verify that runs were successfully joined.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getFirstParagraph().getRuns().getCount());
 Assert.assertEquals("Hello world", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).getText());

 doc.save(getArtifactsDir() + "Paragraph.JoinRunsWithSameFormattingWithOptions.docx");
 
```
## Методы

| Метод | Описание |
| --- | --- |
| [getIgnoreInsignificant()](#getIgnoreInsignificant) | True указывает, что незначительные атрибуты всех диапазонов будут игнорироваться при объединении диапазонов с одинаковым форматированием. |
| [getIgnoreRedundant()](#getIgnoreRedundant) | True указывает, что избыточные атрибуты всех диапазонов будут игнорироваться при объединении диапазонов с одинаковым форматированием. |
| [getIgnoreSpacing()](#getIgnoreSpacing) | True указывает, что атрибуты интервалов всех диапазонов будут игнорироваться при объединении диапазонов с одинаковым форматированием. |
| [setIgnoreInsignificant(boolean value)](#setIgnoreInsignificant-boolean) | True указывает, что незначительные атрибуты всех диапазонов будут игнорироваться при объединении диапазонов с одинаковым форматированием. |
| [setIgnoreRedundant(boolean value)](#setIgnoreRedundant-boolean) | True указывает, что избыточные атрибуты всех диапазонов будут игнорироваться при объединении диапазонов с одинаковым форматированием. |
| [setIgnoreSpacing(boolean value)](#setIgnoreSpacing-boolean) | True указывает, что атрибуты интервалов всех диапазонов будут игнорироваться при объединении диапазонов с одинаковым форматированием. |
### getIgnoreInsignificant() {#getIgnoreInsignificant}
```
public boolean getIgnoreInsignificant()
```


True указывает, что незначительные атрибуты всех диапазонов будут игнорироваться при объединении диапазонов с одинаковым форматированием.

 **Remarks:** 

Не значительные атрибуты — это атрибуты, которые не оказывают заметного влияния на форматирование фрагмента с заданным текстовым содержимым. Значение по умолчанию — False.

**Returns:**
boolean - Соответствующее  boolean  значение.
### getIgnoreRedundant() {#getIgnoreRedundant}
```
public boolean getIgnoreRedundant()
```


True указывает, что избыточные атрибуты всех диапазонов будут игнорироваться при объединении диапазонов с одинаковым форматированием.

 **Remarks:** 

Избыточные атрибуты — это атрибуты, которые не влияют на фрагмент с заданным текстовым содержимым. Значение по умолчанию — False.

**Returns:**
boolean - Соответствующее  boolean  значение.
### getIgnoreSpacing() {#getIgnoreSpacing}
```
public boolean getIgnoreSpacing()
```


True указывает, что атрибуты интервалов всех диапазонов будут игнорироваться при объединении диапазонов с одинаковым форматированием.

 **Remarks:** 

Значение по умолчанию — False.

**Returns:**
boolean - Соответствующее  boolean  значение.
### setIgnoreInsignificant(boolean value) {#setIgnoreInsignificant-boolean}
```
public void setIgnoreInsignificant(boolean value)
```


True указывает, что незначительные атрибуты всех диапазонов будут игнорироваться при объединении диапазонов с одинаковым форматированием.

 **Remarks:** 

Не значительные атрибуты — это атрибуты, которые не оказывают заметного влияния на форматирование фрагмента с заданным текстовым содержимым. Значение по умолчанию — False.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setIgnoreRedundant(boolean value) {#setIgnoreRedundant-boolean}
```
public void setIgnoreRedundant(boolean value)
```


True указывает, что избыточные атрибуты всех диапазонов будут игнорироваться при объединении диапазонов с одинаковым форматированием.

 **Remarks:** 

Избыточные атрибуты — это атрибуты, которые не влияют на фрагмент с заданным текстовым содержимым. Значение по умолчанию — False.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setIgnoreSpacing(boolean value) {#setIgnoreSpacing-boolean}
```
public void setIgnoreSpacing(boolean value)
```


True указывает, что атрибуты интервалов всех диапазонов будут игнорироваться при объединении диапазонов с одинаковым форматированием.

 **Remarks:** 

Значение по умолчанию — False.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

