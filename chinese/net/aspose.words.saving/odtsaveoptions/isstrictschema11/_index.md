---
title: OdtSaveOptions.IsStrictSchema11
linktitle: IsStrictSchema11
articleTitle: IsStrictSchema11
second_title: Aspose.Words for .NET
description: 使用 IsStrictSchema11 属性优化您的 ODT 导出。请确保严格遵循 ODT 1.1 或启用 1.2 兼容性以获得最佳效果。
type: docs
weight: 30
url: /zh/net/aspose.words.saving/odtsaveoptions/isstrictschema11/
---
## OdtSaveOptions.IsStrictSchema11 property

指定导出是否应严格符合 ODT 规范 1.1。 OOo 3.0 在文件包含 ODT 1.2 的元素和属性时正确显示文件。 为此使用“false”，或为严格符合规范 1.1 使用“true”。 默认值为`错误的`.

```csharp
public bool IsStrictSchema11 { get; set; }
```

## 例子

展示如何使保存的文档符合旧的 ODT 模式。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### 也可以看看

* class [OdtSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
