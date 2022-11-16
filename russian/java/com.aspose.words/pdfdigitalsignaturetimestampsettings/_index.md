---
title: PdfDigitalSignatureTimestampSettings
second_title: Справочник по API Aspose.Words для Java
description: Содержит настройки временной метки цифровой подписи.
type: docs
weight: 453
url: /ru/java/com.aspose.words/pdfdigitalsignaturetimestampsettings/
---

**Наследование:**
java.lang.Object
```
public class PdfDigitalSignatureTimestampSettings
```

Содержит настройки временной метки цифровой подписи.

 Чтобы узнать больше, посетите**Work with Digital Signatures** документальная статья.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [PdfDigitalSignatureTimestampSettings()](#PdfDigitalSignatureTimestampSettings--) | Инициализирует экземпляр этого класса. |
| [PdfDigitalSignatureTimestampSettings(String serverUrl, String userName, String password)](#PdfDigitalSignatureTimestampSettings-java.lang.String-java.lang.String-java.lang.String-) | Инициализирует экземпляр этого класса. |
| [PdfDigitalSignatureTimestampSettings(String serverUrl, String userName, String password, long timeout)](#PdfDigitalSignatureTimestampSettings-java.lang.String-java.lang.String-java.lang.String-long-) | Инициализирует экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getPassword()](#getPassword--) | Пароль сервера временной метки. |
| [getServerUrl()](#getServerUrl--) | URL-адрес сервера меток времени. |
| [getTimeout()](#getTimeout--) | Значение времени ожидания в миллисекундах для доступа к серверу меток времени. |
| [getUserName()](#getUserName--) | Имя пользователя сервера меток времени. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setPassword(String value)](#setPassword-java.lang.String-) | Пароль сервера временной метки. |
| [setServerUrl(String value)](#setServerUrl-java.lang.String-) | URL-адрес сервера меток времени. |
| [setTimeout(long value)](#setTimeout-long-) | Значение времени ожидания в миллисекундах для доступа к серверу меток времени. |
| [setUserName(String value)](#setUserName-java.lang.String-) | Имя пользователя сервера меток времени. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### PdfDigitalSignatureTimestampSettings() {#PdfDigitalSignatureTimestampSettings--}
```
public PdfDigitalSignatureTimestampSettings()
```


Инициализирует экземпляр этого класса.

### PdfDigitalSignatureTimestampSettings(String serverUrl, String userName, String password) {#PdfDigitalSignatureTimestampSettings-java.lang.String-java.lang.String-java.lang.String-}
```
public PdfDigitalSignatureTimestampSettings(String serverUrl, String userName, String password)
```


Инициализирует экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| serverUrl | java.lang.String | URL-адрес сервера меток времени. |
| userName | java.lang.String | Имя пользователя сервера меток времени. |
| password | java.lang.String | Пароль сервера временной метки. |

### PdfDigitalSignatureTimestampSettings(String serverUrl, String userName, String password, long timeout) {#PdfDigitalSignatureTimestampSettings-java.lang.String-java.lang.String-java.lang.String-long-}
```
public PdfDigitalSignatureTimestampSettings(String serverUrl, String userName, String password, long timeout)
```


Инициализирует экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| serverUrl | java.lang.String | URL-адрес сервера меток времени. |
| userName | java.lang.String | Имя пользователя сервера меток времени. |
| password | java.lang.String | Пароль сервера временной метки. |
| timeout | long | Значение времени ожидания в миллисекундах для доступа к серверу меток времени. |

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
### getPassword() {#getPassword--}
```
public String getPassword()
```


Пароль сервера временной метки. Значение по умолчанию равно нулю.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getServerUrl() {#getServerUrl--}
```
public String getServerUrl()
```


URL-адрес сервера меток времени. Значение по умолчанию равно нулю. Если значение равно null, то цифровая подпись не будет иметь отметку времени.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getTimeout() {#getTimeout--}
```
public long getTimeout()
```


Значение времени ожидания в миллисекундах для доступа к серверу меток времени. Значение по умолчанию — 100 секунд.

**Возвращает:**
long — соответствующее длинное значение.
### getUserName() {#getUserName--}
```
public String getUserName()
```


Имя пользователя сервера меток времени. Значение по умолчанию равно нулю.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
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




### setPassword(String value) {#setPassword-java.lang.String-}
```
public void setPassword(String value)
```


Пароль сервера временной метки. Значение по умолчанию равно нулю.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setServerUrl(String value) {#setServerUrl-java.lang.String-}
```
public void setServerUrl(String value)
```


URL-адрес сервера меток времени. Значение по умолчанию равно нулю. Если значение равно null, то цифровая подпись не будет иметь отметку времени.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setTimeout(long value) {#setTimeout-long-}
```
public void setTimeout(long value)
```


Значение времени ожидания в миллисекундах для доступа к серверу меток времени. Значение по умолчанию — 100 секунд.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | long | Соответствующее длинное значение. |

### setUserName(String value) {#setUserName-java.lang.String-}
```
public void setUserName(String value)
```


Имя пользователя сервера меток времени. Значение по умолчанию равно нулю.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

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
