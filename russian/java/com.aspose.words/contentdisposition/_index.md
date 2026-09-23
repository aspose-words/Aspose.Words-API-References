---
title: "ContentDisposition"
linktitle: "ContentDisposition"
second_title: "Aspose.Words для Java"
description: "Перечисляет различные способы представления документа в браузере клиента в Java."
type: docs
weight: 126
url: /ru/java/com.aspose.words/contentdisposition/
---

**Inheritance:**
java.lang.Object
```
public class ContentDisposition
```

Перечисляет различные способы отображения документа в браузере клиента.

 **Remarks:** 

Обратите внимание, что реальное поведение в браузере клиента может зависеть от настроек безопасности браузера.

 **Examples:** 

Показывает, как выполнить слияние почты, а затем сохранить документ в браузер клиента.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertField(" MERGEFIELD FullName ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD Company ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD Address ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD City ");

 doc.getMailMerge().execute(new String[]{"FullName", "Company", "Address", "City"},
         new Object[]{"James Bond", "MI5 Headquarters", "Milbank", "London"});
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [ATTACHMENT](#ATTACHMENT) | Отправляет документ в браузер и предлагает вариант сохранить документ на диск или открыть в приложении, связанном с расширением документа. |
| [INLINE](#INLINE) | Отправляет документ в браузер и предлагает вариант сохранить документ на диск или открыть его внутри браузера. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String contentDispositionName)](#fromName-java.lang.String) |  |
| [getName(int contentDisposition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int contentDisposition)](#toString-int) |  |
### ATTACHMENT {#ATTACHMENT}
```
public static int ATTACHMENT
```


Отправляет документ в браузер и предлагает вариант сохранить документ на диск или открыть в приложении, связанном с расширением документа.

### INLINE {#INLINE}
```
public static int INLINE
```


Отправляет документ в браузер и предлагает вариант сохранить документ на диск или открыть его внутри браузера.

### length {#length}
```
public static int length
```


### fromName(String contentDispositionName) {#fromName-java.lang.String}
```
public static int fromName(String contentDispositionName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| contentDispositionName | java.lang.String |  |

**Returns:**
int
### getName(int contentDisposition) {#getName-int}
```
public static String getName(int contentDisposition)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| contentDisposition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int contentDisposition) {#toString-int}
```
public static String toString(int contentDisposition)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| contentDisposition | int |  |

**Returns:**
java.lang.String
