---
title: FileFormatInfo.IsEncrypted
linktitle: IsEncrypted
articleTitle: IsEncrypted
second_title: Aspose.Words for .NET
description: 使用 FileFormatInfo IsEncrypted 属性检查您的文档是否安全 - 对于需要密码才能访问的加密文件，返回 true。
type: docs
weight: 40
url: /zh/net/aspose.words/fileformatinfo/isencrypted/
---
## FileFormatInfo.IsEncrypted property

返回`真的`如果文档已加密并需要密码才能打开。

```csharp
public bool IsEncrypted { get; }
```

## 评论

此属性用于帮助您区分已加密和未加密的文档。 如果您尝试使用 Aspose.Words 加载加密文档而不提供密码，则会引发 异常。您可以使用此属性检测文档是否需要密码 ，并在加载文档之前采取一些措施，例如提示用户输入密码。

## 例子

展示如何使用 FileFormatUtil 类检测文档格式和加密。

```csharp
Document doc = new Document();

// 配置一个 SaveOptions 对象来加密文档
// 保存时使用密码，然后保存文档。
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// 验证我们文档的文件类型及其加密状态。
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.AreEqual(".odt", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.True(info.IsEncrypted);
```

### 也可以看看

* class [FileFormatInfo](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
