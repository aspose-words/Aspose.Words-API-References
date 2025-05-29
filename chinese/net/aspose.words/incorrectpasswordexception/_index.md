---
title: IncorrectPasswordException Class
linktitle: IncorrectPasswordException
articleTitle: IncorrectPasswordException
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.IncorrectPasswordException 类，它处理加密文档的密码错误，确保安全无缝的访问。
type: docs
weight: 3700
url: /zh/net/aspose.words/incorrectpasswordexception/
---
## IncorrectPasswordException class

如果文档使用密码加密，并且打开文档时指定的密码不正确或缺失，则抛出。

要了解更多信息，请访问[使用文档进行编程](https://docs.aspose.com/words/net/programming-with-documents/)文档文章。

```csharp
public class IncorrectPasswordException : Exception
```

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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
