---
title: PdfEncryptionDetails
second_title: Справочник по API Aspose.Words для Java
description: Содержит сведения о шифровании и разрешениях на доступ к PDF-документу.
type: docs
weight: 454
url: /ru/java/com.aspose.words/pdfencryptiondetails/
---

**Наследование:**
java.lang.Object
```
public class PdfEncryptionDetails
```

Содержит сведения о шифровании и разрешениях на доступ к PDF-документу.

 Чтобы узнать больше, посетите**Protect or Encrypt a Document** документальная статья.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [PdfEncryptionDetails(String userPassword, String ownerPassword)](#PdfEncryptionDetails-java.lang.String-java.lang.String-) | Инициализирует экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getOwnerPassword()](#getOwnerPassword--) | Указывает пароль владельца для зашифрованного PDF-документа. |
| [getPermissions()](#getPermissions--) | Определяет операции, разрешенные пользователю для зашифрованного PDF-документа. |
| [getUserPassword()](#getUserPassword--) | Указывает пароль пользователя, необходимый для открытия зашифрованного PDF-документа. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setOwnerPassword(String value)](#setOwnerPassword-java.lang.String-) | Указывает пароль владельца для зашифрованного PDF-документа. |
| [setPermissions(int value)](#setPermissions-int-) | Определяет операции, разрешенные пользователю для зашифрованного PDF-документа. |
| [setUserPassword(String value)](#setUserPassword-java.lang.String-) | Указывает пароль пользователя, необходимый для открытия зашифрованного PDF-документа. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### PdfEncryptionDetails(String userPassword, String ownerPassword) {#PdfEncryptionDetails-java.lang.String-java.lang.String-}
```
public PdfEncryptionDetails(String userPassword, String ownerPassword)
```


Инициализирует экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| userPassword | java.lang.String |  |
| ownerPassword | java.lang.String |  |

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
### getOwnerPassword() {#getOwnerPassword--}
```
public String getOwnerPassword()
```


Указывает пароль владельца для зашифрованного PDF-документа.

 Пароль владельца позволяет пользователю открывать зашифрованный PDF-документ без каких-либо ограничений доступа, указанных в[getPermissions()](../../com.aspose.words/pdfencryptiondetails\#getPermissions--) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails\#setPermissions-int-).

Пароль владельца не может совпадать с паролем пользователя.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getPermissions() {#getPermissions--}
```
public int getPermissions()
```


 Определяет операции, разрешенные пользователю для зашифрованного PDF-документа. Значение по умолчанию[PdfPermissions.DISALLOW\_ALL](../../com.aspose.words/pdfpermissions\#DISALLOW-ALL).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение представляет собой побитовую комбинацию[PdfPermissions](../../com.aspose.words/pdfpermissions) константы.
### getUserPassword() {#getUserPassword--}
```
public String getUserPassword()
```


Указывает пароль пользователя, необходимый для открытия зашифрованного PDF-документа.

 Пароль пользователя потребуется для открытия зашифрованного PDF-документа для просмотра. Разрешения, указанные в[getPermissions()](../../com.aspose.words/pdfencryptiondetails\#getPermissions--) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails\#setPermissions-int-) будет обеспечиваться программным обеспечением считывателя.

Пароль пользователя может быть нулевым или пустой строкой, в этом случае от пользователя не потребуется пароль при открытии документа PDF. Пароль пользователя не может совпадать с паролем владельца.

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




### setOwnerPassword(String value) {#setOwnerPassword-java.lang.String-}
```
public void setOwnerPassword(String value)
```


Указывает пароль владельца для зашифрованного PDF-документа.

 Пароль владельца позволяет пользователю открывать зашифрованный PDF-документ без каких-либо ограничений доступа, указанных в[getPermissions()](../../com.aspose.words/pdfencryptiondetails\#getPermissions--) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails\#setPermissions-int-).

Пароль владельца не может совпадать с паролем пользователя.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setPermissions(int value) {#setPermissions-int-}
```
public void setPermissions(int value)
```


 Определяет операции, разрешенные пользователю для зашифрованного PDF-документа. Значение по умолчанию[PdfPermissions.DISALLOW\_ALL](../../com.aspose.words/pdfpermissions\#DISALLOW-ALL).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть побитовой комбинацией[PdfPermissions](../../com.aspose.words/pdfpermissions) константы. |

### setUserPassword(String value) {#setUserPassword-java.lang.String-}
```
public void setUserPassword(String value)
```


Указывает пароль пользователя, необходимый для открытия зашифрованного PDF-документа.

 Пароль пользователя потребуется для открытия зашифрованного PDF-документа для просмотра. Разрешения, указанные в[getPermissions()](../../com.aspose.words/pdfencryptiondetails\#getPermissions--) / [setPermissions(int)](../../com.aspose.words/pdfencryptiondetails\#setPermissions-int-) будет обеспечиваться программным обеспечением считывателя.

Пароль пользователя может быть нулевым или пустой строкой, в этом случае от пользователя не потребуется пароль при открытии документа PDF. Пароль пользователя не может совпадать с паролем владельца.

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
