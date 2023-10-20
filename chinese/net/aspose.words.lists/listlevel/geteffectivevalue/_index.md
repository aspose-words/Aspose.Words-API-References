---
title: ListLevel.GetEffectiveValue
linktitle: GetEffectiveValue
articleTitle: GetEffectiveValue
second_title: 用于 .NET 的 Aspose.Words
description: ListLevel GetEffectiveValue 方法. 报告的字符串表示形式ListLevel列表项的指定index 的对象参数指定NumberStyle以及可选格式 string 时使用Custom已指定 在 C#.
type: docs
weight: 190
url: /zh/net/aspose.words.lists/listlevel/geteffectivevalue/
---
## ListLevel.GetEffectiveValue method

报告的字符串表示形式[`ListLevel`](../)列表项的指定index 的对象。参数指定[`NumberStyle`](../../../aspose.words/numberstyle/)以及可选格式 string 时使用Custom已指定。

```csharp
public static string GetEffectiveValue(int index, NumberStyle numberStyle, 
    string customNumberStyleFormat)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | Int32 | 列表项的索引（必须在 1 到 32767 范围内）。 |
| numberStyle | NumberStyle | 的[`NumberStyle`](../../../aspose.words/numberstyle/)的[`ListLevel`](../)对象. |
| customNumberStyleFormat | String | 时使用的可选格式字符串Custom被指定（例如“a, ç, ĝ, ...”）。 在其他情况下，该参数必须是`无效的`或为空。 |

### 返回值

的字符串表示形式[`ListLevel`](../)对象，由*numberStyle*参数and *customNumberStyleFormat*参数，在列表项中由*index*参数.

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentException | *customNumberStyleFormat*是`无效的`或空时*numberStyle*是定制的。-或- *customNumberStyleFormat*不是`无效的`或空时*numberStyle*是非自定义的。-或- *customNumberStyleFormat*无效。 |
| ArgumentOutOfRangeException | 索引超出范围。 |

## 例子

演示如何获取具有自定义数字样式的列表的格式。

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

ListLevel listLevel = doc.FirstSection.Body.Paragraphs[0].ListFormat.ListLevel;

string customNumberStyleFormat = string.Empty;

if (listLevel.NumberStyle == NumberStyle.Custom)
    customNumberStyleFormat = listLevel.CustomNumberStyleFormat;

Assert.AreEqual("001, 002, 003, ...", customNumberStyleFormat);

// 我们可以获取列表项的指定索引的值。
Assert.AreEqual("iv", ListLevel.GetEffectiveValue(4, NumberStyle.LowercaseRoman, null));
Assert.AreEqual("005", ListLevel.GetEffectiveValue(5, NumberStyle.Custom, customNumberStyleFormat));
```

### 也可以看看

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [ListLevel](../)
* 命名空间 [Aspose.Words.Lists](../../../aspose.words.lists/)
* 部件 [Aspose.Words](../../../)
