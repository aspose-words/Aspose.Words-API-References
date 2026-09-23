---
title: "MailMergeDestination"
linktitle: "MailMergeDestination"
second_title: "Aspose.Words для Java"
description: "Указывает возможные результаты, которые могут быть получены при выполнении слияния почты над документом в Java."
type: docs
weight: 441
url: /ru/java/com.aspose.words/mailmergedestination/
---

**Inheritance:**
java.lang.Object
```
public class MailMergeDestination
```

Указывает возможные результаты, которые могут быть сгенерированы при выполнении слияния почты в документе.
## Поля

| Поле | Описание |
| --- | --- |
| [DEFAULT](#DEFAULT) | Равно значению [NEW\\_DOCUMENT](../../com.aspose.words/mailmergedestination/\\#NEW-DOCUMENT). |
| [EMAIL](#EMAIL) | Указывает, что совместимые хостинговые приложения должны генерировать электронные письма, используя документы, полученные в результате заполнения полей в данном документе данными из указанного внешнего источника данных. |
| [FAX](#FAX) | Указывает, что совместимые хостинговые приложения должны генерировать факсы, используя документы, полученные в результате заполнения полей в данном документе данными из указанного внешнего источника данных. |
| [NEW_DOCUMENT](#NEW-DOCUMENT) | Указывает, что совместимые хостинговые приложения должны создавать новые документы, заполняя поля в данном документе данными из указанного внешнего источника данных. |
| [PRINTER](#PRINTER) | Указывает, что совместимые хостинговые приложения должны печатать документы, полученные в результате заполнения полей в данном документе внешними данными из указанного внешнего источника данных. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String mailMergeDestinationName)](#fromName-java.lang.String) |  |
| [getName(int mailMergeDestination)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mailMergeDestination)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Равно значению [NEW\\_DOCUMENT](../../com.aspose.words/mailmergedestination/\\#NEW-DOCUMENT).

### EMAIL {#EMAIL}
```
public static int EMAIL
```


Указывает, что совместимые хостинговые приложения должны генерировать электронные письма, используя документы, полученные в результате заполнения полей в данном документе данными из указанного внешнего источника данных.

### FAX {#FAX}
```
public static int FAX
```


Указывает, что совместимые хостинговые приложения должны генерировать факсы, используя документы, полученные в результате заполнения полей в данном документе данными из указанного внешнего источника данных.

### NEW_DOCUMENT {#NEW-DOCUMENT}
```
public static int NEW_DOCUMENT
```


Указывает, что совместимые хостинговые приложения должны создавать новые документы, заполняя поля в данном документе данными из указанного внешнего источника данных.

### PRINTER {#PRINTER}
```
public static int PRINTER
```


Указывает, что совместимые хостинговые приложения должны печатать документы, полученные в результате заполнения полей в данном документе внешними данными из указанного внешнего источника данных.

### length {#length}
```
public static int length
```


### fromName(String mailMergeDestinationName) {#fromName-java.lang.String}
```
public static int fromName(String mailMergeDestinationName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| mailMergeDestinationName | java.lang.String |  |

**Returns:**
int
### getName(int mailMergeDestination) {#getName-int}
```
public static String getName(int mailMergeDestination)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| mailMergeDestination | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int mailMergeDestination) {#toString-int}
```
public static String toString(int mailMergeDestination)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| mailMergeDestination | int |  |

**Returns:**
java.lang.String
