---
title: "ConverterContext"
linktitle: "ConverterContext"
second_title: "Aspose.Words لـ Java"
description: "سياق محول المستند في جافا."
type: docs
weight: 133
url: /ar/java/com.aspose.words/convertercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class ConverterContext extends ProcessorContext
```

سياق محول المستند

 **Examples:** 

يعرض كيفية تحويل المستندات بسطر واحد من الشيفرة باستخدام السياق.

```

 String doc = getMyDir() + "Big document.docx";

 ConverterContext converterContext = new ConverterContext();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.1.pdf")
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.2.pdf", SaveFormat.RTF)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.create(converterContext)
         .from(doc, loadOptions)
         .to(getArtifactsDir() + "LowCode.ConvertContext.3.docx", saveOptions)
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.PNG))
         .execute();
 
```

يعرض كيفية تحويل المستندات من الدفق بسطر واحد من الشيفرة باستخدام السياق.

```

 String doc = getMyDir() + "Document.docx";
 ConverterContext converterContext = new ConverterContext();

 try (FileInputStream streamIn = new FileInputStream(doc)) {
     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ConvertContextStream.1.docx")) {
         Converter.create(converterContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.RTF)
                 .execute();
     }

     OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
     {
         saveOptions.setPassword("Aspose.Words");
     }
     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setIgnoreOleData(true);
     }
     try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.ConvertContextStream.2.docx")) {
         Converter.create(converterContext)
                 .from(streamIn, loadOptions)
                 .to(streamOut1, saveOptions)
                 .execute();
     }
 }
 
```
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getFontSettings()](#getFontSettings) | إعدادات الخط المستخدمة بواسطة المعالج. |
| [getLayoutOptions()](#getLayoutOptions) | خيارات تخطيط المستند المستخدمة بواسطة المعالج. |
| [getWarningCallback()](#getWarningCallback) | دالة رد النداء للتحذير المستخدمة بواسطة المعالج. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | إعدادات الخط المستخدمة بواسطة المعالج. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | دالة رد النداء للتحذير المستخدمة بواسطة المعالج. |
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
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


دالة رد النداء للتحذير المستخدمة بواسطة المعالج.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


إعدادات الخط المستخدمة بواسطة المعالج.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | القيمة المقابلة لـ [FontSettings](../../com.aspose.words/fontsettings/). |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


دالة رد النداء للتحذير المستخدمة بواسطة المعالج.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | القيمة المقابلة لـ [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

