---
title: "HyphenationOptions"
linktitle: "HyphenationOptions"
second_title: "Aspose.Words для Java"
description: "Позволяет настраивать параметры переноса слов в документе на Java."
type: docs
weight: 388
url: /ru/java/com.aspose.words/hyphenationoptions/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class HyphenationOptions implements Cloneable
```

Позволяет настроить параметры переносов в документе.

Чтобы узнать больше, посетите статью документации [ Working with Hyphenation ][Working with Hyphenation].

 **Examples:** 

Показывает, как настроить автоматический перенос слов.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```


[Working with Hyphenation]: https://docs.aspose.com/words/java/working-with-hyphenation/
## Методы

| Метод | Описание |
| --- | --- |
| [getAutoHyphenation()](#getAutoHyphenation) | Получает значение, определяющее, включён ли автоматический перенос слов для документа. |
| [getConsecutiveHyphenLimit()](#getConsecutiveHyphenLimit) | Получает максимальное количество последовательных строк, которые могут заканчиваться дефисами. |
| [getHyphenateCaps()](#getHyphenateCaps) | Получает значение, определяющее, разбиваются ли на слоги слова, написанные заглавными буквами. |
| [getHyphenationZone()](#getHyphenationZone) | Получает расстояние в 1/20 пункта от правого поля, в пределах которого не следует разбивать слова на слоги. |
| [setAutoHyphenation(boolean value)](#setAutoHyphenation-boolean) | Устанавливает значение, определяющее, включено ли автоматическое перенесение слов в документе. |
| [setConsecutiveHyphenLimit(int value)](#setConsecutiveHyphenLimit-int) | Устанавливает максимальное количество последовательных строк, которые могут заканчиваться дефисами. |
| [setHyphenateCaps(boolean value)](#setHyphenateCaps-boolean) | Устанавливает значение, определяющее, разбиваются ли на слоги слова, написанные заглавными буквами. |
| [setHyphenationZone(int value)](#setHyphenationZone-int) | Устанавливает расстояние в 1/20 пункта от правого поля, в пределах которого не следует разбивать слова на слоги. |
### getAutoHyphenation() {#getAutoHyphenation}
```
public boolean getAutoHyphenation()
```


Получает значение, определяющее, включено ли автоматическое перенесение слов в документе. Значение по умолчанию для этого свойства — false.

 **Examples:** 

Показывает, как настроить автоматический перенос слов.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
boolean — значение, определяющее, включено ли автоматическое перенесение слов в документе.
### getConsecutiveHyphenLimit() {#getConsecutiveHyphenLimit}
```
public int getConsecutiveHyphenLimit()
```


Получает максимальное количество последовательных строк, которые могут заканчиваться дефисами. Значение по умолчанию для этого свойства — 0.

 **Remarks:** 

Если значение этого свойства установлено в 0, любое количество последовательных строк может заканчиваться дефисами.

Это свойство не оказывает влияния при сохранении в форматы фиксированных страниц, например PDF.

 **Examples:** 

Показывает, как настроить автоматический перенос слов.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
int — максимальное количество последовательных строк, которые могут заканчиваться дефисами.
### getHyphenateCaps() {#getHyphenateCaps}
```
public boolean getHyphenateCaps()
```


Получает значение, определяющее, разбиваются ли на слоги слова, написанные заглавными буквами. Значение по умолчанию для этого свойства — true.

 **Examples:** 

Показывает, как настроить автоматический перенос слов.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
boolean — значение, определяющее, разбиваются ли на слоги слова, написанные заглавными буквами.
### getHyphenationZone() {#getHyphenationZone}
```
public int getHyphenationZone()
```


Получает расстояние в 1/20 пункта от правого поля, в пределах которого не следует разбивать слова на слоги. Значение по умолчанию для этого свойства — 360 (0,25 дюйма).

 **Examples:** 

Показывает, как настроить автоматический перенос слов.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
int — расстояние в 1/20 пункта от правого поля, в пределах которого не следует разбивать слова на слоги.
### setAutoHyphenation(boolean value) {#setAutoHyphenation-boolean}
```
public void setAutoHyphenation(boolean value)
```


Устанавливает значение, определяющее, включено ли автоматическое перенесение слов в документе. Значение по умолчанию для этого свойства — false.

 **Examples:** 

Показывает, как настроить автоматический перенос слов.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Значение, определяющее, включено ли автоматическое перенесение слов в документе. |

### setConsecutiveHyphenLimit(int value) {#setConsecutiveHyphenLimit-int}
```
public void setConsecutiveHyphenLimit(int value)
```


Устанавливает максимальное количество последовательных строк, которые могут заканчиваться дефисами. Значение по умолчанию для этого свойства — 0.

 **Remarks:** 

Если значение этого свойства установлено в 0, любое количество последовательных строк может заканчиваться дефисами.

Это свойство не оказывает влияния при сохранении в форматы фиксированных страниц, например PDF.

 **Examples:** 

Показывает, как настроить автоматический перенос слов.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Максимальное количество последовательных строк, которые могут заканчиваться дефисами. |

### setHyphenateCaps(boolean value) {#setHyphenateCaps-boolean}
```
public void setHyphenateCaps(boolean value)
```


Устанавливает значение, определяющее, разбиваются ли на слоги слова, написанные заглавными буквами. Значение по умолчанию для этого свойства — true.

 **Examples:** 

Показывает, как настроить автоматический перенос слов.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Значение, определяющее, разбиваются ли на слоги слова, написанные заглавными буквами. |

### setHyphenationZone(int value) {#setHyphenationZone-int}
```
public void setHyphenationZone(int value)
```


Устанавливает расстояние в 1/20 пункта от правого поля, в пределах которого не следует разбивать слова на слоги. Значение по умолчанию для этого свойства — 360 (0,25 дюйма).

 **Examples:** 

Показывает, как настроить автоматический перенос слов.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Расстояние в 1/20 пункта от правого поля, в пределах которого не следует разбивать слова на слоги. |

