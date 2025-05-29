---
title: Replacer.Replace
linktitle: Replace
articleTitle: Replace
second_title: Aspose.Words for .NET
description: 使用 Replacer Replace 方法轻松替换输入文件中所有特定字符串。立即简化您的文本编辑！
type: docs
weight: 20
url: /zh/net/aspose.words.lowcode/replacer/replace/
---
## Replace(*string, string, string, string*) {#replace_8}

用替换字符串替换输入文件中所有出现的指定字符串模式。

```csharp
public static int Replace(string inputFileName, string outputFileName, string pattern, 
    string replacement)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |
| pattern | String | 要替换的字符串。 |
| replacement | String | 用于替换所有出现的模式的字符串。 |

### 返回值

已进行的替换次数。

## 评论

如果输出格式为图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则输出的每一页都将保存为单独的文件。指定的输出文件名将用于生成每个部分的文件名，并遵循以下规则：outputFile_partIndex.extension。

如果输出格式为 TIFF，则输出将保存为单个多帧 TIFF 文件。

## 例子

展示如何替换文档中的字符串。

```csharp
// 有几种方法可以替换文档中的字符串：
string doc = MyDir + "Footer.docx";
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

FindReplaceOptions options = new FindReplaceOptions();
options.FindWholeWordsOnly = false;
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.1.docx", pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.2.docx", SaveFormat.Docx, pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.3.docx", SaveFormat.Docx, pattern, replacement, options);
```

### 也可以看看

* class [Replacer](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Replace(*string, string, [SaveFormat](../../../aspose.words/saveformat/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_4}

使用指定的保存格式和附加选项，用替换字符串替换输入文件中所有出现的指定字符串模式。

```csharp
public static int Replace(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |
| saveFormat | SaveFormat | 保存格式。 |
| pattern | String | 要替换的字符串。 |
| replacement | String | 用于替换所有出现的模式的字符串。 |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/)对象来指定附加选项。 |

### 返回值

已进行的替换次数。

## 评论

如果输出格式为图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则输出的每一页都将保存为单独的文件。指定的输出文件名将用于生成每个部分的文件名，并遵循以下规则：outputFile_partIndex.extension。

如果输出格式为 TIFF，则输出将保存为单个多帧 TIFF 文件。

## 例子

展示如何替换文档中的字符串。

```csharp
// 有几种方法可以替换文档中的字符串：
string doc = MyDir + "Footer.docx";
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

FindReplaceOptions options = new FindReplaceOptions();
options.FindWholeWordsOnly = false;
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.1.docx", pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.2.docx", SaveFormat.Docx, pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.Replace.3.docx", SaveFormat.Docx, pattern, replacement, options);
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Replace(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_6}

使用指定的保存格式和附加选项，用替换字符串替换输入文件中所有出现的指定字符串模式。

```csharp
public static int Replace(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |
| saveOptions | SaveOptions | 保存选项。 |
| pattern | String | 要替换的字符串。 |
| replacement | String | 用于替换所有出现的模式的字符串。 |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/)对象来指定附加选项。 |

### 返回值

已进行的替换次数。

## 评论

如果输出格式为图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则输出的每一页都将保存为单独的文件。指定的输出文件名将用于生成每个部分的文件名，并遵循以下规则：outputFile_partIndex.extension。

如果输出格式为 TIFF，则输出将保存为单个多帧 TIFF 文件。

### 也可以看看

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Replace(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace}

使用指定的保存格式和附加选项，用替换字符串替换输入流中所有出现的指定字符串模式。

```csharp
public static int Replace(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | Stream | 输入流。 |
| outputStream | Stream | 输出流。 |
| saveFormat | SaveFormat | 保存格式。 |
| pattern | String | 要替换的字符串。 |
| replacement | String | 用于替换所有出现的模式的字符串。 |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/)对象来指定附加选项。 |

### 返回值

已进行的替换次数。

## 评论

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则只有输出的第一页会保存到指定的流。

如果输出格式为 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流。

## 例子

展示如何使用流中的文档替换文档中的字符串。

```csharp
// 有几种方法可以使用流中的文档替换文档中的字符串：
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

