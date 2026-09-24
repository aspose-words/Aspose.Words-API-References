---
title: "ComparerContext"
linktitle: "ComparerContext"
second_title: "Aspose.Words Java için"
description: "Java'da belge karşılaştırıcı bağlamı."
type: docs
weight: 115
url: /tr/java/com.aspose.words/comparercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class ComparerContext extends ProcessorContext
```

Belge karşılaştırıcı bağlamı

 **Examples:** 

Bağlam kullanarak belgeleri basitçe karşılaştırmanın nasıl yapılacağını gösterir.

```

 // There is a several ways to compare documents:
 String firstDoc = getMyDir() + "Table column bookmarks.docx";
 String secondDoc = getMyDir() + "Table column bookmarks.doc";

 ComparerContext comparerContext = new ComparerContext();
 comparerContext.getCompareOptions().setIgnoreCaseChanges(true);
 comparerContext.setAuthor("Author");
 comparerContext.setDateTime(new Date());

 Comparer.create(comparerContext)
         .from(firstDoc)
         .from(secondDoc)
         .to(getArtifactsDir() + "LowCode.CompareContextDocuments.docx")
         .execute();
 
```

Bağlam kullanarak akıştan belgeleri karşılaştırmanın nasıl yapılacağını gösterir.

```

 // There is a several ways to compare documents from the stream:
 try (FileInputStream firstStreamIn = new FileInputStream(getMyDir() + "Table column bookmarks.docx")) {
     try (FileInputStream secondStreamIn = new FileInputStream(getMyDir() + "Table column bookmarks.doc")) {
         ComparerContext comparerContext = new ComparerContext();
         comparerContext.getCompareOptions().setIgnoreCaseChanges(true);
         comparerContext.setAuthor("Author");
         comparerContext.setDateTime(new Date());

         try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.CompareContextStreamDocuments.docx")) {
             Comparer.create(comparerContext)
                     .from(firstStreamIn)
                     .from(secondStreamIn)
                     .to(streamOut, SaveFormat.DOCX)
                     .execute();
         }
     }
 }
 
```
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [ComparerContext()](#ComparerContext) | Bu sınıfın yeni bir örneğini başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getAcceptRevisions()](#getAcceptRevisions) | Belgeleri karşılaştırmadan önce revizyonların kabul edilip edilmeyeceğini gösterir. |
| [getAuthor()](#getAuthor) | Belge karşılaştırması sırasında oluşturulan revizyonlara atanacak yazar. |
| [getCompareOptions()](#getCompareOptions) | Belgeler karşılaştırılırken kullanılan seçenekler. |
| [getDateTime()](#getDateTime) | Belge karşılaştırması sırasında oluşturulan revizyonlara atanan tarih ve saat. |
| [getFontSettings()](#getFontSettings) | İşlemci tarafından kullanılan yazı tipi ayarları. |
| [getLayoutOptions()](#getLayoutOptions) | İşlemci tarafından kullanılan belge düzeni seçenekleri. |
| [getWarningCallback()](#getWarningCallback) | İşlemci tarafından kullanılan uyarı geri çağırma. |
| [setAcceptRevisions(boolean value)](#setAcceptRevisions-boolean) | Belgeleri karşılaştırmadan önce revizyonların kabul edilip edilmeyeceğini gösterir. |
| [setAuthor(String value)](#setAuthor-java.lang.String) | Belge karşılaştırması sırasında oluşturulan revizyonlara atanacak yazar. |
| [setDateTime(Date value)](#setDateTime-java.util.Date) | Belge karşılaştırması sırasında oluşturulan revizyonlara atanan tarih ve saat. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | İşlemci tarafından kullanılan yazı tipi ayarları. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | İşlemci tarafından kullanılan uyarı geri çağırma. |
### ComparerContext() {#ComparerContext}
```
public ComparerContext()
```


Bu sınıfın yeni bir örneğini başlatır.

### getAcceptRevisions() {#getAcceptRevisions}
```
public boolean getAcceptRevisions()
```


Belgeleri karşılaştırmadan önce revizyonların kabul edilip edilmeyeceğini gösterir. Karşılaştırılan belgeler revizyon içeriyorsa ve bu bayrak false olarak ayarlanmışsa, işlemci revizyonları reddeder. Varsayılan değer true'tir.

**Returns:**
boolean - İlgili  boolean  değeri.
### getAuthor() {#getAuthor}
```
public String getAuthor()
```


Belge karşılaştırması sırasında oluşturulan revizyonlara atanacak yazar.

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getCompareOptions() {#getCompareOptions}
```
public CompareOptions getCompareOptions()
```


Belgeler karşılaştırılırken kullanılan seçenekler.

 **Examples:** 

Bağlam kullanarak belgeleri basitçe karşılaştırmanın nasıl yapılacağını gösterir.

```

 // There is a several ways to compare documents:
 String firstDoc = getMyDir() + "Table column bookmarks.docx";
 String secondDoc = getMyDir() + "Table column bookmarks.doc";

 ComparerContext comparerContext = new ComparerContext();
 comparerContext.getCompareOptions().setIgnoreCaseChanges(true);
 comparerContext.setAuthor("Author");
 comparerContext.setDateTime(new Date());

 Comparer.create(comparerContext)
         .from(firstDoc)
         .from(secondDoc)
         .to(getArtifactsDir() + "LowCode.CompareContextDocuments.docx")
         .execute();
 
