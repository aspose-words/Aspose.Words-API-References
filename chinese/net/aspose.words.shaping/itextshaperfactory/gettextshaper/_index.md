---
title: ITextShaperFactory.GetTextShaper
linktitle: GetTextShaper
articleTitle: GetTextShaper
second_title: Aspose.Words for .NET
description: 探索 ITextShaperFactory GetTextShaper 方法，为您的特定字体需求创建自定义文本塑造器，增强您的文本渲染体验。
type: docs
weight: 10
url: /zh/net/aspose.words.shaping/itextshaperfactory/gettextshaper/
---
## GetTextShaper(*string, int*) {#gettextshaper_1}

返回由指定字体的文本整形器的新实例*fontPath*和*faceIndex*.

```csharp
public ITextShaper GetTextShaper(string fontPath, int faceIndex)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontPath | String | 字体文件的绝对路径。 |
| faceIndex | Int32 | TrueType 字体集合中的字体索引，如果指定的字体文件不是 TrueType 字体集合，则为 或 0。 |

### 也可以看看

* interface [ITextShaper](../../itextshaper/)
* interface [ITextShaperFactory](../)
* 命名空间 [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* 部件 [Aspose.Words](../../../)

---

## GetTextShaper(*string, byte[], int*) {#gettextshaper}

返回由以下字体表示的文本塑造器的新实例*fontBlob*和*faceIndex*.

```csharp
public ITextShaper GetTextShaper(string fontId, byte[] fontBlob, int faceIndex)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontId | String | 可与所提供字体唯一关联的唯一标识符*fontBlob*. |
| fontBlob | Byte[] | 包含字体数据的字节数组。 |
| faceIndex | Int32 | TrueType 字体集合中的字体索引，如果为 或 0*fontBlob*不是 TrueType 字体集合。 |

### 也可以看看

* interface [ITextShaper](../../itextshaper/)
* interface [ITextShaperFactory](../)
* 命名空间 [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* 部件 [Aspose.Words](../../../)