using (FileStream streamIn = new FileStream(MyDir + "Footer.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Replace(streamIn, streamOut, SaveFormat.Docx, pattern, replacement);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
    {
        FindReplaceOptions options = new FindReplaceOptions();
        options.FindWholeWordsOnly = false;
        Replacer.Replace(streamIn, streamOut, SaveFormat.Docx, pattern, replacement, options);
    }
}
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Replace(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_2}

使用指定的保存格式和附加选项，用替换字符串替换输入流中所有出现的指定字符串模式。

```csharp
public static int Replace(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | Stream | 输入流。 |
| outputStream | Stream | 输出流。 |
| saveOptions | SaveOptions | 保存选项。 |
| pattern | String | 要替换的字符串。 |
| replacement | String | 用于替换所有出现的模式的字符串。 |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/)对象来指定附加选项。 |

### 返回值

已进行的替换次数。

## 评论

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则只有输出的第一页会保存到指定的流。

如果输出格式为 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流。

### 也可以看看

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Replace(*string, string, Regex, string*) {#replace_9}

使用正则表达式将输入文件中所有出现的指定字符串模式替换为替换字符串。

```csharp
public static int Replace(string inputFileName, string outputFileName, Regex pattern, 
    string replacement)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |
| pattern | Regex | 用于查找匹配项的正则表达式模式。 |
| replacement | String | 用于替换所有出现的模式的字符串。 |

### 返回值

已进行的替换次数。

## 评论

如果输出格式为图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则输出的每一页都将保存为单独的文件。指定的输出文件名将用于生成每个部分的文件名，并遵循以下规则：outputFile_partIndex.extension。

如果输出格式为 TIFF，则输出将保存为单个多帧 TIFF 文件。

## 例子

展示如何在文档中用正则表达式替换字符串。

```csharp
// 有几种方法可以在文档中使用正则表达式替换字符串：
string doc = MyDir + "Footer.docx";
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.1.docx", pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.2.docx", SaveFormat.Docx, pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.3.docx", SaveFormat.Docx, pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
```

### 也可以看看

* class [Replacer](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Replace(*string, string, [SaveFormat](../../../aspose.words/saveformat/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_5}

使用正则表达式、指定的保存格式和附加选项，将输入文件中所有出现的指定字符串模式替换为替换字符串。

```csharp
public static int Replace(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |
| saveFormat | SaveFormat | 保存格式。 |
| pattern | Regex | 用于查找匹配项的正则表达式模式。 |
| replacement | String | 用于替换所有出现的模式的字符串。 |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/)对象来指定附加选项。 |

### 返回值

已进行的替换次数。

## 评论

如果输出格式为图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则输出的每一页都将保存为单独的文件。指定的输出文件名将用于生成每个部分的文件名，并遵循以下规则：outputFile_partIndex.extension。

如果输出格式为 TIFF，则输出将保存为单个多帧 TIFF 文件。

## 例子

展示如何在文档中用正则表达式替换字符串。

```csharp
// 有几种方法可以在文档中使用正则表达式替换字符串：
string doc = MyDir + "Footer.docx";
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.1.docx", pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.2.docx", SaveFormat.Docx, pattern, replacement);
Replacer.Replace(doc, ArtifactsDir + "LowCode.ReplaceRegex.3.docx", SaveFormat.Docx, pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Replace(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_7}

使用正则表达式、指定的保存格式和附加选项，将输入文件中所有出现的指定字符串模式替换为替换字符串。

```csharp
public static int Replace(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |
| saveOptions | SaveOptions | 保存选项。 |
| pattern | Regex | 用于查找匹配项的正则表达式模式。 |
| replacement | String | 用于替换所有出现的模式的字符串。 |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/)对象来指定附加选项。 |

### 返回值

已进行的替换次数。

## 评论

如果输出格式为图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则输出的每一页都将保存为单独的文件。指定的输出文件名将用于生成每个部分的文件名，并遵循以下规则：outputFile_partIndex.extension。

如果输出格式为 TIFF，则输出将保存为单个多帧 TIFF 文件。

### 也可以看看

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Replace(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_1}

使用正则表达式、指定的保存格式和附加选项，将输入流中所有出现的指定字符串模式替换为替换字符串。

```csharp
public static int Replace(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | Stream | 输入流。 |
| outputStream | Stream | 输出流。 |
| saveFormat | SaveFormat | 保存格式。 |
| pattern | Regex | 用于查找匹配项的正则表达式模式。 |
| replacement | String | 用于替换所有出现的模式的字符串。 |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/)对象来指定附加选项。 |

### 返回值

已进行的替换次数。

## 评论

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则只有输出的第一页会保存到指定的流。

如果输出格式为 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流。

## 例子

展示如何使用流中的文档用正则表达式替换文档中的字符串。

```csharp
// 有几种方法可以使用流中的文档将文档中的字符串替换为正则表达式：
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

using (FileStream streamIn = new FileStream(MyDir + "Replace regex.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceStreamRegex.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Replace(streamIn, streamOut, SaveFormat.Docx, pattern, replacement);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceStreamRegex.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Replace(streamIn, streamOut, SaveFormat.Docx, pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
}
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Replace(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_3}

使用正则表达式、指定的保存格式和附加选项，将输入流中所有出现的指定字符串模式替换为替换字符串。

```csharp
public static int Replace(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | Stream | 输入流。 |
| outputStream | Stream | 输出流。 |
| saveOptions | SaveOptions | 保存选项。 |
| pattern | Regex | 用于查找匹配项的正则表达式模式。 |
| replacement | String | 用于替换所有出现的模式的字符串。 |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/)对象来指定附加选项。 |

### 返回值

已进行的替换次数。

## 评论

如果输出格式是图像（BMP、EMF、EPS、GIF、JPEG、PNG 或 WebP），则只有输出的第一页会保存到指定的流。

如果输出格式为 TIFF，则输出将作为单个多帧 TIFF 保存到指定的流。

### 也可以看看

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)
