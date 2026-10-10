---
title: "BlockImportMode"
linktitle: "BlockImportMode"
second_title: "Aspose.Words для Java"
description: "Указывает, как свойства блочных элементов импортируются из HTML‑документов в Java."
type: docs
weight: 39
url: /ru/java/com.aspose.words/blockimportmode/
---

**Inheritance:**
java.lang.Object
```
public class BlockImportMode
```

Указывает, как свойства блочных элементов импортируются из HTML‑документов.

 **Examples:** 

Показывает, как свойства блочных элементов импортируются из HTML‑документов.

```

 final String html = "\n\n \n \n paragraph 1\n paragraph 2\n\n\n";

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();
 // Set the new mode of import HTML block-level elements.
 loadOptions.setBlockImportMode(blockImportMode);

 Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF_8)), loadOptions);
 doc.save(getArtifactsDir() + "HtmlLoadOptions.BlockImport.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [MERGE](#MERGE) | Свойства родительских блоков объединяются и сохраняются в дочерних элементах (т.е. |
| [PRESERVE](#PRESERVE) | Свойства родительских блоков импортируются в специальную логическую структуру и хранятся отдельно от узлов документа. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String blockImportModeName)](#fromName-java.lang.String) |  |
| [getName(int blockImportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int blockImportMode)](#toString-int) |  |
### MERGE {#MERGE}
```
public static int MERGE
```


Свойства родительских блоков объединяются и сохраняются в дочерних элементах (т.е. в абзацах или таблицах).

 **Remarks:** 

Свойства родительских блоков объединяются следующим образом: отступы суммируются; границы блоков более высокого уровня отбрасываются, сохраняются только границы самого внутреннего уровня. В результате, когда указан этот режим, часть форматирования блоков исходного документа будет утеряна.

С другой стороны, поскольку все объединённые свойства блочного уровня хранятся в узлах документа, всё форматирование в результирующем документе будет доступно для изменения.

### PRESERVE {#PRESERVE}
```
public static int PRESERVE
```


Свойства родительских блоков импортируются в специальную логическую структуру и хранятся отдельно от узлов документа.

 **Remarks:** 

Импортируются только отступы и границы HTML‑элементов 'body', 'div' и 'blockquote'. Свойства каждого HTML‑элемента хранятся отдельно.

Этот режим позволяет лучше сохранять границы и отступы, видимые в HTML‑документе, и получать более качественные результаты конвертации. Недостаток заключается в том, что результирующий документ становится труднее изменять, поскольку границы и отступы, хранящиеся в логической структуре, недоступны для редактирования.

Этот режим имитирует поведение MS Word при импорте свойств блоков.

### length {#length}
```
public static int length
```


### fromName(String blockImportModeName) {#fromName-java.lang.String}
```
public static int fromName(String blockImportModeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| blockImportModeName | java.lang.String |  |

**Returns:**
int
### getName(int blockImportMode) {#getName-int}
```
public static String getName(int blockImportMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| blockImportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int blockImportMode) {#toString-int}
```
public static String toString(int blockImportMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| blockImportMode | int |  |

**Returns:**
java.lang.String
