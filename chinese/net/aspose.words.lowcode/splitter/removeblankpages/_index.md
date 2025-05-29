---
title: Splitter.RemoveBlankPages
linktitle: RemoveBlankPages
articleTitle: RemoveBlankPages
second_title: Aspose.Words for .NET
description: 使用 Splitter RemoveBlankPages 方法轻松删除文档中的空白页。立即节省时间并优化您的工作流程！
type: docs
weight: 30
url: /zh/net/aspose.words.lowcode/splitter/removeblankpages/
---
## RemoveBlankPages(*string, string*) {#removeblankpages_2}

从文档中删除空白页并保存输出。返回已删除页码的列表。

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |

### 返回值

页码列表已被视为空白并被删除。

## 例子

展示如何从文档中删除空白页。

```csharp
// 有几种方法可以从文档中删除空白页：
string doc = MyDir + "Blank pages.docx";

Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.1.docx");
Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.2.docx", SaveFormat.Docx);
```

### 也可以看看

* class [Splitter](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## RemoveBlankPages(*string, string, [SaveFormat](../../../aspose.words/saveformat/)*) {#removeblankpages_3}

从文档中删除空白页，并以指定格式保存输出。返回已删除页码的列表。

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName, 
    SaveFormat saveFormat)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |
| saveFormat | SaveFormat | 保存格式。 |

### 返回值

页码列表已被视为空白并被删除。

## 例子

展示如何从文档中删除空白页。

```csharp
// 有几种方法可以从文档中删除空白页：
string doc = MyDir + "Blank pages.docx";

Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.1.docx");
Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.2.docx", SaveFormat.Docx);
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## RemoveBlankPages(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#removeblankpages_4}

从文档中删除空白页，并以指定格式保存输出。返回已删除页码的列表。

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName, 
    SaveOptions saveOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputFileName | String | 输入文件名。 |
| outputFileName | String | 输出文件名。 |
| saveOptions | SaveOptions | 保存选项。 |

### 返回值

页码列表已被视为空白并被删除。

### 也可以看看

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## RemoveBlankPages(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#removeblankpages}

从输入流提供的文档中删除空白页，并将更新后的文档 以指定的保存格式保存到输出流。返回已删除页码的列表。

```csharp
public static List<int> RemoveBlankPages(Stream inputStream, Stream outputStream, 
    SaveFormat saveFormat)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | Stream | 输入流。 |
| outputStream | Stream | 输出流。 |
| saveFormat | SaveFormat | 保存格式。 |

### 返回值

页码列表已被视为空白并被删除。

## 例子

展示如何从文档流中删除空白页。

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Blank pages.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.RemoveBlankPagesStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Splitter.RemoveBlankPages(streamIn, streamOut, SaveFormat.Docx);
}
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## RemoveBlankPages(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#removeblankpages_1}

从输入流提供的文档中删除空白页，并将更新后的文档 以指定的保存格式保存到输出流。返回已删除页码的列表。

```csharp
public static List<int> RemoveBlankPages(Stream inputStream, Stream outputStream, 
    SaveOptions saveOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| inputStream | Stream | 输入流。 |
| outputStream | Stream | 输出流。 |
| saveOptions | SaveOptions | 保存选项。 |

### 返回值

页码列表已被视为空白并被删除。

### 也可以看看

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)