```

Bağlam kullanarak akıştan belgeleri karşılaştırmanın nasıl yapılacağını gösterir.

```

 // There is a several ways to compare documents from the stream:
 try (FileInputStream firstStreamIn = new FileInputStream(getMyDir() + "Table column bookmarks.docx")) {
     try (FileInputStream secondStreamIn = new FileInputStream(getMyDir() + "Table column bookmarks.doc")) {
         ComparerContext comparerContext = new ComparerContext();
         comparerContext.getCompareOptions().setIgnoreCaseChanges(true);
         comparerContext.setAuthor("Author");
         comparerContext.setDateTime(new Date());

         try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.CompareContextStreamDocuments.docx")) {
             Comparer.create(comparerContext)
                     .from(firstStreamIn)
                     .from(secondStreamIn)
                     .to(streamOut, SaveFormat.DOCX)
                     .execute();
         }
     }
 }
 
```

**Returns:**
[CompareOptions](../../com.aspose.words/compareoptions/) - The corresponding [CompareOptions](../../com.aspose.words/compareoptions/) value.
### getDateTime() {#getDateTime}
```
public Date getDateTime()
```


Belge karşılaştırması sırasında oluşturulan revizyonlara atanan tarih ve saat.

**Returns:**
java.util.Date - İlgili java.util.Date değeri.
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
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


İşlemci tarafından kullanılan uyarı geri çağırma.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setAcceptRevisions(boolean value) {#setAcceptRevisions-boolean}
```
public void setAcceptRevisions(boolean value)
```


Belgeleri karşılaştırmadan önce revizyonların kabul edilip edilmeyeceğini gösterir. Karşılaştırılan belgeler revizyon içeriyorsa ve bu bayrak false olarak ayarlanmışsa, işlemci revizyonları reddeder. Varsayılan değer true'tir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setAuthor(String value) {#setAuthor-java.lang.String}
```
public void setAuthor(String value)
```


Belge karşılaştırması sırasında oluşturulan revizyonlara atanacak yazar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setDateTime(Date value) {#setDateTime-java.util.Date}
```
public void setDateTime(Date value)
```


Belge karşılaştırması sırasında oluşturulan revizyonlara atanan tarih ve saat.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.util.Date | İlgili java.util.Date değeri. |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


İşlemci tarafından kullanılan yazı tipi ayarları.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | İlgili [FontSettings](../../com.aspose.words/fontsettings/) değeri. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


İşlemci tarafından kullanılan uyarı geri çağırma.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | İlgili [IWarningCallback](../../com.aspose.words/iwarningcallback/) değeri. |

