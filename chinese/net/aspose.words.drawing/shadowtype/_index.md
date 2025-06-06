---
title: ShadowType Enum
linktitle: ShadowType
articleTitle: ShadowType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.ShadowType 枚举，使用可自定义的阴影类型增强您的形状，以获得令人惊叹的文档视觉效果。
type: docs
weight: 1630
url: /zh/net/aspose.words.drawing/shadowtype/
---
## ShadowType enumeration

指定形状阴影的类型。

```csharp
public enum ShadowType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| ShadowMixed | `-2` | 没有预定义的阴影预设。 |
| Shadow1 | `1` | 第一种阴影类型。 |
| Shadow10 | `10` | 第十种阴影类型。 |
| Shadow11 | `11` | 第十一种阴影类型。 |
| Shadow12 | `12` | 第十二种阴影类型。 |
| Shadow13 | `13` | 第十三种阴影类型。 |
| Shadow14 | `14` | 第十四种阴影类型。 |
| Shadow15 | `15` | 第十五种阴影类型。 |
| Shadow16 | `16` | 第十六种阴影类型。 |
| Shadow17 | `17` | 第十七种阴影类型。 |
| Shadow18 | `18` | 第十八种阴影类型。 |
| Shadow19 | `19` | 第十九种阴影类型。 |
| Shadow2 | `2` | 第二种阴影类型。 |
| Shadow20 | `20` | 第二十种阴影类型。 |
| Shadow21 | `21` | 第二十一种影子类型。 |
| Shadow22 | `22` | 第二十二个影子类型。 |
| Shadow23 | `23` | 第二十三种影子类型。 |
| Shadow24 | `24` | 第二十四种阴影类型。 |
| Shadow25 | `25` | 第二十五种阴影类型。 |
| Shadow26 | `26` | 第二十六种阴影类型。 |
| Shadow27 | `27` | 第二十七种阴影类型。 |
| Shadow28 | `28` | 第二十八种阴影类型。 |
| Shadow29 | `29` | 第二十九种阴影类型。 |
| Shadow3 | `3` | 第三种阴影类型。 |
| Shadow30 | `30` | 第三十种阴影类型。 |
| Shadow31 | `31` | 第三十一种影子类型。 |
| Shadow32 | `32` | 三十二秒暗影类型。 |
| Shadow33 | `33` | 第三十三种影子类型。 |
| Shadow34 | `34` | 第三十四种影子类型。 |
| Shadow35 | `35` | 第三十五种阴影类型。 |
| Shadow36 | `36` | 第三十六种阴影类型。 |
| Shadow37 | `37` | 第三十七种阴影类型。 |
| Shadow38 | `38` | 第三十八种阴影类型。 |
| Shadow39 | `39` | 第三十九种阴影类型。 |
| Shadow4 | `4` | 第四种阴影类型。 |
| Shadow40 | `40` | 第四十种阴影类型。 |
| Shadow41 | `41` | 第四十一种影子类型。 |
| Shadow42 | `42` | 第四十二个影子类型。 |
| Shadow43 | `43` | 第四十三种影子类型。 |
| Shadow5 | `5` | 第五种阴影类型。 |
| Shadow6 | `6` | 第六种阴影类型。 |
| Shadow7 | `7` | 第七种阴影类型。 |
| Shadow8 | `8` | 第八种阴影类型。 |
| Shadow9 | `9` | 第九种影子类型。 |

## 评论

ShadowType 不是一个简单的属性，而是一个预设，它一次性设置了形成 阴影外观的几个属性。

## 例子

展示如何使用形状的阴影格式。

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];

if (shape.ShadowFormat.Visible && shape.ShadowFormat.Type == ShadowType.Shadow2)
    shape.ShadowFormat.Type = ShadowType.Shadow7;

if (shape.ShadowFormat.Type == ShadowType.ShadowMixed)
    shape.ShadowFormat.Clear();
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
