---
title: "HtmlInsertOptions"
linktitle: "HtmlInsertOptions"
second_title: "Aspose.Words для Java"
description: "Указывает параметры для метода MAspose.Words.DocumentBuilder.InsertHtmlSystem.StringAspose.Words.HtmlInsertOptions в Java."
type: docs
weight: 381
url: /ru/java/com.aspose.words/htmlinsertoptions/
---

**Inheritance:**
java.lang.Object
```
public class HtmlInsertOptions
```

Указывает параметры для метода **M:Aspose.Words.DocumentBuilder.InsertHtml(System.String,Aspose.Words.HtmlInsertOptions)**.

 **Examples:** 

Показывает, как лучше сохранять видимые границы и отступы.

```

 final String HTML = "\n                \n                    \n                    \n                        paragraph 1\n                        paragraph 2\n                    \n                    \n                ";

 // Set the new mode of import HTML block-level elements.
 int insertOptions = HtmlInsertOptions.PRESERVE_BLOCKS;

 DocumentBuilder builder = new DocumentBuilder();
 builder.insertHtml(HTML, insertOptions);
 builder.getDocument().save(getArtifactsDir() + "DocumentBuilder.PreserveBlocks.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [NONE](#NONE) | Используйте параметры по умолчанию при вставке HTML. |
| [PRESERVE_BLOCKS](#PRESERVE-BLOCKS) | Сохранять свойства блочных элементов. |
| [REMOVE_LAST_EMPTY_PARAGRAPH](#REMOVE-LAST-EMPTY-PARAGRAPH) | Удалить пустой абзац, который обычно вставляется после HTML, заканчивающегося блочным элементом. |
| [USE_BUILDER_FORMATTING](#USE-BUILDER-FORMATTING) | Используйте шрифтовое и абзацное форматирование, указанное в [DocumentBuilder](../../com.aspose.words/documentbuilder/), в качестве базового форматирования для текста, вставляемого из HTML. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String htmlInsertOptionsName)](#fromName-java.lang.String) |  |
| [fromNames(Set htmlInsertOptionsNames)](#fromNames-java.util.Set) |  |
| [getName(int htmlInsertOptions)](#getName-int) |  |
| [getNames(int htmlInsertOptions)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int htmlInsertOptions)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Используйте параметры по умолчанию при вставке HTML.

### PRESERVE_BLOCKS {#PRESERVE-BLOCKS}
```
public static int PRESERVE_BLOCKS
```


Сохранять свойства блочных элементов.

 **Remarks:** 

По умолчанию свойства родительских блоков объединяются и сохраняются в их дочерних элементах (т. е. абзацах или таблицах). Если эта опция указана, свойства каждого блока сохраняются отдельно в специальной логической структуре. В результате эта опция позволяет лучше сохранять отдельные границы и отступы, видимые в HTML‑документе, и получать более качественные результаты конвертации. Недостаток заключается в том, что полученный документ становится сложнее изменять, поскольку границы и отступы, хранящиеся в логической структуре, недоступны для редактирования.

Сохраняются только отступы и границы HTML‑элементов 'body', 'div' и 'blockquote'. Свойства каждого HTML‑элемента сохраняются отдельно.

Если эта опция указана, Aspose.Words имитирует поведение MS Word при импорте свойств блоков.

### REMOVE_LAST_EMPTY_PARAGRAPH {#REMOVE-LAST-EMPTY-PARAGRAPH}
```
public static int REMOVE_LAST_EMPTY_PARAGRAPH
```


Удалить пустой абзац, который обычно вставляется после HTML, заканчивающегося блочным элементом.

 **Remarks:** 

По умолчанию [DocumentBuilder](../../com.aspose.words/documentbuilder/) гарантирует, что последний блочный элемент, импортированный из HTML, закрывается после импорта и вставляет разрыв абзаца после элемента. Этот разрыв абзаца отделяет содержимое, импортированное из HTML, от содержимого шаблонного документа. Однако если фрагмент HTML вставляется в пустой абзац, этот разрыв абзаца создаст дополнительный пустой абзац. Если такое поведение нежелательно, укажите эту опцию.

### USE_BUILDER_FORMATTING {#USE-BUILDER-FORMATTING}
```
public static int USE_BUILDER_FORMATTING
```


Используйте шрифтовое и абзацное форматирование, указанное в [DocumentBuilder](../../com.aspose.words/documentbuilder/), в качестве базового форматирования для текста, вставляемого из HTML.

 **Remarks:** 

Если эта опция не указана, форматирование [DocumentBuilder](../../com.aspose.words/documentbuilder/) игнорируется, и текст вставляется с форматированием HTML по умолчанию. В результате текст выглядит так, как он отображается в браузерах.

Если эта опция указана, форматирование вставляемого текста основывается на форматировании, указанном в [DocumentBuilder](../../com.aspose.words/documentbuilder/), и текст выглядит так, как будто он был вставлен с помощью [DocumentBuilder.write(java.lang.String)](../../com.aspose.words/documentbuilder/\\#write-java.lang.String).

### length {#length}
```
public static int length
```


### fromName(String htmlInsertOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String htmlInsertOptionsName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| htmlInsertOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set htmlInsertOptionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set htmlInsertOptionsNames)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| htmlInsertOptionsNames | java.util.Set |  |

**Returns:**
int
### getName(int htmlInsertOptions) {#getName-int}
```
public static String getName(int htmlInsertOptions)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| htmlInsertOptions | int |  |

**Returns:**
java.lang.String
### getNames(int htmlInsertOptions) {#getNames-int}
```
public static Set getNames(int htmlInsertOptions)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| htmlInsertOptions | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int htmlInsertOptions) {#toString-int}
```
public static String toString(int htmlInsertOptions)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| htmlInsertOptions | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
