---
title: "SignerContext"
linktitle: "SignerContext"
second_title: "Aspose.Words Java için"
description: "Java'da belge imzalayan bağlamı."
type: docs
weight: 623
url: /tr/java/com.aspose.words/signercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class SignerContext extends ProcessorContext
```

Belge imzalayan bağlamı
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getCertificateHolder()](#getCertificateHolder) | Dosyayı imzalamak için kullanılan sertifikaya sahip CertificateHolder nesnesi. |
| [getFontSettings()](#getFontSettings) | İşlemci tarafından kullanılan yazı tipi ayarları. |
| [getLayoutOptions()](#getLayoutOptions) | İşlemci tarafından kullanılan belge düzeni seçenekleri. |
| [getSignOptions()](#getSignOptions) | Çeşitli imzalama seçeneklerine sahip SignOptions nesnesi. |
| [getWarningCallback()](#getWarningCallback) | İşlemci tarafından kullanılan uyarı geri çağırma. |
| [setCertificateHolder(CertificateHolder value)](#setCertificateHolder-com.aspose.words.CertificateHolder) | Dosyayı imzalamak için kullanılan sertifikaya sahip CertificateHolder nesnesi. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | İşlemci tarafından kullanılan yazı tipi ayarları. |
| [setSignOptions(SignOptions value)](#setSignOptions-com.aspose.words.SignOptions) | Çeşitli imzalama seçeneklerine sahip SignOptions nesnesi. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | İşlemci tarafından kullanılan uyarı geri çağırma. |
### getCertificateHolder() {#getCertificateHolder}
```
public CertificateHolder getCertificateHolder()
```


Dosyayı imzalamak için kullanılan sertifikaya sahip CertificateHolder nesnesi.

 **Remarks:** 

Holder içindeki sertifika, özel anahtarlar içermeli ve X509KeyStorageFlags.Exportable bayrağı ayarlanmış olmalıdır.

**Returns:**
[CertificateHolder](../../com.aspose.words/certificateholder/) - The corresponding [CertificateHolder](../../com.aspose.words/certificateholder/) value.
### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


İşlemci tarafından kullanılan yazı tipi ayarları.

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getLayoutOptions() {#getLayoutOptions}
```
public LayoutOptions getLayoutOptions()
```


İşlemci tarafından kullanılan belge düzeni seçenekleri.

**Returns:**
[LayoutOptions](../../com.aspose.words/layoutoptions/) - The corresponding [LayoutOptions](../../com.aspose.words/layoutoptions/) value.
### getSignOptions() {#getSignOptions}
```
public SignOptions getSignOptions()
```


Çeşitli imzalama seçeneklerine sahip SignOptions nesnesi.

**Returns:**
[SignOptions](../../com.aspose.words/signoptions/) - The corresponding [SignOptions](../../com.aspose.words/signoptions/) value.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


İşlemci tarafından kullanılan uyarı geri çağırma.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setCertificateHolder(CertificateHolder value) {#setCertificateHolder-com.aspose.words.CertificateHolder}
```
public void setCertificateHolder(CertificateHolder value)
```


Dosyayı imzalamak için kullanılan sertifikaya sahip CertificateHolder nesnesi.

 **Remarks:** 

Holder içindeki sertifika, özel anahtarlar içermeli ve X509KeyStorageFlags.Exportable bayrağı ayarlanmış olmalıdır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [CertificateHolder](../../com.aspose.words/certificateholder/) | İlgili [CertificateHolder](../../com.aspose.words/certificateholder/) değeri. |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


İşlemci tarafından kullanılan yazı tipi ayarları.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | İlgili [FontSettings](../../com.aspose.words/fontsettings/) değeri. |

### setSignOptions(SignOptions value) {#setSignOptions-com.aspose.words.SignOptions}
```
public void setSignOptions(SignOptions value)
```


Çeşitli imzalama seçeneklerine sahip SignOptions nesnesi.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [SignOptions](../../com.aspose.words/signoptions/) | İlgili [SignOptions](../../com.aspose.words/signoptions/) değeri. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


İşlemci tarafından kullanılan uyarı geri çağırma.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | İlgili [IWarningCallback](../../com.aspose.words/iwarningcallback/) değeri. |

