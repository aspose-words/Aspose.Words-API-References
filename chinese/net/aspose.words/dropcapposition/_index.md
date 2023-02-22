---
title: Enum DropCapPosition
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.DropCapPosition 枚举. 指定首字下沉文本的位置
type: docs
weight: 1260
url: /zh/net/aspose.words/dropcapposition/
---
## DropCapPosition enumeration

指定首字下沉文本的位置。

```csharp
public enum DropCapPosition
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 该段落没有首字下沉。 |
| Normal | `1` | 首字下沉位于锚段落的文本边距内。 |
| Margin | `2` | 首字下沉位于锚段落的文本边距之外。 |

### 例子

显示如何创建首字下沉。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个带有大字母的段落，第二和第三段中的文本以该字母开头。
builder.Font.Size = 54;
builder.Writeln("L");

builder.Font.Size = 18;
builder.Writeln("orem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder.Writeln("Ut enim ad minim veniam, quis nostrud exercitation " +
                "ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// 目前，第二和第三段将出现在第一段的下方。
// 我们可以通过“ParagraphFormat”对象将第一段转换为其他段落的首字下沉。
// 将“DropCapPosition”属性设置为“DropCapPosition.Margin”以放置首字下沉
// 如果我们的文本是从左到右的，则在左侧页边距之外。
// 将“DropCapPosition”属性设置为“DropCapPosition.Normal”以将首字下沉放置在页边距内
// 并将其余的文本包裹在它周围。
// “DropCapPosition.None”是所有段落的默认状态。
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.DropCapPosition = dropCapPosition;

doc.Save(ArtifactsDir + "ParagraphFormat.DropCap.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)


