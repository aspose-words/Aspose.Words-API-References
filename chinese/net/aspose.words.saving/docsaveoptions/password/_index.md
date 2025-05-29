---
title: DocSaveOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words for .NET
description: 使用 DocSaveOptions 保护您的文档！轻松设置或检索 RC4 加密密码，保护您的敏感信息。
type: docs
weight: 40
url: /zh/net/aspose.words.saving/docsaveoptions/password/
---
## DocSaveOptions.Password property

获取/设置使用 RC4 加密方法加密文档的密码。

```csharp
public string Password { get; set; }
```

## 评论

为了在不加密的情况下保存文档，此属性应该是`无效的`或空字符串。

## 例子

展示如何设置旧版 Microsoft Word 格式的保存选项。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// 设置一个密码，以保护 Microsoft Word 或 Aspose.Words 对文档的加载。
// 请注意，这不会以任何方式加密文档的内容。
options.Password = "MyPassword";

// 如果文档包含路由单，我们可以通过将此标志设置为 true 来在保存时保留它。
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// 为了能够加载文档，
// 我们将需要在 LoadOptions 对象中应用我们在 DocSaveOptions 对象中指定的密码。
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc"));

LoadOptions loadOptions = new LoadOptions("MyPassword");
doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### 也可以看看

* class [DocSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
