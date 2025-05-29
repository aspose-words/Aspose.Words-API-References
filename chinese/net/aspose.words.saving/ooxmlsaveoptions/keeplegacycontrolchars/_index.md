---
title: OoxmlSaveOptions.KeepLegacyControlChars
linktitle: KeepLegacyControlChars
articleTitle: KeepLegacyControlChars
second_title: Aspose.Words for .NET
description: 发现 OoxmlSaveOptions 的 KeepLegacyControlChars 属性，以维护旧式控制字符的原始格式，实现无缝文档转换。
type: docs
weight: 50
url: /zh/net/aspose.words.saving/ooxmlsaveoptions/keeplegacycontrolchars/
---
## OoxmlSaveOptions.KeepLegacyControlChars property

保留旧式控制字符的原始表示。

```csharp
public bool KeepLegacyControlChars { get; set; }
```

## 例子

展示如何在转换为 .docx 时支持旧式控制字符。

```csharp
Document doc = new Document(MyDir + "Legacy control character.doc");

// 当我们将文档保存为 OOXML 格式时，我们可以创建一个 OoxmlSaveOptions 对象
// 然后将其传递给文档的保存方法来修改我们保存文档的方式。
// 将“KeepLegacyControlChars”属性设置为“true”以保留
// 保存时使用“ShortDateTime”遗留字符。
// 将“KeepLegacyControlChars”属性设置为“false”以删除
// 输出文档中的“ShortDateTime”遗留字符。
OoxmlSaveOptions so = new OoxmlSaveOptions(SaveFormat.Docx);
so.KeepLegacyControlChars = keepLegacyControlChars;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx");

Assert.AreEqual(keepLegacyControlChars ? "\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f" : "\u001e\f",
    doc.FirstSection.Body.GetText());
```

### 也可以看看

* class [OoxmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
