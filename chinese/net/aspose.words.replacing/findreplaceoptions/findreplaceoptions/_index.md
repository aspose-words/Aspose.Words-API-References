---
title: FindReplaceOptions
linktitle: FindReplaceOptions
articleTitle: FindReplaceOptions
second_title: Aspose.Words for .NET
description: 发现 FindReplaceOptions 构造函数以便使用默认设置轻松初始化新实例，从而增强您的搜索和替换功能。
type: docs
weight: 10
url: /zh/net/aspose.words.replacing/findreplaceoptions/findreplaceoptions/
---
## FindReplaceOptions() {#constructor}

使用默认设置初始化 FindReplaceOptions 类的新实例。

```csharp
public FindReplaceOptions()
```

## 例子

展示如何识别和使用替换模式中的替换。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Jason gave money to Paul.");

Regex regex = new Regex(@"([A-z]+) gave money to ([A-z]+)");

FindReplaceOptions options = new FindReplaceOptions();
options.UseSubstitutions = true;

// 使用传统模式不支持许多高级功能，因此我们需要将其设置为“false”。
options.LegacyMode = false;

doc.Range.Replace(regex, @"$2 took money from $1", options);

Assert.AreEqual(doc.GetText(), "Paul took money from Jason.\f");
```

### 也可以看看

* class [FindReplaceOptions](../)
* 命名空间 [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* 部件 [Aspose.Words](../../../)

---

## FindReplaceOptions(*[FindReplaceDirection](../../findreplacedirection/)*) {#constructor_1}

使用指定的方向初始化 FindReplaceOptions 类的新实例。

```csharp
public FindReplaceOptions(FindReplaceDirection direction)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| direction | FindReplaceDirection | 查找和替换操作的方向。 |

### 也可以看看

* enum [FindReplaceDirection](../../findreplacedirection/)
* class [FindReplaceOptions](../)
* 命名空间 [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* 部件 [Aspose.Words](../../../)

---

## FindReplaceOptions(*[IReplacingCallback](../../ireplacingcallback/)*) {#constructor_3}

使用指定的替换回调初始化 FindReplaceOptions 类的新实例。

```csharp
public FindReplaceOptions(IReplacingCallback replacingCallback)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| replacingCallback | IReplacingCallback | 用于替换找到的文本的回调。 |

## 例子

展示如何跟踪文本替换操作遍历节点的顺序。

```csharp
public void Order(bool differentFirstPageHeaderFooter)
{
    Document doc = new Document(MyDir + "Header and footer types.docx");

    Section firstPageSection = doc.FirstSection;

    ReplaceLog logger = new ReplaceLog();
    FindReplaceOptions options = new FindReplaceOptions(logger);

    // 对第一页使用不同的页眉/页脚将影响搜索顺序。
    firstPageSection.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;
    doc.Range.Replace(new Regex("(header|footer)"), "", options);

    if (differentFirstPageHeaderFooter)
        Assert.AreEqual("First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n", 
            logger.Text.Replace("\r", ""));
    else
        Assert.AreEqual("Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n", 
            logger.Text.Replace("\r", ""));
}

/// <summary>
/// 在查找和替换操作期间，记录操作“找到”的每个包含文本的节点的内容，
/// 处于替换发生之前的状态。
/// 这将显示文本替换操作遍历节点的顺序。
/// </summary>
private class ReplaceLog : IReplacingCallback
{
    public ReplaceAction Replacing(ReplacingArgs args)
    {
        mTextBuilder.AppendLine(args.MatchNode.GetText());
        return ReplaceAction.Skip;
    }

    internal string Text => mTextBuilder.ToString();

    private readonly StringBuilder mTextBuilder = new StringBuilder();
}
```

### 也可以看看

* interface [IReplacingCallback](../../ireplacingcallback/)
* class [FindReplaceOptions](../)
* 命名空间 [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* 部件 [Aspose.Words](../../../)

---

## FindReplaceOptions(*[FindReplaceDirection](../../findreplacedirection/), [IReplacingCallback](../../ireplacingcallback/)*) {#constructor_2}

使用指定的方向和替换回调初始化 FindReplaceOptions 类的新实例。

```csharp
public FindReplaceOptions(FindReplaceDirection direction, IReplacingCallback replacingCallback)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| direction | FindReplaceDirection | 查找和替换操作的方向。 |
| replacingCallback | IReplacingCallback | 用于替换找到的文本的回调。 |

### 也可以看看

* enum [FindReplaceDirection](../../findreplacedirection/)
* interface [IReplacingCallback](../../ireplacingcallback/)
* class [FindReplaceOptions](../)
* 命名空间 [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* 部件 [Aspose.Words](../../../)
