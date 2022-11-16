---
title: ReportBuildOptions
second_title: Справочник по API Aspose.Words для Java
description: Задает параметры, управляющие поведением при построении отчета.
type: docs
weight: 477
url: /ru/java/com.aspose.words/reportbuildoptions/
---

**Наследование:**
java.lang.Object
```
public class ReportBuildOptions
```

 Задает параметры, управляющие поведением[ReportingEngine](../../com.aspose.words/reportingengine) при построении отчета.
## Поля

| Поле | Описание |
| --- | --- |
| [ALLOW_MISSING_MEMBERS](#ALLOW-MISSING-MEMBERS) | Указывает, что отсутствующие элементы объекта должны рассматриваться механизмом как пустые литералы. |
| [INLINE_ERROR_MESSAGES](#INLINE-ERROR-MESSAGES) | Указывает, что механизм должен встраивать сообщения об ошибках синтаксиса шаблона в выходные документы. |
| [NONE](#NONE) | Указывает параметры по умолчанию. |
| [REMOVE_EMPTY_PARAGRAPHS](#REMOVE-EMPTY-PARAGRAPHS) | Указывает, что механизм должен удалять абзацы, которые становятся пустыми после удаления или замены тегов синтаксиса шаблона пустыми значениями. |
| [RESPECT_JPEG_EXIF_ORIENTATION](#RESPECT-JPEG-EXIF-ORIENTATION) |  Указывает, что движок должен использовать EXIF\в\значения ориентации изображения для соответствующего поворота вставленных изображений JPEG. |
| [USE_LEGACY_HEADER_FOOTER_VISITING](#USE-LEGACY-HEADER-FOOTER-VISITING) | Указывает, что движок должен посещать дочерние узлы раздела (заголовки, нижние колонтитулы, тело) в порядке, совместимом с версиями Aspose.Words до 21.9. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String reportBuildOptionsName)](#fromName-java.lang.String-) |  |
| [fromNames(Set reportBuildOptionsNames)](#fromNames-java.util.Set-) |  |
| [getClass()](#getClass--) |  |
| [getName(int reportBuildOptions)](#getName-int-) |  |
| [getNames(int reportBuildOptions)](#getNames-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int reportBuildOptions)](#toString-int-) |  |
| [toStringSet(int attr)](#toStringSet-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ALLOW_MISSING_MEMBERS {#ALLOW-MISSING-MEMBERS}
```
public static int ALLOW_MISSING_MEMBERS
```


Указывает, что отсутствующие элементы объекта должны рассматриваться механизмом как пустые литералы. Этот параметр влияет только на доступ к экземплярам (то есть нестатическим) членам объекта и методам расширения. Если этот параметр не установлен, механизм выдает исключение при обнаружении отсутствующего члена объекта.

### INLINE_ERROR_MESSAGES {#INLINE-ERROR-MESSAGES}
```
public static int INLINE_ERROR_MESSAGES
```


Указывает, что механизм должен встраивать сообщения об ошибках синтаксиса шаблона в выходные документы. Если этот параметр не установлен, механизм выдает исключение при обнаружении синтаксической ошибки.

### NONE {#NONE}
```
public static int NONE
```


Указывает параметры по умолчанию.

### REMOVE_EMPTY_PARAGRAPHS {#REMOVE-EMPTY-PARAGRAPHS}
```
public static int REMOVE_EMPTY_PARAGRAPHS
```


Указывает, что механизм должен удалять абзацы, которые становятся пустыми после удаления или замены тегов синтаксиса шаблона пустыми значениями.

### RESPECT_JPEG_EXIF_ORIENTATION {#RESPECT-JPEG-EXIF-ORIENTATION}
```
public static int RESPECT_JPEG_EXIF_ORIENTATION
```


 Указывает, что движок должен использовать EXIF\в\значения ориентации изображения для соответствующего поворота вставленных изображений JPEG.

### USE_LEGACY_HEADER_FOOTER_VISITING {#USE-LEGACY-HEADER-FOOTER-VISITING}
```
public static int USE_LEGACY_HEADER_FOOTER_VISITING
```


Указывает, что движок должен посещать дочерние узлы раздела (заголовки, нижние колонтитулы, тело) в порядке, совместимом с версиями Aspose.Words до 21.9.

По умолчанию движок обрабатывает верхние и нижние колонтитулы так, как если бы они были связаны с разрывами разделов. То есть при посещении дочерних узлов раздела сначала посещается тело, а только потом — верхние и нижние колонтитулы. Это согласуется с поведением Microsoft Word при копировании и вставке или удалении содержимого, состоящего из нескольких разделов, и дает более правильные результаты в большинстве сценариев.

 До Aspose.Words 21.9 движок использовал другой порядок посещения: дочерние узлы раздела посещались в том порядке, в котором они появляются в документе. Примените это значение к[ReportingEngine.getOptions()](../../com.aspose.words/reportingengine\#getOptions--) / [ReportingEngine.setOptions(int)](../../com.aspose.words/reportingengine\#setOptions-int-) если требуется совместимость со старыми версиями Aspose.Words.

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
### fromName(String reportBuildOptionsName) {#fromName-java.lang.String-}
```
public static int fromName(String reportBuildOptionsName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| reportBuildOptionsName | java.lang.String |  |

**Возвращает:**
инт
### fromNames(Set reportBuildOptionsNames) {#fromNames-java.util.Set-}
```
public static int fromNames(Set reportBuildOptionsNames)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| reportBuildOptionsNames | java.util.Set |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int reportBuildOptions) {#getName-int-}
```
public static String getName(int reportBuildOptions)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| reportBuildOptions | int |  |

**Возвращает:**
java.lang.String
### getNames(int reportBuildOptions) {#getNames-int-}
```
public static Set getNames(int reportBuildOptions)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| reportBuildOptions | int |  |

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
### toString(int reportBuildOptions) {#toString-int-}
```
public static String toString(int reportBuildOptions)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| reportBuildOptions | int |  |

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
