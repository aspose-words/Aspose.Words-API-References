---
title: "ImportFormatMode"
linktitle: "ImportFormatMode"
second_title: "Aspose.Words для Java"
description: "Указывает, как объединяется форматирование при импорте содержимого из другого документа в Java."
type: docs
weight: 400
url: /ru/java/com.aspose.words/importformatmode/
---

**Inheritance:**
java.lang.Object
```
public class ImportFormatMode
```

Указывает, как форматирование объединяется при импорте содержимого из другого документа.

 **Remarks:** 

При копировании узлов из одного документа в другой эта опция указывает, как разрешается форматирование, когда оба документа имеют стиль с одинаковым именем, но разным форматированием.

Форматирование разрешается следующим образом:

1. Встроенные стили сопоставляются по их независимому от локали идентификатору стиля. Пользовательские стили сопоставляются по регистрозависимому имени стиля.
2. Если соответствующий стиль не найден в целевом документе, стиль (и все стили, на которые он ссылается) копируются в целевой документ, и импортированные узлы обновляются, чтобы ссылаться на новый стиль.
3. Если соответствующий стиль уже существует в целевом документе, то то, что происходит, зависит от параметра  importFormatMode , переданного в **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**, как описано ниже.

При использовании опции [USE\_DESTINATION\_STYLES](../../com.aspose.words/importformatmode/\#USE-DESTINATION-STYLES) если соответствующий стиль уже существует в целевом документе, стиль не копируется, и импортированные узлы обновляются, чтобы ссылаться на существующий стиль.

Недостаток использования [USE\_DESTINATION\_STYLES](../../com.aspose.words/importformatmode/\#USE-DESTINATION-STYLES) заключается в том, что импортированный текст может выглядеть иначе в целевом документе по сравнению с исходным документом. Например, стиль "Heading 1" в исходном документе использует шрифт Arial 16pt, а стиль "Heading 1" в целевом документе использует шрифт Times New Roman 14pt. При импорте текста стиля "Heading 1" без другого прямого форматирования он будет отображаться шрифтом Times New Roman 14pt в целевом документе.

[KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) option allows to make sure the imported content looks the same in the destination document like it looks in the source document. If a matching style already exists in the destination document, the source style formatting is expanded into direct Node attributes and the style is changed to Normal. If the style does not exist in the destination document, then the source style is imported into the destination document and applied to the imported node. Note, that it is not always possible to preserve the source style even if it does not exist in the destination document. In this case formatting of such style will be expanded into direct Node attributes in favor of preserving original Node formatting.

Недостаток использования [KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) состоит в том, что при выполнении нескольких импортов вы можете получить множество стилей в целевом документе, что может затруднить использование согласованного форматирования стилей в Microsoft Word для этого документа.

Использование опции [KEEP\_DIFFERENT\_STYLES](../../com.aspose.words/importformatmode/\#KEEP-DIFFERENT-STYLES) позволяет повторно использовать стили целевого документа, если предоставляемое ими форматирование идентично стилям в исходном документе. Если стиль в целевом документе отличается от исходного, он импортируется.

 **Examples:** 

Показывает, как вставить документ в другой документ.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.insertBreak(BreakType.PAGE_BREAK);

 Document docToInsert = new Document(getMyDir() + "Formatted elements.docx");

 builder.insertDocument(docToInsert, ImportFormatMode.KEEP_SOURCE_FORMATTING);
 builder.getDocument().save(getArtifactsDir() + "DocumentBuilder.InsertDocument.docx");
 
```

**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**
## Поля

| Поле | Описание |
| --- | --- |
| [KEEP_DIFFERENT_STYLES](#KEEP-DIFFERENT-STYLES) | Копировать только стили, отличные от тех, что находятся в исходном документе. |
| [KEEP_SOURCE_FORMATTING](#KEEP-SOURCE-FORMATTING) | Скопировать все необходимые стили в целевой документ, при необходимости сгенерировать уникальные имена стилей. |
| [USE_DESTINATION_STYLES](#USE-DESTINATION-STYLES) | Использовать стили целевого документа и копировать новые стили. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String importFormatModeName)](#fromName-java.lang.String) |  |
| [getName(int importFormatMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int importFormatMode)](#toString-int) |  |
### KEEP_DIFFERENT_STYLES {#KEEP-DIFFERENT-STYLES}
```
public static int KEEP_DIFFERENT_STYLES
```


Копировать только стили, отличные от тех, что находятся в исходном документе.

### KEEP_SOURCE_FORMATTING {#KEEP-SOURCE-FORMATTING}
```
public static int KEEP_SOURCE_FORMATTING
```


Скопировать все необходимые стили в целевой документ, при необходимости сгенерировать уникальные имена стилей.

### USE_DESTINATION_STYLES {#USE-DESTINATION-STYLES}
```
public static int USE_DESTINATION_STYLES
```


Использовать стили целевого документа и копировать новые стили. Это вариант по умолчанию.

### length {#length}
```
public static int length
```


### fromName(String importFormatModeName) {#fromName-java.lang.String}
```
public static int fromName(String importFormatModeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| importFormatModeName | java.lang.String |  |

**Returns:**
int
### getName(int importFormatMode) {#getName-int}
```
public static String getName(int importFormatMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| importFormatMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int importFormatMode) {#toString-int}
```
public static String toString(int importFormatMode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| importFormatMode | int |  |

**Returns:**
java.lang.String
