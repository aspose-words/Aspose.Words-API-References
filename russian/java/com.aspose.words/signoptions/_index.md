---
title: SignOptions
second_title: Справочник по API Aspose.Words для Java
description: Позволяет указать параметры подписания документа.
type: docs
weight: 523
url: /ru/java/com.aspose.words/signoptions/
---

**Наследование:**
java.lang.Object
```
public class SignOptions
```

Позволяет указать параметры подписания документа.

 Чтобы узнать больше, посетите**Work with Digital Signatures** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getComments()](#getComments--) | Задает комментарии к цифровой подписи. |
| [getDecryptionPassword()](#getDecryptionPassword--) | Пароль для расшифровки исходного документа. |
| [getProviderId()](#getProviderId--) | Указывает идентификатор класса поставщика подписи. |
| [getSignTime()](#getSignTime--) | Дата подписания. |
| [getSignatureLineId()](#getSignatureLineId--) | Идентификатор строки подписи. |
| [getSignatureLineImage()](#getSignatureLineImage--) |  Изображение, которое будет отображаться в связанных[SignatureLine](../../com.aspose.words/signatureline). |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setComments(String value)](#setComments-java.lang.String-) | Задает комментарии к цифровой подписи. |
| [setDecryptionPassword(String value)](#setDecryptionPassword-java.lang.String-) | Пароль для расшифровки исходного документа. |
| [setProviderId(UUID value)](#setProviderId-java.util.UUID-) | Указывает идентификатор класса поставщика подписи. |
| [setSignTime(Date value)](#setSignTime-java.util.Date-) | Дата подписания. |
| [setSignatureLineId(UUID value)](#setSignatureLineId-java.util.UUID-) | Идентификатор строки подписи. |
| [setSignatureLineImage(byte[] value)](#setSignatureLineImage-byte---) |  Изображение, которое будет отображаться в связанных[SignatureLine](../../com.aspose.words/signatureline). |
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
### getComments() {#getComments--}
```
public String getComments()
```


 Задает комментарии к цифровой подписи. Значение по умолчанию**empty string**.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getDecryptionPassword() {#getDecryptionPassword--}
```
public String getDecryptionPassword()
```


 Пароль для расшифровки исходного документа. Значение по умолчанию**empty string**Если документ OOXML зашифрован, вы должны предоставить пароль для расшифровки исходного документа, прежде чем он будет подписан. Это не требуется для документов в двоичном формате DOC.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getProviderId() {#getProviderId--}
```
public UUID getProviderId()
```


 Указывает идентификатор класса поставщика подписи. Значение по умолчанию**Empty (all zeroes) Guid**.

 Поставщик криптографических услуг (CSP) — это независимый программный модуль, который фактически выполняет криптографические алгоритмы для аутентификации, кодирования и шифрования. MS Office резервирует стоимость\{00000000-0000-0000-0000-000000000000\} для поставщика подписи по умолчанию.

GUID дополнительно установленного провайдера следует получить из документации, поставляемой с провайдером.

Кроме того, все установленные криптографические провайдеры перечислены в реестре Windows. Его можно найти по следующему пути: HKLM\\ПРОГРАММНОГО ОБЕСПЕЧЕНИЯ\\Майкрософт\\Криптография\\По умолчанию\\Провайдер. Существует имя ключа «CP Service UUID», которое соответствует GUID поставщика подписи.

**Возвращает:**
java.util.UUID — соответствующее значение java.util.UUID.
### getSignTime() {#getSignTime--}
```
public Date getSignTime()
```


 Дата подписания. Значение по умолчанию**current time**.

**Возвращает:**
java.util.Date — соответствующее значение java.util.Date.
### getSignatureLineId() {#getSignatureLineId--}
```
public UUID getSignatureLineId()
```


 Идентификатор строки подписи. Значение по умолчанию**Empty (all zeroes) Guid** . Когда он установлен, он ассоциируется[SignatureLine](../../com.aspose.words/signatureline) с соответствующим[DigitalSignature](../../com.aspose.words/digitalsignature).

**Возвращает:**
java.util.UUID — соответствующее значение java.util.UUID.
### getSignatureLineImage() {#getSignatureLineImage--}
```
public byte[] getSignatureLineImage()
```


 Изображение, которое будет отображаться в связанных[SignatureLine](../../com.aspose.words/signatureline). Значение по умолчанию равно нулю.

**Возвращает:**
байт[] - соответствующий байт[] ценность.
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




### setComments(String value) {#setComments-java.lang.String-}
```
public void setComments(String value)
```


 Задает комментарии к цифровой подписи. Значение по умолчанию**empty string**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setDecryptionPassword(String value) {#setDecryptionPassword-java.lang.String-}
```
public void setDecryptionPassword(String value)
```


 Пароль для расшифровки исходного документа. Значение по умолчанию**empty string**Если документ OOXML зашифрован, вы должны предоставить пароль для расшифровки исходного документа, прежде чем он будет подписан. Это не требуется для документов в двоичном формате DOC.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setProviderId(UUID value) {#setProviderId-java.util.UUID-}
```
public void setProviderId(UUID value)
```


 Указывает идентификатор класса поставщика подписи. Значение по умолчанию**Empty (all zeroes) Guid**.

 Поставщик криптографических услуг (CSP) — это независимый программный модуль, который фактически выполняет криптографические алгоритмы для аутентификации, кодирования и шифрования. MS Office резервирует стоимость\{00000000-0000-0000-0000-000000000000\} для поставщика подписи по умолчанию.

GUID дополнительно установленного провайдера следует получить из документации, поставляемой с провайдером.

Кроме того, все установленные криптографические провайдеры перечислены в реестре Windows. Его можно найти по следующему пути: HKLM\\ПРОГРАММНОГО ОБЕСПЕЧЕНИЯ\\Майкрософт\\Криптография\\По умолчанию\\Провайдер. Существует имя ключа «CP Service UUID», которое соответствует GUID поставщика подписи.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.util.UUID | Соответствующее значение java.util.UUID. |

### setSignTime(Date value) {#setSignTime-java.util.Date-}
```
public void setSignTime(Date value)
```


 Дата подписания. Значение по умолчанию**current time**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.util.Date | Соответствующее значение java.util.Date. |

### setSignatureLineId(UUID value) {#setSignatureLineId-java.util.UUID-}
```
public void setSignatureLineId(UUID value)
```


 Идентификатор строки подписи. Значение по умолчанию**Empty (all zeroes) Guid** . Когда он установлен, он ассоциируется[SignatureLine](../../com.aspose.words/signatureline) с соответствующим[DigitalSignature](../../com.aspose.words/digitalsignature).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.util.UUID | Соответствующее значение java.util.UUID. |

### setSignatureLineImage(byte[] value) {#setSignatureLineImage-byte---}
```
public void setSignatureLineImage(byte[] value)
```


 Изображение, которое будет отображаться в связанных[SignatureLine](../../com.aspose.words/signatureline). Значение по умолчанию равно нулю.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | byte[] | Соответствующий байт[] ценность. |

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
