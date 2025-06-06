---
title: PlainTextDocument
linktitle: PlainTextDocument
articleTitle: PlainTextDocument
second_title: Aspose.Words for .NET
description: 使用我们的 PlainTextDocument 构造函数轻松创建纯文本文档。享受自动文件格式检测功能，实现无缝集成！
type: docs
weight: 10
url: /zh/net/aspose.words/plaintextdocument/plaintextdocument/
---
## PlainTextDocument(*string*) {#constructor_2}

从文件创建纯文本文档。自动检测文件格式。

```csharp
public PlainTextDocument(string fileName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 要从中提取文本的文件的名称。 |

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | 该文档格式无法识别或不受支持。 |
| [FileCorruptedException](../../filecorruptedexception/) | 该文档似乎已损坏，无法加载。 |
| Exception | 该文档存在问题，应报告给 Aspose.Words 开发人员。 |
| IOException | 存在输入/输出异常。 |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | 该文档已加密，需要密码才能打开，但您提供的密码不正确。 |
| ArgumentException | 文件名不能为空或空字符串。 |

## 例子

展示如何以纯文本形式加载 Microsoft Word 文档的内容。

```csharp
Document doc = new Document(); 
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PlainTextDocument.Load.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.Load.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### 也可以看看

* class [PlainTextDocument](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## PlainTextDocument(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_3}

从文件创建纯文本文档。允许指定其他选项，例如加密密码。

```csharp
public PlainTextDocument(string fileName, LoadOptions loadOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 要从中提取文本的文件的名称。 |
| loadOptions | LoadOptions | 加载文档时使用的附加选项。可以是`无效的`。 |

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | 该文档格式无法识别或不受支持。 |
| [FileCorruptedException](../../filecorruptedexception/) | 该文档似乎已损坏，无法加载。 |
| Exception | 该文档存在问题，应报告给 Aspose.Words 开发人员。 |
| IOException | 存在输入/输出异常。 |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | 该文档已加密，需要密码才能打开，但您提供的密码不正确。 |
| ArgumentException | 文件名不能为空或空字符串。 |

## 例子

展示如何以纯文本形式加载加密的 Microsoft Word 文档的内容。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "PlainTextDocument.LoadEncrypted.docx", saveOptions);

LoadOptions loadOptions = new LoadOptions();
loadOptions.Password = "MyPassword";

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.LoadEncrypted.docx", loadOptions);

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### 也可以看看

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [PlainTextDocument](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## PlainTextDocument(*Stream*) {#constructor}

从流创建纯文本文档。自动检测文件格式。

```csharp
public PlainTextDocument(Stream stream)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | Stream | 从中提取文本的流。 |

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | 该文档格式无法识别或不受支持。 |
| [FileCorruptedException](../../filecorruptedexception/) | 该文档似乎已损坏，无法加载。 |
| Exception | 该文档存在问题，应报告给 Aspose.Words 开发人员。 |
| IOException | 存在输入/输出异常。 |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | 该文档已加密，需要密码才能打开，但您提供的密码不正确。 |
| ArgumentNullException | 流不能为空。 |
| NotSupportedException | 该流不支持读取或查找。 |
| ObjectDisposedException | 该流是一个已处置的对象。 |

## 评论

文档必须存储在流的开头。流必须支持随机定位。

## 例子

展示如何使用流以纯文本形式加载 Microsoft Word 文档的内容。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
doc.Save(ArtifactsDir + "PlainTextDocument.LoadFromStream.docx");

using (FileStream stream = new FileStream(ArtifactsDir + "PlainTextDocument.LoadFromStream.docx", FileMode.Open))
{
    PlainTextDocument plaintext = new PlainTextDocument(stream);

    Assert.AreEqual("Hello world!", plaintext.Text.Trim());
}
```

### 也可以看看

* class [PlainTextDocument](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## PlainTextDocument(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_1}

从流创建纯文本文档。允许指定其他选项，例如加密密码。

```csharp
public PlainTextDocument(Stream stream, LoadOptions loadOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | Stream | 从中提取文本的流。 |
| loadOptions | LoadOptions | 加载文档时使用的附加选项。可以是`无效的`。 |

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | 该文档格式无法识别或不受支持。 |
| [FileCorruptedException](../../filecorruptedexception/) | 该文档似乎已损坏，无法加载。 |
| Exception | 该文档存在问题，应报告给 Aspose.Words 开发人员。 |
| IOException | 存在输入/输出异常。 |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | 该文档已加密，需要密码才能打开，但您提供的密码不正确。 |
| ArgumentNullException | 流不能为空。 |
| NotSupportedException | 该流不支持读取或查找。 |
| ObjectDisposedException | 该流是一个已处置的对象。 |

## 评论

文档必须存储在流的开头。流必须支持随机定位。

## 例子

展示如何使用流以纯文本形式加载加密的 Microsoft Word 文档的内容。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "PlainTextDocument.LoadFromStreamWithOptions.docx", saveOptions);

LoadOptions loadOptions = new LoadOptions();
loadOptions.Password = "MyPassword";

using (FileStream stream = new FileStream(ArtifactsDir + "PlainTextDocument.LoadFromStreamWithOptions.docx", FileMode.Open))
{
    PlainTextDocument plaintext = new PlainTextDocument(stream, loadOptions);

    Assert.AreEqual("Hello world!", plaintext.Text.Trim());
}
```

### 也可以看看

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [PlainTextDocument](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
