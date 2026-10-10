---
title: "MergerContext"
linktitle: "MergerContext"
second_title: "Aspose.Words Java için"
description: "Java'da belge birleştirici bağlamı."
type: docs
weight: 466
url: /tr/java/com.aspose.words/mergercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class MergerContext extends ProcessorContext
```

Belge birleştirici bağlamı.

 **Examples:** 

Bağlamı kullanarak belgeleri tek bir çıktı belgesine birleştirmenin nasıl yapılacağını gösterir.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.1.docx")
         .execute();

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.create(mergerContext)
         .from(inputDoc1, firstLoadOptions)
         .from(inputDoc2, secondLoadOptions)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.2.docx", SaveFormat.DOCX)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.3.docx", saveOptions)
         .execute();
 
```

Bağlamı kullanarak akıştan belgeleri tek bir çıktı belgesine birleştirmenin nasıl yapılacağını gösterir.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 try (FileInputStream firstStreamIn = new FileInputStream(inputDoc1)) {
     try (FileInputStream secondStreamIn = new FileInputStream(inputDoc2)) {
         OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
         {
             saveOptions.setPassword("Aspose.Words");
         }
         try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MergeStreamContextDocuments.1.docx")) {
             Merger.create(mergerContext)
                     .from(firstStreamIn)
                     .from(secondStreamIn)
                     .to(streamOut, saveOptions)
                     .execute();
         }

         LoadOptions firstLoadOptions = new LoadOptions();
         {
             firstLoadOptions.setIgnoreOleData(true);
         }
         LoadOptions secondLoadOptions = new LoadOptions();
         {
             secondLoadOptions.setIgnoreOleData(false);
         }
         try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.MergeStreamContextDocuments.2.docx")) {
             Merger.create(mergerContext)
                     .from(firstStreamIn, firstLoadOptions)
                     .from(secondStreamIn, secondLoadOptions)
                     .to(streamOut1, SaveFormat.DOCX)
                     .execute();
         }
     }
 }
 
```
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getFontSettings()](#getFontSettings) | İşlemci tarafından kullanılan yazı tipi ayarları. |
| [getLayoutOptions()](#getLayoutOptions) | İşlemci tarafından kullanılan belge düzeni seçenekleri. |
| [getMergeFormatMode()](#getMergeFormatMode) | Çakışan biçimlendirmelerin nasıl birleştirileceğini belirtir. |
| [getWarningCallback()](#getWarningCallback) | İşlemci tarafından kullanılan uyarı geri çağırma. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | İşlemci tarafından kullanılan yazı tipi ayarları. |
| [setMergeFormatMode(int value)](#setMergeFormatMode-int) | Çakışan biçimlendirmelerin nasıl birleştirileceğini belirtir. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | İşlemci tarafından kullanılan uyarı geri çağırma. |
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
### getMergeFormatMode() {#getMergeFormatMode}
```
public int getMergeFormatMode()
```


Çakışan biçimlendirmelerin nasıl birleştirileceğini belirtir.

**Returns:**
int - İlgili  int  değeri. Döndürülen değer, [MergeFormatMode](../../com.aspose.words/mergeformatmode/) sabitlerinden biridir.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


İşlemci tarafından kullanılan uyarı geri çağırma.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


İşlemci tarafından kullanılan yazı tipi ayarları.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | İlgili [FontSettings](../../com.aspose.words/fontsettings/) değeri. |

### setMergeFormatMode(int value) {#setMergeFormatMode-int}
```
public void setMergeFormatMode(int value)
```


Çakışan biçimlendirmelerin nasıl birleştirileceğini belirtir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili  int  değeri. Değer, [MergeFormatMode](../../com.aspose.words/mergeformatmode/) sabitlerinden biri olmalıdır. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


İşlemci tarafından kullanılan uyarı geri çağırma.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | İlgili [IWarningCallback](../../com.aspose.words/iwarningcallback/) değeri. |

