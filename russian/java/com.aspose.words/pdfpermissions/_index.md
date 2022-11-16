---
title: PdfPermissions
second_title: Справочник по API Aspose.Words для Java
description: Определяет операции, разрешенные пользователю для зашифрованного PDF-документа.
type: docs
weight: 460
url: /ru/java/com.aspose.words/pdfpermissions/
---

**Наследование:**
java.lang.Object
```
public class PdfPermissions
```

Определяет операции, разрешенные пользователю для зашифрованного PDF-документа.
## Поля

| Поле | Описание |
| --- | --- |
| [ALLOW_ALL](#ALLOW-ALL) | Разрешает все операции с документом PDF. |
| [CONTENT_COPY](#CONTENT-COPY) |  Скопируйте или иным образом извлеките текст и графику из документа с помощью операций, отличных от контролируемых[CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions\#CONTENT-COPY-FOR-ACCESSIBILITY). |
| [CONTENT_COPY_FOR_ACCESSIBILITY](#CONTENT-COPY-FOR-ACCESSIBILITY) | Извлечение текста и графики (для обеспечения доступности для пользователей с ограниченными возможностями или для других целей). |
| [DISALLOW_ALL](#DISALLOW-ALL) | Запрещает все операции с документом PDF. |
| [DOCUMENT_ASSEMBLY](#DOCUMENT-ASSEMBLY) |  Соберите документ (вставьте, поверните или удалите страницы и создайте элементы структуры документа или эскизы), даже если[MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions\#MODIFY-CONTENTS) ясно. |
| [FILL_IN](#FILL-IN) |  Заполните существующие поля интерактивной формы (включая поля подписи), даже если[MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions\#MODIFY-CONTENTS) ясно. |
| [HIGH_RESOLUTION_PRINTING](#HIGH-RESOLUTION-PRINTING) | Распечатайте документ в представлении, из которого можно создать точную цифровую копию содержимого PDF на основе алгоритма, зависящего от реализации. |
| [MODIFY_ANNOTATIONS](#MODIFY-ANNOTATIONS) |  Добавьте или измените текстовые аннотации, заполните поля интерактивной формы и, если[MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions\#MODIFY-CONTENTS) также задавать, создавать или изменять поля интерактивной формы (включая поля подписи). |
| [MODIFY_CONTENTS](#MODIFY-CONTENTS) |  Изменять содержимое документа с помощью операций, отличных от тех, которые контролируются[MODIFY\_ANNOTATIONS](../../com.aspose.words/pdfpermissions\#MODIFY-ANNOTATIONS), [FILL\_IN](../../com.aspose.words/pdfpermissions\#FILL-IN) , а также[DOCUMENT\_ASSEMBLY](../../com.aspose.words/pdfpermissions\#DOCUMENT-ASSEMBLY). |
| [PRINTING](#PRINTING) |  Распечатайте документ (возможно, не на самом высоком уровне качества, в зависимости от того,[HIGH\_RESOLUTION\_PRINTING](../../com.aspose.words/pdfpermissions\#HIGH-RESOLUTION-PRINTING) также установлено). |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String pdfPermissionsName)](#fromName-java.lang.String-) |  |
| [fromNames(Set pdfPermissionsNames)](#fromNames-java.util.Set-) |  |
| [getClass()](#getClass--) |  |
| [getName(int pdfPermissions)](#getName-int-) |  |
| [getNames(int pdfPermissions)](#getNames-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int pdfPermissions)](#toString-int-) |  |
| [toStringSet(int attr)](#toStringSet-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ALLOW_ALL {#ALLOW-ALL}
```
public static int ALLOW_ALL
```


Разрешает все операции с документом PDF.

### CONTENT_COPY {#CONTENT-COPY}
```
public static int CONTENT_COPY
```


 Скопируйте или иным образом извлеките текст и графику из документа с помощью операций, отличных от контролируемых[CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions\#CONTENT-COPY-FOR-ACCESSIBILITY).

### CONTENT_COPY_FOR_ACCESSIBILITY {#CONTENT-COPY-FOR-ACCESSIBILITY}
```
public static int CONTENT_COPY_FOR_ACCESSIBILITY
```


Извлечение текста и графики (для обеспечения доступности для пользователей с ограниченными возможностями или для других целей).

### DISALLOW_ALL {#DISALLOW-ALL}
```
public static int DISALLOW_ALL
```


Запрещает все операции с документом PDF. Это значение по умолчанию.

### DOCUMENT_ASSEMBLY {#DOCUMENT-ASSEMBLY}
```
public static int DOCUMENT_ASSEMBLY
```


 Соберите документ (вставьте, поверните или удалите страницы и создайте элементы структуры документа или эскизы), даже если[MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions\#MODIFY-CONTENTS) ясно.

### FILL_IN {#FILL-IN}
```
public static int FILL_IN
```


 Заполните существующие поля интерактивной формы (включая поля подписи), даже если[MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions\#MODIFY-CONTENTS) ясно.

### HIGH_RESOLUTION_PRINTING {#HIGH-RESOLUTION-PRINTING}
```
public static int HIGH_RESOLUTION_PRINTING
```


Распечатайте документ в представлении, из которого можно создать точную цифровую копию содержимого PDF на основе алгоритма, зависящего от реализации. Когда этот флаг снят (и[PRINTING](../../com.aspose.words/pdfpermissions\#PRINTING) установлен), печать должна быть ограничена низкоуровневым представлением внешнего вида, возможно, с ухудшением качества.

### MODIFY_ANNOTATIONS {#MODIFY-ANNOTATIONS}
```
public static int MODIFY_ANNOTATIONS
```


 Добавьте или измените текстовые аннотации, заполните поля интерактивной формы и, если[MODIFY\_CONTENTS](../../com.aspose.words/pdfpermissions\#MODIFY-CONTENTS) также задавать, создавать или изменять поля интерактивной формы (включая поля подписи).

### MODIFY_CONTENTS {#MODIFY-CONTENTS}
```
public static int MODIFY_CONTENTS
```


 Изменять содержимое документа с помощью операций, отличных от тех, которые контролируются[MODIFY\_ANNOTATIONS](../../com.aspose.words/pdfpermissions\#MODIFY-ANNOTATIONS), [FILL\_IN](../../com.aspose.words/pdfpermissions\#FILL-IN) , а также[DOCUMENT\_ASSEMBLY](../../com.aspose.words/pdfpermissions\#DOCUMENT-ASSEMBLY).

### PRINTING {#PRINTING}
```
public static int PRINTING
```


 Распечатайте документ (возможно, не на самом высоком уровне качества, в зависимости от того,[HIGH\_RESOLUTION\_PRINTING](../../com.aspose.words/pdfpermissions\#HIGH-RESOLUTION-PRINTING) также установлено).

### length {#length}
```
public static int length
```


### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Возвращает:**
логический
### fromName(String pdfPermissionsName) {#fromName-java.lang.String-}
```
public static int fromName(String pdfPermissionsName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfPermissionsName | java.lang.String |  |

**Возвращает:**
инт
### fromNames(Set pdfPermissionsNames) {#fromNames-java.util.Set-}
```
public static int fromNames(Set pdfPermissionsNames)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfPermissionsNames | java.util.Set |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int pdfPermissions) {#getName-int-}
```
public static String getName(int pdfPermissions)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfPermissions | int |  |

**Возвращает:**
java.lang.String
### getNames(int pdfPermissions) {#getNames-int-}
```
public static Set getNames(int pdfPermissions)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfPermissions | int |  |

**Возвращает:**
java.util.Set
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Возвращает:**
инт[]
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### toString(int pdfPermissions) {#toString-int-}
```
public static String toString(int pdfPermissions)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfPermissions | int |  |

**Возвращает:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int-}
```
public static String toStringSet(int attr)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| attr | int |  |

**Возвращает:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
