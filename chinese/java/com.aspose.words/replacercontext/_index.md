---
title: "ReplacerContext"
linktitle: "ReplacerContext"
second_title: "Aspose.Words for Java"
description: "Java 中的查找/替换操作上下文。"
type: docs
weight: 568
url: /zh/java/com.aspose.words/replacercontext/
---

**Inheritance:**
java.lang.Object，[com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class ReplacerContext extends ProcessorContext
```

查找/替换操作上下文。

 **Examples:** 

展示如何使用上下文在文档中替换字符串。

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

展示如何使用来自流的文档并使用上下文在文档中替换字符串。

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

展示如何使用上下文在文档中使用正则表达式替换字符串。

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

展示如何使用来自流的文档并使用上下文在文档中使用正则表达式替换字符串。

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
## 构造函数

| 构造函数 | 描述 |
| --- | --- |
| [ReplacerContext()](#ReplacerContext) | 初始化此类的新实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [getFindReplaceOptions()](#getFindReplaceOptions) | 查找/替换选项。 |
| [getFontSettings()](#getFontSettings) | 处理器使用的字体设置。 |
| [getLayoutOptions()](#getLayoutOptions) | 处理器使用的文档布局选项。 |
| [getWarningCallback()](#getWarningCallback) | 处理器使用的警告回调。 |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | 处理器使用的字体设置。 |
| [setReplacement(String pattern, String replacement)](#setReplacement-java.lang.String-java.lang.String) | 设置查找/替换操作使用的模式和替换内容。 |
| [setReplacement(Pattern pattern, String replacement)](#setReplacement-java.util.regex.Pattern-java.lang.String) | 设置查找/替换操作使用的模式和替换内容。 |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | 处理器使用的警告回调。 |
### ReplacerContext() {#ReplacerContext}
```
public ReplacerContext()
```


初始化此类的新实例。

### getFindReplaceOptions() {#getFindReplaceOptions}
```
public FindReplaceOptions getFindReplaceOptions()
```


查找/替换选项。

 **Examples:** 

展示如何使用上下文在文档中替换字符串。

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

展示如何使用来自流的文档并使用上下文在文档中替换字符串。

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

展示如何使用上下文在文档中使用正则表达式替换字符串。

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

展示如何使用来自流的文档并使用上下文在文档中使用正则表达式替换字符串。

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

### setReplacement(String pattern, String replacement) {#setReplacement-java.lang.String-java.lang.String}
```
public void setReplacement(String pattern, String replacement)
```


设置查找/替换操作使用的模式和替换内容。

 **Remarks:** 

使用此方法会覆盖先前设置的模式和替换内容。

 **Examples:** 

展示如何使用上下文在文档中替换字符串。

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

展示如何使用来自流的文档并使用上下文在文档中替换字符串。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 模式 | java.lang.String |  |
| 替换 | java.lang.String |  |

### setReplacement(Pattern pattern, String replacement) {#setReplacement-java.util.regex.Pattern-java.lang.String}
```
public void setReplacement(Pattern pattern, String replacement)
```


设置查找/替换操作使用的模式和替换内容。

 **Remarks:** 

使用此方法会覆盖先前设置的模式和替换内容。

 **Examples:** 

展示如何使用上下文在文档中使用正则表达式替换字符串。

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

展示如何使用来自流的文档并使用上下文在文档中使用正则表达式替换字符串。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 模式 | java.util.regex.Pattern |  |
| 替换 | java.lang.String |  |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


处理器使用的警告回调。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | 对应的[IWarningCallback](../../com.aspose.words/iwarningcallback/)值。 |

