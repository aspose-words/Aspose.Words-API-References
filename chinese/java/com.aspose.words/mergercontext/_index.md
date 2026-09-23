---
title: "MergerContext"
linktitle: "MergerContext"
second_title: "Aspose.Words for Java"
description: "Java 中的文档合并上下文。"
type: docs
weight: 466
url: /zh/java/com.aspose.words/mergercontext/
---

**Inheritance:**
java.lang.Object，[com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class MergerContext extends ProcessorContext
```

文档合并上下文。

 **Examples:** 

展示如何在上下文中将文档合并为单个输出文档。

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

展示如何在上下文中将来自流的文档合并为单个输出文档。

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
## 方法

| 方法 | 描述 |
| --- | --- |
| [getFontSettings()](#getFontSettings) | 处理器使用的字体设置。 |
| [getLayoutOptions()](#getLayoutOptions) | 处理器使用的文档布局选项。 |
| [getMergeFormatMode()](#getMergeFormatMode) | 指定如何合并冲突的格式。 |
| [getWarningCallback()](#getWarningCallback) | 处理器使用的警告回调。 |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | 处理器使用的字体设置。 |
| [setMergeFormatMode(int value)](#setMergeFormatMode-int) | 指定如何合并冲突的格式。 |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | 处理器使用的警告回调。 |
### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


处理器使用的字体设置。

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getLayoutOptions() {#getLayoutOptions}
```
public LayoutOptions getLayoutOptions()
```


处理器使用的文档布局选项。

**Returns:**
[LayoutOptions](../../com.aspose.words/layoutoptions/) - The corresponding [LayoutOptions](../../com.aspose.words/layoutoptions/) value.
### getMergeFormatMode() {#getMergeFormatMode}
```
public int getMergeFormatMode()
```


指定如何合并冲突的格式。

**Returns:**
int - 对应的 int 值。返回值是 [MergeFormatMode](../../com.aspose.words/mergeformatmode/) 常量之一。
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


处理器使用的警告回调。

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


处理器使用的字体设置。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | 对应的[FontSettings](../../com.aspose.words/fontsettings/)值。 |

### setMergeFormatMode(int value) {#setMergeFormatMode-int}
```
public void setMergeFormatMode(int value)
```


指定如何合并冲突的格式。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是 [MergeFormatMode](../../com.aspose.words/mergeformatmode/) 常量之一。 |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


处理器使用的警告回调。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | 对应的[IWarningCallback](../../com.aspose.words/iwarningcallback/)值。 |

