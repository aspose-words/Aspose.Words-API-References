---
title: FileFormatInfo
second_title: Справочник по API Aspose.Words для Java
description: Содержит данные, возвращаемые методами определения формата документа.
type: docs
weight: 265
url: /ru/java/com.aspose.words/fileformatinfo/
---

**Наследование:**
java.lang.Object
```
public class FileFormatInfo
```

Содержит данные, возвращаемые[FileFormatUtil](../../com.aspose.words/fileformatutil) методы определения формата документа.

 Чтобы узнать больше, посетите**Detect File Format and Check Format Compatibility** документальная статья.

 Вы не создаете экземпляры этого класса напрямую. Объекты этого класса возвращаются**M:Aspose.Words.FileFormatUtil.DetectFileFormat(System.IO.Stream)** методы.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getEncoding()](#getEncoding--) | Получает обнаруженную кодировку, если она применима к текущему формату документа. |
| [getLoadFormat()](#getLoadFormat--) | Получает обнаруженный формат документа. |
| [hasDigitalSignature()](#hasDigitalSignature--) | Возвращает true, если этот документ содержит цифровую подпись. |
| [hashCode()](#hashCode--) |  |
| [isEncrypted()](#isEncrypted--) | Возвращает true, если документ зашифрован и для его открытия требуется пароль. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getEncoding() {#getEncoding--}
```
public Charset getEncoding()
```


Получает обнаруженную кодировку, если она применима к текущему формату документа. На данный момент определяет кодировку только для документов HTML.

**Возвращает:**
java.nio.charset.Charset — обнаруженная кодировка, если она применима к текущему формату документа.
### getLoadFormat() {#getLoadFormat--}
```
public int getLoadFormat()
```


Получает обнаруженный формат документа.

 Когда документ OOXML зашифрован, невозможно определить, является ли он документом Excel, Word или PowerPoint, без его предварительной расшифровки, поэтому для зашифрованного документа OOXML это свойство всегда будет возвращаться.[LoadFormat.DOCX](../../com.aspose.words/loadformat\#DOCX).

**Возвращает:**
 int — Обнаруженный формат документа. Возвращаемое значение является одним из[LoadFormat](../../com.aspose.words/loadformat) константы.
### hasDigitalSignature() {#hasDigitalSignature--}
```
public boolean hasDigitalSignature()
```


Возвращает true, если этот документ содержит цифровую подпись. Это свойство просто информирует о том, что в документе присутствует цифровая подпись, но не указывает, является ли подпись действительной или нет.

Это свойство существует, чтобы помочь вам сортировать документы с цифровой подписью от тех, которые не подписаны. Если вы используете Aspose.Words для изменения и сохранения документа с цифровой подписью, цифровая подпись будет потеряна. Это сделано намеренно, потому что цифровая подпись существует для защиты подлинности документа. Используя это свойство, вы можете обнаруживать документы с цифровой подписью перед их обработкой так же, как и обычные документы, и предпринимать какие-либо действия, чтобы избежать потери цифровой подписи, например, уведомлять пользователя.

**Возвращает:**
boolean — Истинно, если этот документ содержит цифровую подпись.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isEncrypted() {#isEncrypted--}
```
public boolean isEncrypted()
```


Возвращает true, если документ зашифрован и для его открытия требуется пароль.

Это свойство существует, чтобы помочь вам отсортировать зашифрованные документы от незашифрованных. Если вы попытаетесь загрузить зашифрованный документ с помощью Aspose.Words без указания пароля, будет выдано исключение. Вы можете использовать это свойство, чтобы определить, требует ли документ пароль, и выполнить какое-либо действие перед загрузкой документа, например запросить у пользователя пароль.

**Возвращает:**
boolean — True, если документ зашифрован и для его открытия требуется пароль.
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
