---
title: FindReplaceOptions.UseSubstitutions
linktitle: UseSubstitutions
articleTitle: UseSubstitutions
second_title: Aspose.Words for .NET
description: 探索 FindReplaceOptions 中的 UseSubstitutions 属性。轻松在替换模式中启用替换，增强文本编辑的灵活性。
type: docs
weight: 190
url: /zh/net/aspose.words.replacing/findreplaceoptions/usesubstitutions/
---
## FindReplaceOptions.UseSubstitutions property

获取或设置一个布尔值，指示是否识别并使用替换模式中的替换。 默认值为`错误的`.

```csharp
public bool UseSubstitutions { get; set; }
```

## 评论

有关替换元素的详细信息，请参阅： https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.

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

展示如何用替代内容替换文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("John sold a car to Paul.");
builder.Writeln("Jane sold a house to Joe.");

// 我们可以使用“FindReplaceOptions”对象来修改查找和替换过程。
FindReplaceOptions options = new FindReplaceOptions();

// 将“UseSubstitutions”属性设置为“true”以获取
// 查找和替换操作来识别替换元素。
// 将“UseSubstitutions”属性设置为“false”以忽略替换元素。
options.UseSubstitutions = useSubstitutions;

Regex regex = new Regex(@"([A-z]+) sold a ([A-z]+) to ([A-z]+)");
doc.Range.Replace(regex, @"$3 bought a $2 from $1", options);

Assert.AreEqual(
    useSubstitutions
        ? "Paul bought a car from John.\rJoe bought a house from Jane."
        : "$3 bought a $2 from $1.\r$3 bought a $2 from $1.", doc.GetText().Trim());
```

### 也可以看看

* class [FindReplaceOptions](../)
* 命名空间 [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* 部件 [Aspose.Words](../../../)
