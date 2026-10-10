---
title: "SignerContext"
linktitle: "SignerContext"
second_title: "Aspose.Words для Java"
description: "Контекст подписывающего документ в Java."
type: docs
weight: 623
url: /ru/java/com.aspose.words/signercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class SignerContext extends ProcessorContext
```

Контекст подписанта документа.
## Методы

| Метод | Описание |
| --- | --- |
| [getCertificateHolder()](#getCertificateHolder) | Объект CertificateHolder с сертификатом, используемым для подписи файла. |
| [getFontSettings()](#getFontSettings) | Настройки шрифтов, используемые процессором. |
| [getLayoutOptions()](#getLayoutOptions) | Параметры макета документа, используемые процессором. |
| [getSignOptions()](#getSignOptions) | Объект SignOptions с различными параметрами подписи. |
| [getWarningCallback()](#getWarningCallback) | Обратный вызов предупреждения, используемый процессором. |
| [setCertificateHolder(CertificateHolder value)](#setCertificateHolder-com.aspose.words.CertificateHolder) | Объект CertificateHolder с сертификатом, используемым для подписи файла. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Настройки шрифтов, используемые процессором. |
| [setSignOptions(SignOptions value)](#setSignOptions-com.aspose.words.SignOptions) | Объект SignOptions с различными параметрами подписи. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Обратный вызов предупреждения, используемый процессором. |
### getCertificateHolder() {#getCertificateHolder}
```
public CertificateHolder getCertificateHolder()
```


Объект CertificateHolder с сертификатом, используемым для подписи файла.

 **Remarks:** 

Сертификат в holder ДОЛЖЕН содержать закрытые ключи и иметь установленный флаг X509KeyStorageFlags.Exportable.

**Returns:**
[CertificateHolder](../../com.aspose.words/certificateholder/) - The corresponding [CertificateHolder](../../com.aspose.words/certificateholder/) value.
### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


Настройки шрифтов, используемые процессором.

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getLayoutOptions() {#getLayoutOptions}
```
public LayoutOptions getLayoutOptions()
```


Параметры макета документа, используемые процессором.

**Returns:**
[LayoutOptions](../../com.aspose.words/layoutoptions/) - The corresponding [LayoutOptions](../../com.aspose.words/layoutoptions/) value.
### getSignOptions() {#getSignOptions}
```
public SignOptions getSignOptions()
```


Объект SignOptions с различными параметрами подписи.

**Returns:**
[SignOptions](../../com.aspose.words/signoptions/) - The corresponding [SignOptions](../../com.aspose.words/signoptions/) value.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Обратный вызов предупреждения, используемый процессором.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setCertificateHolder(CertificateHolder value) {#setCertificateHolder-com.aspose.words.CertificateHolder}
```
public void setCertificateHolder(CertificateHolder value)
```


Объект CertificateHolder с сертификатом, используемым для подписи файла.

 **Remarks:** 

Сертификат в holder ДОЛЖЕН содержать закрытые ключи и иметь установленный флаг X509KeyStorageFlags.Exportable.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [CertificateHolder](../../com.aspose.words/certificateholder/) | Соответствующее значение [CertificateHolder](../../com.aspose.words/certificateholder/). |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


Настройки шрифтов, используемые процессором.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | Соответствующее значение [FontSettings](../../com.aspose.words/fontsettings/). |

### setSignOptions(SignOptions value) {#setSignOptions-com.aspose.words.SignOptions}
```
public void setSignOptions(SignOptions value)
```


Объект SignOptions с различными параметрами подписи.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [SignOptions](../../com.aspose.words/signoptions/) | Соответствующее значение [SignOptions](../../com.aspose.words/signoptions/). |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Обратный вызов предупреждения, используемый процессором.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | Соответствующее значение [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

