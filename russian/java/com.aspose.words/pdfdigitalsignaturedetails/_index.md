---
title: PdfDigitalSignatureDetails
second_title: Справочник по API Aspose.Words для Java
description: Содержит сведения о подписании документа PDF цифровой подписью.
type: docs
weight: 451
url: /ru/java/com.aspose.words/pdfdigitalsignaturedetails/
---

**Наследование:**
java.lang.Object
```
public class PdfDigitalSignatureDetails
```

Содержит сведения о подписании документа PDF цифровой подписью.

В настоящее время цифровая подпись PDF-документов доступна только в .NET 2.0 или более поздней версии.

 Чтобы подписать PDF-документ цифровой подписью при его создании с помощью Aspose.Words, установите[PdfSaveOptions.getDigitalSignatureDetails()](../../com.aspose.words/pdfsaveoptions\#getDigitalSignatureDetails--) / [PdfSaveOptions.setDigitalSignatureDetails(com.aspose.words.PdfDigitalSignatureDetails)](../../com.aspose.words/pdfsaveoptions\#setDigitalSignatureDetails-com.aspose.words.PdfDigitalSignatureDetails-)собственность на действительный[PdfDigitalSignatureDetails](../../com.aspose.words/pdfdigitalsignaturedetails) объект, а затем сохраните документ в формате PDF, передав[PdfSaveOptions](../../com.aspose.words/pdfsaveoptions) как параметр в[Document.save(java.lang.String, com.aspose.words.SaveOptions)](../../com.aspose.words/document\#save-java.lang.String--com.aspose.words.SaveOptions-) метод.

Aspose.Words создает PKCS\Подпись #7 по всему документу PDF и использует фильтр «Adobe.PPKMS» и подфильтр «adbe.pkcs7.sha1» при создании цифровой подписи.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [PdfDigitalSignatureDetails()](#PdfDigitalSignatureDetails--) | Инициализирует экземпляр этого класса. |
| [PdfDigitalSignatureDetails(CertificateHolder certificateHolder, String reason, String location, Date signatureDate)](#PdfDigitalSignatureDetails-com.aspose.words.CertificateHolder-java.lang.String-java.lang.String-java.util.Date-) | Инициализирует экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getCertificateHolder()](#getCertificateHolder--) | Возвращает объект держателя сертификата, содержащий сертификат, который использовался для подписи документа. |
| [getClass()](#getClass--) |  |
| [getHashAlgorithm()](#getHashAlgorithm--) | Получает алгоритм хеширования. |
| [getLocation()](#getLocation--) | Получает расположение подписи. |
| [getReason()](#getReason--) | Получает причину подписания. |
| [getSignatureDate()](#getSignatureDate--) | Получает дату подписания. |
| [getTimestampSettings()](#getTimestampSettings--) | Получает настройки временной метки цифровой подписи. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setCertificateHolder(CertificateHolder value)](#setCertificateHolder-com.aspose.words.CertificateHolder-) | Возвращает объект держателя сертификата, содержащий сертификат, который использовался для подписи документа. |
| [setHashAlgorithm(int value)](#setHashAlgorithm-int-) | Устанавливает алгоритм хеширования. |
| [setLocation(String value)](#setLocation-java.lang.String-) | Устанавливает место подписи. |
| [setReason(String value)](#setReason-java.lang.String-) | Устанавливает причину подписания. |
| [setSignatureDate(Date value)](#setSignatureDate-java.util.Date-) | Устанавливает дату подписания. |
| [setTimestampSettings(PdfDigitalSignatureTimestampSettings value)](#setTimestampSettings-com.aspose.words.PdfDigitalSignatureTimestampSettings-) | Задает параметры временной метки цифровой подписи. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### PdfDigitalSignatureDetails() {#PdfDigitalSignatureDetails--}
```
public PdfDigitalSignatureDetails()
```


Инициализирует экземпляр этого класса.

### PdfDigitalSignatureDetails(CertificateHolder certificateHolder, String reason, String location, Date signatureDate) {#PdfDigitalSignatureDetails-com.aspose.words.CertificateHolder-java.lang.String-java.lang.String-java.util.Date-}
```
public PdfDigitalSignatureDetails(CertificateHolder certificateHolder, String reason, String location, Date signatureDate)
```


Инициализирует экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| certificateHolder | [CertificateHolder](../../com.aspose.words/certificateholder) | Держатель сертификата, который содержит сам сертификат. |
| reason | java.lang.String | Причина подписания. |
| location | java.lang.String | Место подписания. |
| signatureDate | java.util.Date | Дата и время подписания. |

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
### getCertificateHolder() {#getCertificateHolder--}
```
public CertificateHolder getCertificateHolder()
```


Возвращает объект держателя сертификата, содержащий сертификат, который использовался для подписи документа.

**Возвращает:**
[CertificateHolder](../../com.aspose.words/certificateholder) - Объект держателя сертификата, содержащий сертификат, использовался для подписи документа.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getHashAlgorithm() {#getHashAlgorithm--}
```
public int getHashAlgorithm()
```


Получает алгоритм хеширования. Значение по умолчанию — алгоритм SHA-256.

**Возвращает:**
int - Алгоритм хеширования. Возвращаемое значение является одним из[PdfDigitalSignatureHashAlgorithm](../../com.aspose.words/pdfdigitalsignaturehashalgorithm) константы.
### getLocation() {#getLocation--}
```
public String getLocation()
```


Получает расположение подписи. Значение по умолчанию равно нулю.

**Возвращает:**
java.lang.String — расположение подписи.
### getReason() {#getReason--}
```
public String getReason()
```


Получает причину подписания. Значение по умолчанию равно нулю.

**Возвращает:**
java.lang.String — Причина подписания.
### getSignatureDate() {#getSignatureDate--}
```
public Date getSignatureDate()
```


Получает дату подписания.

Значение по умолчанию — текущее время.

Это значение появится в цифровой подписи как непроверенное компьютерное время.

**Возвращает:**
java.util.Date - Дата подписания.
### getTimestampSettings() {#getTimestampSettings--}
```
public PdfDigitalSignatureTimestampSettings getTimestampSettings()
```


Получает настройки временной метки цифровой подписи.

 Значение по умолчанию равно null, и цифровая подпись не будет иметь отметку времени. Когда для этого свойства задано допустимое значение[PdfDigitalSignatureTimestampSettings](../../com.aspose.words/pdfdigitalsignaturetimestampsettings) объекта, то цифровая подпись в документе PDF будет иметь отметку времени.

**Возвращает:**
[PdfDigitalSignatureTimestampSettings](../../com.aspose.words/pdfdigitalsignaturetimestampsettings) - Настройки временной метки цифровой подписи.
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




### setCertificateHolder(CertificateHolder value) {#setCertificateHolder-com.aspose.words.CertificateHolder-}
```
public void setCertificateHolder(CertificateHolder value)
```


Возвращает объект держателя сертификата, содержащий сертификат, который использовался для подписи документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [CertificateHolder](../../com.aspose.words/certificateholder) | Объект держателя сертификата, содержащий сертификат, использовался для подписи документа. |

### setHashAlgorithm(int value) {#setHashAlgorithm-int-}
```
public void setHashAlgorithm(int value)
```


Устанавливает алгоритм хеширования. Значение по умолчанию — алгоритм SHA-256.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Алгоритм хеширования. Значение должно быть одним из[PdfDigitalSignatureHashAlgorithm](../../com.aspose.words/pdfdigitalsignaturehashalgorithm) константы. |

### setLocation(String value) {#setLocation-java.lang.String-}
```
public void setLocation(String value)
```


Устанавливает место подписи. Значение по умолчанию равно нулю.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Место подписания. |

### setReason(String value) {#setReason-java.lang.String-}
```
public void setReason(String value)
```


Устанавливает причину подписания. Значение по умолчанию равно нулю.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Причина подписания. |

### setSignatureDate(Date value) {#setSignatureDate-java.util.Date-}
```
public void setSignatureDate(Date value)
```


Устанавливает дату подписания.

Значение по умолчанию — текущее время.

Это значение появится в цифровой подписи как непроверенное компьютерное время.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.util.Date | Дата подписания. |

### setTimestampSettings(PdfDigitalSignatureTimestampSettings value) {#setTimestampSettings-com.aspose.words.PdfDigitalSignatureTimestampSettings-}
```
public void setTimestampSettings(PdfDigitalSignatureTimestampSettings value)
```


Задает параметры временной метки цифровой подписи.

 Значение по умолчанию равно null, и цифровая подпись не будет иметь отметку времени. Когда для этого свойства задано допустимое значение[PdfDigitalSignatureTimestampSettings](../../com.aspose.words/pdfdigitalsignaturetimestampsettings) объекта, то цифровая подпись в документе PDF будет иметь отметку времени.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [PdfDigitalSignatureTimestampSettings](../../com.aspose.words/pdfdigitalsignaturetimestampsettings) | Параметры временной метки цифровой подписи. |

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
