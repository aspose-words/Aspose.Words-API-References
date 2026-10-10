---
title: "SignerContext"
linktitle: "SignerContext"
second_title: "Aspose.Words لـ Java"
description: "سياق موقّع المستند في Java."
type: docs
weight: 623
url: /ar/java/com.aspose.words/signercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class SignerContext extends ProcessorContext
```

سياق موقّع المستند
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getCertificateHolder()](#getCertificateHolder) | كائن CertificateHolder مع الشهادة المستخدمة لتوقيع الملف. |
| [getFontSettings()](#getFontSettings) | إعدادات الخط المستخدمة بواسطة المعالج. |
| [getLayoutOptions()](#getLayoutOptions) | خيارات تخطيط المستند المستخدمة بواسطة المعالج. |
| [getSignOptions()](#getSignOptions) | كائن SignOptions مع خيارات توقيع متنوعة. |
| [getWarningCallback()](#getWarningCallback) | دالة رد النداء للتحذير المستخدمة بواسطة المعالج. |
| [setCertificateHolder(CertificateHolder value)](#setCertificateHolder-com.aspose.words.CertificateHolder) | كائن CertificateHolder مع الشهادة المستخدمة لتوقيع الملف. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | إعدادات الخط المستخدمة بواسطة المعالج. |
| [setSignOptions(SignOptions value)](#setSignOptions-com.aspose.words.SignOptions) | كائن SignOptions مع خيارات توقيع متنوعة. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | دالة رد النداء للتحذير المستخدمة بواسطة المعالج. |
### getCertificateHolder() {#getCertificateHolder}
```
public CertificateHolder getCertificateHolder()
```


كائن CertificateHolder مع الشهادة المستخدمة لتوقيع الملف.

 **Remarks:** 

يجب أن تحتوي الشهادة في الحامل على مفاتيح خاصة وأن يكون علم X509KeyStorageFlags.Exportable مُعيّنًا.

**Returns:**
[CertificateHolder](../../com.aspose.words/certificateholder/) - The corresponding [CertificateHolder](../../com.aspose.words/certificateholder/) value.
### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


إعدادات الخط المستخدمة بواسطة المعالج.

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getLayoutOptions() {#getLayoutOptions}
```
public LayoutOptions getLayoutOptions()
```


خيارات تخطيط المستند المستخدمة بواسطة المعالج.

**Returns:**
[LayoutOptions](../../com.aspose.words/layoutoptions/) - The corresponding [LayoutOptions](../../com.aspose.words/layoutoptions/) value.
### getSignOptions() {#getSignOptions}
```
public SignOptions getSignOptions()
```


كائن SignOptions مع خيارات توقيع متنوعة.

**Returns:**
[SignOptions](../../com.aspose.words/signoptions/) - The corresponding [SignOptions](../../com.aspose.words/signoptions/) value.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


دالة رد النداء للتحذير المستخدمة بواسطة المعالج.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setCertificateHolder(CertificateHolder value) {#setCertificateHolder-com.aspose.words.CertificateHolder}
```
public void setCertificateHolder(CertificateHolder value)
```


كائن CertificateHolder مع الشهادة المستخدمة لتوقيع الملف.

 **Remarks:** 

يجب أن تحتوي الشهادة في الحامل على مفاتيح خاصة وأن يكون علم X509KeyStorageFlags.Exportable مُعيّنًا.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [CertificateHolder](../../com.aspose.words/certificateholder/) | القيمة المقابلة لـ [CertificateHolder](../../com.aspose.words/certificateholder/). |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


إعدادات الخط المستخدمة بواسطة المعالج.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | القيمة المقابلة لـ [FontSettings](../../com.aspose.words/fontsettings/). |

### setSignOptions(SignOptions value) {#setSignOptions-com.aspose.words.SignOptions}
```
public void setSignOptions(SignOptions value)
```


كائن SignOptions مع خيارات توقيع متنوعة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [SignOptions](../../com.aspose.words/signoptions/) | القيمة المقابلة لـ [SignOptions](../../com.aspose.words/signoptions/). |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


دالة رد النداء للتحذير المستخدمة بواسطة المعالج.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | القيمة المقابلة لـ [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

