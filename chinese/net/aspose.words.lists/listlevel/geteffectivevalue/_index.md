---
title: ListLevel.GetEffectiveValue
linktitle: GetEffectiveValue
articleTitle: GetEffectiveValue
second_title: Aspose.Words for .NET
description: 探索 ListLevel 的 GetEffectiveValue 方法，轻松检索列表项的字符串表示形式。使用 NumberStyle 和格式选项进行自定义！
type: docs
weight: 190
url: /zh/net/aspose.words.lists/listlevel/geteffectivevalue/
---
## ListLevel.GetEffectiveValue method

报告[`ListLevel`](../)列表项指定 index 的对象。参数指定[`NumberStyle`](../../../aspose.words/numberstyle/)以及可选格式 string 用于Custom已指定。

```csharp
public static string GetEffectiveValue(int index, NumberStyle numberStyle, 
    string customNumberStyleFormat)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | Int32 | 列表项的索引（必须在 1 到 32767 范围内）。 |
| numberStyle | NumberStyle | [`NumberStyle`](../../../aspose.words/numberstyle/)的[`ListLevel`](../)对象. |
| customNumberStyleFormat | String | 可选格式字符串Custom已指定（例如“a、ç、ĝ、...”）。 在其他情况下，此参数必须是`无效的`或为空。 |

### 返回值

的字符串表示形式[`ListLevel`](../)对象，由*numberStyle*参数and *customNumberStyleFormat*参数，在列表项中由*index*参数.

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentException | *customNumberStyleFormat*是`无效的`或为空时*numberStyle*是自定义的。-或- *customNumberStyleFormat*不是`无效的`或为空时*numberStyle*是非自定义的。-或- *customNumberStyleFormat*无效。 |
| ArgumentOutOfRangeException | 索引超出范围。 |

## 例子

展示如何获取具有自定义数字样式的列表格式。

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

ListLevel listLevel = doc.FirstSection.Body.Paragraphs[0].ListFormat.ListLevel;

string customNumberStyleFormat = string.Empty;

if (listLevel.NumberStyle == NumberStyle.Custom)
    customNumberStyleFormat = listLevel.CustomNumberStyleFormat;

Assert.AreEqual("001, 002, 003, ...", customNumberStyleFormat);

// 我们可以获取列表项指定索引的值。
Assert.AreEqual("iv", ListLevel.GetEffectiveValue(4, NumberStyle.LowercaseRoman, null));
Assert.AreEqual("005", ListLevel.GetEffectiveValue(5, NumberStyle.Custom, customNumberStyleFormat));
```

### 也可以看看

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [ListLevel](../)
* 命名空间 [Aspose.Words.Lists](../../../aspose.words.lists/)
* 部件 [Aspose.Words](../../../)
