---
title: GeneralFormat Enum
linktitle: GeneralFormat
articleTitle: GeneralFormat
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fields.GeneralFormat 枚举，它增强了字段的数字文本格式，确保文档的清晰度和精确度。
type: docs
weight: 3050
url: /zh/net/aspose.words.fields/generalformat/
---
## GeneralFormat enumeration

指定应用于数字、文本或任何字段结果的通用格式。 一个字段可能有多种通用格式的组合。

```csharp
public enum GeneralFormat
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 用于指定缺少的通用格式。 |
| Aiueo | `1` | 数字格式。使用传统 aiueo 顺序的平假名字符格式化数字结果。 |
| UppercaseAlphabetic | `2` | 数字格式。将数字结果格式化为一个或多个大写拉丁字母。 |
| LowercaseAlphabetic | `3` | 数字格式。将数字结果格式化为一个或多个小写拉丁字母。 |
| Arabic | `4` | 数字格式。使用阿拉伯基数格式化数字结果。 |
| ArabicAbjad | `5` | 数字格式。使用升序 Abjad 数字格式化数字结果。 |
| ArabicAlpha | `6` | 数字格式。使用阿拉伯字母中的字符格式化数字结果。 |
| ArabicDash | `7` | 数字格式。使用阿拉伯基数格式化数字结果，前缀为“-”，后缀为“-”。 |
| BahtText | `8` | 数字格式。使用泰国计数系统格式化数字结果。 |
| CardText | `9` | 数字格式。基数文本（一、二、三……）。 |
| ChineseNum1 | `10` | 数字格式。使用相应计数系统中的升序数字格式化数字结果。 |
| ChineseNum2 | `11` | 数字格式。使用符合适当合法格式的连续数字来格式化数字结果。 |
| ChineseNum3 | `12` | 数字格式。使用适当的千位进制中的连续数字来格式化数字结果。 |
| Chosung | `13` | 数字格式。使用韩文朝鲜文格式的连续数字来格式化数字结果。 |
| CircleNum | `14` | 数字格式。使用圆圈括起来的十进制数字来格式化数字结果，并使用 括起来的字母数字符号来表示 1 至 20 范围内的数字。 |
| DBChar | `15` | 数字格式。使用双字节阿拉伯数字格式化数字结果。 |
| DBNum1 | `16` | 数字格式。使用连续的数字表意文字，并使用适当的字符来格式化数字结果。 |
| DBNum2 | `17` | 数字格式。使用相应计数系统中的连续数字来格式化数字结果。 |
| DBNum3 | `18` | 数字格式。使用来自适当合法计数系统的连续数字来格式化数字结果。 |
| DBNum4 | `19` | 数字格式。使用相应数字计数系统中的连续数字来格式化数字结果。 |
| DollarText | `20` | 数字格式。美元符号文本（一、二、三……+ AND 55/100）。 |
| Ganada | `21` | 数字格式。使用韩语 Ganada 格式的连续数字来格式化数字结果。 |
| GB1 | `22` | 数字格式。使用十进制数字后跟句点来格式化数字结果，并使用 括起来的字母数字符号。 |
| GB2 | `23` | 数字格式。使用括号中的十进制数字格式化数字结果， 使用括号中的字母数字符号。 |
| GB3 | `24` | 数字格式。使用圆圈括起来的十进制数字来格式化数字结果，并使用 括起来的字母数字符号。 |
| GB4 | `25` | 数字格式。使用圆圈括起来的十进制数字来格式化数字结果，并使用 括起来的字母数字符号。 |
| Hebrew1 | `26` | 数字格式。使用希伯来数字格式化数字结果。 |
| Hebrew2 | `27` | 数字格式。使用希伯来字母格式化数字结果。 |
| Hex | `28` | 数字格式。使用大写十六进制数字格式化数字结果。 |
| HindiArabic | `29` | 数字格式。使用印地语数字格式化数字结果。 |
| HindiCardText | `30` | 数字格式。使用印地语计数系统中的连续数字来格式化数字结果。 |
| HindiLetter1 | `31` | 数字格式。使用印地语元音字母格式化数字结果。 |
| HindiLetter2 | `32` | 数字格式。使用印地语辅音格式化数字结果。 |
| Iroha | `33` | 数字格式。使用日语伊吕波格式格式化数字结果。 |
| KanjiNum1 | `34` | 数字格式。使用适当的计数系统，按照日语格式格式化数字结果。 |
| KanjiNum2 | `35` | 数字格式。使用适当的计数系统格式化数字结果。 |
| KanjiNum3 | `36` | 数字格式。使用适当的计数系统格式化数字结果。 |
| Ordinal | `37` | 数字格式。序数（第一、第二、第三……）。 |
| OrdText | `38` | 数字格式。序数文本（第一、第二、第三……）。 |
| UppercaseRoman | `39` | 数字格式。大写罗马字母 (I、II、III、...)。 |
| LowercaseRoman | `40` | 数字格式。小写罗马字母 (i, ii, iii, ...). |
| SBChar | `41` | 数字格式。使用单字节阿拉伯数字格式化数字结果。 |
| ThaiArabic | `42` | 数字格式。使用泰文数字格式化数字结果。 |
| ThaiCardText | `43` | 数字格式。使用泰国计数系统中的连续数字来格式化数字结果。 |
| ThaiLetter | `44` | 数字格式。使用泰语字母格式化数字结果。 |
| VietCardText | `45` | 数字格式。使用越南数字格式化数字结果。 |
| Zodiac1 | `46` | 数字格式。使用连续的数字传统表意文字格式化数字结果。 |
| Zodiac2 | `47` | 数字格式。使用连续的十二生肖表意文字格式化数字结果。 |
| Zodiac3 | `48` | 数字格式。使用连续的传统十二生肖表意文字格式化数字结果。 |
| Caps | `49` | 文本格式。将每个单词的首字母大写。 |
| FirstCap | `50` | 文本格式。将第一个单词的首字母大写。 |
| Lower | `51` | 文本格式。所有字母均为小写。 |
| Upper | `52` | 文本格式。所有字母均大写。 |
| CharFormat | `53` | 字段结果格式化。CHARFORMAT 指令。 |
| MergeFormat | `54` | 字段结果格式化。MERGEFORMAT 指令。 |
| MergeFormatInet | `55` | 字段结果格式化。MERGEFORMATINET 指令。 |

## 例子

显示如何格式化字段结果。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 使用文档生成器插入一个显示未应用格式的结果的字段。
Field field = builder.InsertField("= 2 + 3");

Assert.AreEqual("= 2 + 3", field.GetFieldCode());
Assert.AreEqual("5", field.Result);

// 我们可以使用字段的属性将格式应用于字段的结果。
// 以下是我们可以应用于字段结果的三种格式。
// 1 - 数字格式：
FieldFormat format = field.Format;
format.NumericFormat = "$###.00";
field.Update();

Assert.AreEqual("= 2 + 3 \\# $###.00", field.GetFieldCode());
Assert.AreEqual("$  5.00", field.Result);

// 2 - 日期/时间格式：
field = builder.InsertField("DATE");
format = field.Format;
format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());
Console.WriteLine($"Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

// 3 - 一般格式：
field = builder.InsertField("= 25 + 33");
format = field.Format;
format.GeneralFormats.Add(GeneralFormat.LowercaseRoman);
format.GeneralFormats.Add(GeneralFormat.Upper);
field.Update();

int index = 0;
using (IEnumerator<GeneralFormat> generalFormatEnumerator = format.GeneralFormats.GetEnumerator())
    while (generalFormatEnumerator.MoveNext())
        Console.WriteLine($"General format index {index++}: {generalFormatEnumerator.Current}");

Assert.AreEqual("= 25 + 33 \\* roman \\* Upper", field.GetFieldCode());
Assert.AreEqual("LVIII", field.Result);
Assert.AreEqual(2, format.GeneralFormats.Count);
Assert.AreEqual(GeneralFormat.LowercaseRoman, format.GeneralFormats[0]);

// 我们可以删除格式以将字段的结果恢复为其原始形式。
format.GeneralFormats.Remove(GeneralFormat.LowercaseRoman);
format.GeneralFormats.RemoveAt(0);
Assert.AreEqual(0, format.GeneralFormats.Count);
field.Update();

Assert.AreEqual("= 25 + 33  ", field.GetFieldCode());
Assert.AreEqual("58", field.Result);
Assert.AreEqual(0, format.GeneralFormats.Count);
```

### 也可以看看

* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
