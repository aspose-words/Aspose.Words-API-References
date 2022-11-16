---
title: FileFormatUtil
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет служебные методы для работы с форматами файлов, такие как определение формата файла или преобразование расширений файлов в перечисления форматов файлов и из них.
type: docs
weight: 266
url: /ru/java/com.aspose.words/fileformatutil/
---

**Наследование:**
java.lang.Object
```
public class FileFormatUtil
```

Предоставляет служебные методы для работы с форматами файлов, такие как определение формата файла или преобразование расширений файлов в перечисления форматов файлов и из них.

 Чтобы узнать больше, посетите**Detect File Format and Check Format Compatibility** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [contentTypeToLoadFormat(String contentType)](#contentTypeToLoadFormat-java.lang.String-) | Преобразует тип контента IANA в перечисляемое значение формата загрузки. |
| [contentTypeToSaveFormat(String contentType)](#contentTypeToSaveFormat-java.lang.String-) | Преобразует тип контента IANA в перечисляемое значение формата сохранения. |
| [detectFileFormat(InputStream stream)](#detectFileFormat-java.io.InputStream-) |  |
| [detectFileFormat(String fileName)](#detectFileFormat-java.lang.String-) | Обнаруживает и возвращает информацию о формате документа. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [extensionToSaveFormat(String extension)](#extensionToSaveFormat-java.lang.String-) |  Преобразует расширение имени файла в[SaveFormat](../../com.aspose.words/saveformat) ценность. |
| [getClass()](#getClass--) |  |
| [hashCode()](#hashCode--) |  |
| [imageTypeToExtension(int imageType)](#imageTypeToExtension-int-) |  |
| [loadFormatToExtension(int loadFormat)](#loadFormatToExtension-int-) |  |
| [loadFormatToSaveFormat(int loadFormat)](#loadFormatToSaveFormat-int-) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [saveFormatToExtension(int saveFormat)](#saveFormatToExtension-int-) |  |
| [saveFormatToLoadFormat(int saveFormat)](#saveFormatToLoadFormat-int-) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### contentTypeToLoadFormat(String contentType) {#contentTypeToLoadFormat-java.lang.String-}
```
public static int contentTypeToLoadFormat(String contentType)
```


Преобразует тип контента IANA в перечисляемое значение формата загрузки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| contentType | java.lang.String |  |

**Возвращает:**
инт
### contentTypeToSaveFormat(String contentType) {#contentTypeToSaveFormat-java.lang.String-}
```
public static int contentTypeToSaveFormat(String contentType)
```


Преобразует тип контента IANA в перечисляемое значение формата сохранения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| contentType | java.lang.String |  |

**Возвращает:**
инт
### detectFileFormat(InputStream stream) {#detectFileFormat-java.io.InputStream-}
```
public static FileFormatInfo detectFileFormat(InputStream stream)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | java.io.InputStream |  |

**Возвращает:**
[FileFormatInfo](../../com.aspose.words/fileformatinfo)
### detectFileFormat(String fileName) {#detectFileFormat-java.lang.String-}
```
public static FileFormatInfo detectFileFormat(String fileName)
```


Обнаруживает и возвращает информацию о формате документа. Обнаруживает и возвращает информацию о формате документа, хранящегося в файле на диске.

 Даже если этот метод определяет формат документа, он не гарантирует, что указанный документ действителен. Этот метод определяет формат документа только путем считывания данных, достаточных для обнаружения. Чтобы полностью убедиться в том, что документ действителен, вам необходимо загрузить документ в[Document](../../com.aspose.words/document) объект.

 Этот метод выдает[FileCorruptedException](../../com.aspose.words/filecorruptedexception)когда формат распознается, но обнаружение не может быть завершено из-за повреждения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Имя файла. |

**Возвращает:**
[FileFormatInfo](../../com.aspose.words/fileformatinfo) - А[FileFormatInfo](../../com.aspose.words/fileformatinfo) объект, содержащий обнаруженную информацию.
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
### extensionToSaveFormat(String extension) {#extensionToSaveFormat-java.lang.String-}
```
public static int extensionToSaveFormat(String extension)
```


 Преобразует расширение имени файла в[SaveFormat](../../com.aspose.words/saveformat) ценность.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| extension | java.lang.String | Расширение файла. Может быть с ведущей точкой или без нее. Без учета регистра.

 Если расширение не может быть распознано, возвращается[SaveFormat.UNKNOWN](../../com.aspose.words/saveformat\#UNKNOWN). |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### imageTypeToExtension(int imageType) {#imageTypeToExtension-int-}
```
public static String imageTypeToExtension(int imageType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| imageType | int |  |

**Возвращает:**
java.lang.String
### loadFormatToExtension(int loadFormat) {#loadFormatToExtension-int-}
```
public static String loadFormatToExtension(int loadFormat)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| loadFormat | int |  |

**Возвращает:**
java.lang.String
### loadFormatToSaveFormat(int loadFormat) {#loadFormatToSaveFormat-int-}
```
public static int loadFormatToSaveFormat(int loadFormat)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| loadFormat | int |  |

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




### saveFormatToExtension(int saveFormat) {#saveFormatToExtension-int-}
```
public static String saveFormatToExtension(int saveFormat)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| saveFormat | int |  |

**Возвращает:**
java.lang.String
### saveFormatToLoadFormat(int saveFormat) {#saveFormatToLoadFormat-int-}
```
public static int saveFormatToLoadFormat(int saveFormat)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| saveFormat | int |  |

**Возвращает:**
инт
### toString() {#toString--}
```
public String toString()
```




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
