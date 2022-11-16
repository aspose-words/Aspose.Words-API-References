---
title: MailMergeCleanupOptions
second_title: Справочник по API Aspose.Words для Java
description: Задает параметры, определяющие, какие элементы удаляются при слиянии почты.
type: docs
weight: 381
url: /ru/java/com.aspose.words/mailmergecleanupoptions/
---

**Наследование:**
java.lang.Object
```
public class MailMergeCleanupOptions
```

Задает параметры, определяющие, какие элементы удаляются при слиянии почты.
## Поля

| Поле | Описание |
| --- | --- |
| [NONE](#NONE) | Указывает значение по умолчанию. |
| [REMOVE_CONTAINING_FIELDS](#REMOVE-CONTAINING-FIELDS) | Указывает, следует ли удалять из документа поля, содержащие поля слияния (например, ЕСЛИ), если удаляются вложенные поля слияния. |
| [REMOVE_EMPTY_PARAGRAPHS](#REMOVE-EMPTY-PARAGRAPHS) | Указывает, следует ли удалять из документа абзацы, содержащие поля слияния без данных. |
| [REMOVE_EMPTY_TABLE_ROWS](#REMOVE-EMPTY-TABLE-ROWS) | Указывает, следует ли удалять из документа пустые строки, содержащие области слияния. |
| [REMOVE_STATIC_FIELDS](#REMOVE-STATIC-FIELDS) | Указывает, следует ли удалять статические поля из документа. |
| [REMOVE_UNUSED_FIELDS](#REMOVE-UNUSED-FIELDS) | Указывает, следует ли удалять из документа неиспользуемые поля слияния. |
| [REMOVE_UNUSED_REGIONS](#REMOVE-UNUSED-REGIONS) | Указывает, следует ли удалять из документа неиспользуемые области слияния. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String mailMergeCleanupOptionsName)](#fromName-java.lang.String-) |  |
| [fromNames(Set mailMergeCleanupOptionsNames)](#fromNames-java.util.Set-) |  |
| [getClass()](#getClass--) |  |
| [getName(int mailMergeCleanupOptions)](#getName-int-) |  |
| [getNames(int mailMergeCleanupOptions)](#getNames-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int mailMergeCleanupOptions)](#toString-int-) |  |
| [toStringSet(int attr)](#toStringSet-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### NONE {#NONE}
```
public static int NONE
```


Указывает значение по умолчанию.

### REMOVE_CONTAINING_FIELDS {#REMOVE-CONTAINING-FIELDS}
```
public static int REMOVE_CONTAINING_FIELDS
```


Указывает, следует ли удалять из документа поля, содержащие поля слияния (например, ЕСЛИ), если удаляются вложенные поля слияния.

### REMOVE_EMPTY_PARAGRAPHS {#REMOVE-EMPTY-PARAGRAPHS}
```
public static int REMOVE_EMPTY_PARAGRAPHS
```


Указывает, следует ли удалять из документа абзацы, содержащие поля слияния без данных. Если этот параметр установлен, абзацы, содержащие поля слияния начала и конца области, которые в противном случае пусты, также удаляются.

### REMOVE_EMPTY_TABLE_ROWS {#REMOVE-EMPTY-TABLE-ROWS}
```
public static int REMOVE_EMPTY_TABLE_ROWS
```


Указывает, следует ли удалять из документа пустые строки, содержащие области слияния. Этот параметр применяется только для слияния почты с регионами.

### REMOVE_STATIC_FIELDS {#REMOVE-STATIC-FIELDS}
```
public static int REMOVE_STATIC_FIELDS
```


 Указывает, следует ли удалять статические поля из документа. Статические поля — это поля, результаты которых остаются неизменными при любом изменении документа. Поля, результаты которых не сохраняются в документе, а рассчитываются «на лету» (например,[FieldType.FIELD\_LIST\_NUM](../../com.aspose.words/fieldtype\#FIELD-LIST-NUM), [FieldType.FIELD\_SYMBOL](../../com.aspose.words/fieldtype\#FIELD-SYMBOL)и т. д.) не считаются статическими. Вот полный список типов полей, которые не считаются статическими:

 *  [FieldType.FIELD\_ADVANCE](../../com.aspose.words/fieldtype\#FIELD-ADVANCE)
 *  [FieldType.FIELD\_AUTO\_NUM](../../com.aspose.words/fieldtype\#FIELD-AUTO-NUM)
 *  [FieldType.FIELD\_AUTO\_NUM\_LEGAL](../../com.aspose.words/fieldtype\#FIELD-AUTO-NUM-LEGAL)
 *  [FieldType.FIELD\_AUTO\_NUM\_OUTLINE](../../com.aspose.words/fieldtype\#FIELD-AUTO-NUM-OUTLINE)
 *  [FieldType.FIELD\_BARCODE](../../com.aspose.words/fieldtype\#FIELD-BARCODE)
 *  [FieldType.FIELD\_BIDI\_OUTLINE](../../com.aspose.words/fieldtype\#FIELD-BIDI-OUTLINE)
 *  [FieldType.FIELD\_DATE](../../com.aspose.words/fieldtype\#FIELD-DATE)
 *  [FieldType.FIELD\_DISPLAY\_BARCODE](../../com.aspose.words/fieldtype\#FIELD-DISPLAY-BARCODE)
 *  [FieldType.FIELD\_MERGE\_BARCODE](../../com.aspose.words/fieldtype\#FIELD-MERGE-BARCODE)
 *  [FieldType.FIELD\_FORM\_CHECK\_BOX](../../com.aspose.words/fieldtype\#FIELD-FORM-CHECK-BOX)
 *  [FieldType.FIELD\_FORM\_DROP\_DOWN](../../com.aspose.words/fieldtype\#FIELD-FORM-DROP-DOWN)
 *  [FieldType.FIELD\_FORMULA](../../com.aspose.words/fieldtype\#FIELD-FORMULA)
 *  [FieldType.FIELD\_GO\_TO\_BUTTON](../../com.aspose.words/fieldtype\#FIELD-GO-TO-BUTTON)
 *  [FieldType.FIELD\_HYPERLINK](../../com.aspose.words/fieldtype\#FIELD-HYPERLINK)
 *  [FieldType.FIELD\_INCLUDE\_TEXT](../../com.aspose.words/fieldtype\#FIELD-INCLUDE-TEXT)
 *  [FieldType.FIELD\_INDEX\_ENTRY](../../com.aspose.words/fieldtype\#FIELD-INDEX-ENTRY)
 *  [FieldType.FIELD\_LINK](../../com.aspose.words/fieldtype\#FIELD-LINK)
 *  [FieldType.FIELD\_LIST\_NUM](../../com.aspose.words/fieldtype\#FIELD-LIST-NUM)
 *  [FieldType.FIELD\_MACRO\_BUTTON](../../com.aspose.words/fieldtype\#FIELD-MACRO-BUTTON)
 *  [FieldType.FIELD\_NOTE\_REF](../../com.aspose.words/fieldtype\#FIELD-NOTE-REF)
 *  [FieldType.FIELD\_NUM\_PAGES](../../com.aspose.words/fieldtype\#FIELD-NUM-PAGES)
 *  [FieldType.FIELD\_PAGE](../../com.aspose.words/fieldtype\#FIELD-PAGE)
 *  [FieldType.FIELD\_PAGE\_REF](../../com.aspose.words/fieldtype\#FIELD-PAGE-REF)
 *  [FieldType.FIELD\_PRINT](../../com.aspose.words/fieldtype\#FIELD-PRINT)
 *  [FieldType.FIELD\_PRINT\_DATE](../../com.aspose.words/fieldtype\#FIELD-PRINT-DATE)
 *  [FieldType.FIELD\_PRIVATE](../../com.aspose.words/fieldtype\#FIELD-PRIVATE)
 *  [FieldType.FIELD\_REF\_DOC](../../com.aspose.words/fieldtype\#FIELD-REF-DOC)
 *  [FieldType.FIELD\_SECTION](../../com.aspose.words/fieldtype\#FIELD-SECTION)
 *  [FieldType.FIELD\_SECTION\_PAGES](../../com.aspose.words/fieldtype\#FIELD-SECTION-PAGES)
 *  [FieldType.FIELD\_SYMBOL](../../com.aspose.words/fieldtype\#FIELD-SYMBOL)
 *  [FieldType.FIELD\_TIME](../../com.aspose.words/fieldtype\#FIELD-TIME)
 *  [FieldType.FIELD\_TOA\_ENTRY](../../com.aspose.words/fieldtype\#FIELD-TOA-ENTRY)
 *  [FieldType.FIELD\_TOC\_ENTRY](../../com.aspose.words/fieldtype\#FIELD-TOC-ENTRY)

### REMOVE_UNUSED_FIELDS {#REMOVE-UNUSED-FIELDS}
```
public static int REMOVE_UNUSED_FIELDS
```


Указывает, следует ли удалять из документа неиспользуемые поля слияния.

### REMOVE_UNUSED_REGIONS {#REMOVE-UNUSED-REGIONS}
```
public static int REMOVE_UNUSED_REGIONS
```


Указывает, следует ли удалять из документа неиспользуемые области слияния. Этот параметр применяется только для слияния почты с регионами.

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
### fromName(String mailMergeCleanupOptionsName) {#fromName-java.lang.String-}
```
public static int fromName(String mailMergeCleanupOptionsName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| mailMergeCleanupOptionsName | java.lang.String |  |

**Возвращает:**
инт
### fromNames(Set mailMergeCleanupOptionsNames) {#fromNames-java.util.Set-}
```
public static int fromNames(Set mailMergeCleanupOptionsNames)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| mailMergeCleanupOptionsNames | java.util.Set |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int mailMergeCleanupOptions) {#getName-int-}
```
public static String getName(int mailMergeCleanupOptions)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| mailMergeCleanupOptions | int |  |

**Возвращает:**
java.lang.String
### getNames(int mailMergeCleanupOptions) {#getNames-int-}
```
public static Set getNames(int mailMergeCleanupOptions)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| mailMergeCleanupOptions | int |  |

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
### toString(int mailMergeCleanupOptions) {#toString-int-}
```
public static String toString(int mailMergeCleanupOptions)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| mailMergeCleanupOptions | int |  |

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
