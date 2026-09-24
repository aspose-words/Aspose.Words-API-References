---
title: "ReplacerContext"
linktitle: "ReplacerContext"
second_title: "Aspose.Words Java için"
description: "Java'da bul/değiştir işlemi bağlamı."
type: docs
weight: 568
url: /tr/java/com.aspose.words/replacercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class ReplacerContext extends ProcessorContext
```

Bul/değiştir işlemi bağlamı.

 **Examples:** 

Bağlam kullanarak belgede dizeyi nasıl değiştireceğinizi gösterir.

```

 // There is a several ways to replace string in the document:
 String doc = getMyDir() + "Footer.docx";
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 ReplacerContext replacerContext = new ReplacerContext();
 replacerContext.setReplacement(pattern, replacement);
 replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

 Replacer.create(replacerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ReplaceContext.docx")
         .execute();
 
```

Akıştan gelen belgeleri kullanarak ve bağlamı kullanarak belgede dizeyi nasıl değiştireceğinizi gösterir.

```

 // There is a several ways to replace string in the document using documents from the stream:
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Footer.docx")) {
     ReplacerContext replacerContext = new ReplacerContext();
     replacerContext.setReplacement(pattern, replacement);
     replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ReplaceContextStream.docx")) {
         Replacer.create(replacerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

Bağlam kullanarak belgede dizeyi regex ile nasıl değiştireceğinizi gösterir.

```

 // There is a several ways to replace string with regex in the document:
 String doc = getMyDir() + "Footer.docx";
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 ReplacerContext replacerContext = new ReplacerContext();
 replacerContext.setReplacement(pattern, replacement);
 replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

 Replacer.create(replacerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ReplaceContextRegex.docx")
         .execute();
 
```

Akıştan gelen belgeleri kullanarak ve bağlamı kullanarak belgede dizeyi regex ile nasıl değiştireceğinizi gösterir.

```

 // There is a several ways to replace string with regex in the document using documents from the stream:
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Replace regex.docx")) {
     ReplacerContext replacerContext = new ReplacerContext();
     replacerContext.setReplacement(pattern, replacement);
     replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ReplaceContextStreamRegex.docx")) {
         Replacer.create(replacerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [ReplacerContext()](#ReplacerContext) | Bu sınıfın yeni bir örneğini başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getFindReplaceOptions()](#getFindReplaceOptions) | Bul/değiştir seçenekleri. |
| [getFontSettings()](#getFontSettings) | İşlemci tarafından kullanılan yazı tipi ayarları. |
| [getLayoutOptions()](#getLayoutOptions) | İşlemci tarafından kullanılan belge düzeni seçenekleri. |
| [getWarningCallback()](#getWarningCallback) | İşlemci tarafından kullanılan uyarı geri çağırma. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | İşlemci tarafından kullanılan yazı tipi ayarları. |
| [setReplacement(String pattern, String replacement)](#setReplacement-java.lang.String-java.lang.String) | Bul/değiştir işlemi tarafından kullanılan desen ve değiştirme değerini ayarlar. |
| [setReplacement(Pattern pattern, String replacement)](#setReplacement-java.util.regex.Pattern-java.lang.String) | Bul/değiştir işlemi tarafından kullanılan desen ve değiştirme değerini ayarlar. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | İşlemci tarafından kullanılan uyarı geri çağırma. |
### ReplacerContext() {#ReplacerContext}
```
public ReplacerContext()
```


Bu sınıfın yeni bir örneğini başlatır.

### getFindReplaceOptions() {#getFindReplaceOptions}
```
public FindReplaceOptions getFindReplaceOptions()
```


Bul/değiştir seçenekleri.

 **Examples:** 

Bağlam kullanarak belgede dizeyi nasıl değiştireceğinizi gösterir.

```

 // There is a several ways to replace string in the document:
 String doc = getMyDir() + "Footer.docx";
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 ReplacerContext replacerContext = new ReplacerContext();
 replacerContext.setReplacement(pattern, replacement);
 replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

 Replacer.create(replacerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ReplaceContext.docx")
         .execute();
 
```

Akıştan gelen belgeleri kullanarak ve bağlamı kullanarak belgede dizeyi nasıl değiştireceğinizi gösterir.

```

 // There is a several ways to replace string in the document using documents from the stream:
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Footer.docx")) {
     ReplacerContext replacerContext = new ReplacerContext();
     replacerContext.setReplacement(pattern, replacement);
     replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ReplaceContextStream.docx")) {
         Replacer.create(replacerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

Bağlam kullanarak belgede dizeyi regex ile nasıl değiştireceğinizi gösterir.

```

 // There is a several ways to replace string with regex in the document:
 String doc = getMyDir() + "Footer.docx";
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 ReplacerContext replacerContext = new ReplacerContext();
 replacerContext.setReplacement(pattern, replacement);
 replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

 Replacer.create(replacerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ReplaceContextRegex.docx")
         .execute();
 
```

Akıştan gelen belgeleri kullanarak ve bağlamı kullanarak belgede dizeyi regex ile nasıl değiştireceğinizi gösterir.

```

 // There is a several ways to replace string with regex in the document using documents from the stream:
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Replace regex.docx")) {
     ReplacerContext replacerContext = new ReplacerContext();
     replacerContext.setReplacement(pattern, replacement);
     replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ReplaceContextStreamRegex.docx")) {
         Replacer.create(replacerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Returns:**
[FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) - The corresponding [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) value.
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
### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


İşlemci tarafından kullanılan yazı tipi ayarları.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | İlgili [FontSettings](../../com.aspose.words/fontsettings/) değeri. |

### setReplacement(String pattern, String replacement) {#setReplacement-java.lang.String-java.lang.String}
```
public void setReplacement(String pattern, String replacement)
```


Bul/değiştir işlemi tarafından kullanılan desen ve değiştirme değerini ayarlar.

 **Remarks:** 

Bu yöntemi kullanmak, daha önce ayarlanmış deseni ve değiştirmeyi geçersiz kılar.

 **Examples:** 

Bağlam kullanarak belgede dizeyi nasıl değiştireceğinizi gösterir.

```

 // There is a several ways to replace string in the document:
 String doc = getMyDir() + "Footer.docx";
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 ReplacerContext replacerContext = new ReplacerContext();
 replacerContext.setReplacement(pattern, replacement);
 replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

 Replacer.create(replacerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ReplaceContext.docx")
         .execute();
 
```

Akıştan gelen belgeleri kullanarak ve bağlamı kullanarak belgede dizeyi nasıl değiştireceğinizi gösterir.

```

 // There is a several ways to replace string in the document using documents from the stream:
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Footer.docx")) {
     ReplacerContext replacerContext = new ReplacerContext();
     replacerContext.setReplacement(pattern, replacement);
     replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ReplaceContextStream.docx")) {
         Replacer.create(replacerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| desen | java.lang.String |  |
| değiştirme | java.lang.String |  |

### setReplacement(Pattern pattern, String replacement) {#setReplacement-java.util.regex.Pattern-java.lang.String}
```
public void setReplacement(Pattern pattern, String replacement)
```


Bul/değiştir işlemi tarafından kullanılan desen ve değiştirme değerini ayarlar.

 **Remarks:** 

Bu yöntemi kullanmak, daha önce ayarlanmış deseni ve değiştirmeyi geçersiz kılar.

 **Examples:** 

Bağlam kullanarak belgede dizeyi regex ile nasıl değiştireceğinizi gösterir.

```

 // There is a several ways to replace string with regex in the document:
 String doc = getMyDir() + "Footer.docx";
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 ReplacerContext replacerContext = new ReplacerContext();
 replacerContext.setReplacement(pattern, replacement);
 replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

 Replacer.create(replacerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ReplaceContextRegex.docx")
         .execute();
 
```

Akıştan gelen belgeleri kullanarak ve bağlamı kullanarak belgede dizeyi regex ile nasıl değiştireceğinizi gösterir.

```

 // There is a several ways to replace string with regex in the document using documents from the stream:
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Replace regex.docx")) {
     ReplacerContext replacerContext = new ReplacerContext();
     replacerContext.setReplacement(pattern, replacement);
     replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ReplaceContextStreamRegex.docx")) {
         Replacer.create(replacerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| desen | java.util.regex.Pattern |  |
| değiştirme | java.lang.String |  |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


İşlemci tarafından kullanılan uyarı geri çağırma.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | İlgili [IWarningCallback](../../com.aspose.words/iwarningcallback/) değeri. |

