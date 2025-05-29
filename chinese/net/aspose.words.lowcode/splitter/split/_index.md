---
title: Splitter.Split
linktitle: Split
articleTitle: Split
second_title: Aspose.Words for .NET
description: 使用我们灵活的 Splitter 方法，轻松将文档拆分成多个部分。保存为您选择的格式，方便文件管理！
type: docs
weight: 40
url: /zh/net/aspose.words.lowcode/splitter/split/
---
## Split(*string, string, [SplitOptions](../../splitoptions/)*) {#split_2}

根据指定的拆分选项将文档拆分为多个部分，并将拆分后的部分保存到文件中。输出文件格式由输出文件的扩展名决定。

```csharp
public static void Split(string inputFileName, string outputFileName, SplitOptions options)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 使用规则“outputFile_partIndex.extension”生成文档部分文件名的输出文件名 |
| options | SplitOptions | 文档拆分选项。 |

## 例子

显示如何按页面拆分文档。

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### 也可以看看

* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Split(*string, string, [SaveFormat](../../../aspose.words/saveformat/), [SplitOptions](../../splitoptions/)*) {#split_3}

根据指定的拆分选项将文档拆分为多个部分，并将拆分后的部分保存为指定保存格式的文件中。

```csharp
public static void Split(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    SplitOptions options)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 使用规则“outputFile_partIndex.extension”生成文档部分文件名的输出文件名 |
| saveFormat | SaveFormat | 保存格式。 |
| options | SplitOptions | 文档拆分选项。 |

## 例子

显示如何按页面拆分文档。

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Split(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), [SplitOptions](../../splitoptions/)*) {#split_4}

根据指定的拆分选项将文档拆分为多个部分，并将拆分后的部分保存为指定保存格式的文件中。

```csharp
public static void Split(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    SplitOptions options)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 使用规则“outputFile_partIndex.extension”生成文档部分文件名的输出文件名 |
| saveOptions | SaveOptions | 保存选项。 |
| options | SplitOptions | 文档拆分选项。 |

### 也可以看看

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Split(*Stream, [SaveFormat](../../../aspose.words/saveformat/), [SplitOptions](../../splitoptions/)*) {#split}

根据指定的拆分选项将输入流中的文档拆分为多个部分，并且 将结果部分作为指定保存格式的流数组返回。

```csharp
public static Stream[] Split(Stream inputStream, SaveFormat saveFormat, SplitOptions options)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | Stream | 输入流。 |
| saveFormat | SaveFormat | 保存格式。 |
| options | SplitOptions | 文档拆分选项。 |

## 例子

展示如何按页面从流中拆分文档。

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    SplitOptions options = new SplitOptions();
    options.SplitCriteria = SplitCriteria.Page;
    Stream[] stream = Splitter.Split(streamIn, SaveFormat.Docx, options);
}
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Split(*Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), [SplitOptions](../../splitoptions/)*) {#split_1}

根据指定的拆分选项将输入流中的文档拆分为多个部分，并且 将结果部分作为指定保存格式的流数组返回。

```csharp
public static Stream[] Split(Stream inputStream, SaveOptions saveOptions, SplitOptions options)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | Stream | 输入流。 |
| saveOptions | SaveOptions | 保存选项。 |
| options | SplitOptions | 文档拆分选项。 |

### 也可以看看

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)
