---
title: GeneralFormat
second_title: Aspose.Words for .NET API 参考
description: 指定应用于数字文本或任何字段结果的通用格式 一个字段可能有通用格式的组合
type: docs
weight: 2440
url: /zh/net/aspose.words.fields/generalformat/
---
## GeneralFormat enumeration

指定应用于数字、文本或任何字段结果的通用格式。 一个字段可能有通用格式的组合。

```csharp
public enum GeneralFormat
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 用于指定缺少的通用格式。 |
| Aiueo | `1` | 数字格式。使用传统 aiueo 顺序中的平假名字符格式化数字结果。 |
| UppercaseAlphabetic | `2` | 数字格式。将数值结果格式化为一次或多次出现的大写拉丁字母字符。 |
| LowercaseAlphabetic | `3` | 数字格式。将数值结果格式化为一个或多个小写字母拉丁字符。 |
| Arabic | `4` | 数字格式。使用阿拉伯基数格式化数字结果。 |
| ArabicAbjad | `5` | 数字格式。使用升序 Abjad 数字格式化数字结果。 |
| ArabicAlpha | `6` | 数字格式。使用阿拉伯字母表中的字符格式化数字结果。 |
| ArabicDash | `7` | 数字格式。使用阿拉伯基数来格式化数字结果，前缀为“-”，后缀为“-”。 |
| BahtText | `8` | 数字格式。在泰语计数系统中格式化数字结果。 |
| CardText | `9` | 数字格式。主要文本（一、二、三、...）。 |
| ChineseNum1 | `10` | 数字格式。使用来自适当计数系统的升序数字格式化数字结果。 |
| ChineseNum2 | `11` | 数字格式。使用来自适当合法格式的序列号格式化数字结果。 |
| ChineseNum3 | `12` | 数字格式。使用来自适当的计数千系统的序列号格式化数字结果。 |
| Chosung | `13` | 数字格式。使用韩国 Chosung 格式的序列号格式化数字结果。 |
| CircleNum | `14` | 数字格式。使用包围在圆圈中的十进制编号格式化数字结果，使用 封闭的字母数字字形字符表示 1–20 范围内的数字。 |
| DBChar | `15` | 数字格式。使用双字节阿拉伯编号格式化数字结果。 |
| DBNum1 | `16` | 数字格式。使用适当的字符，使用顺序数字表意文字格式化数字结果。 |
| DBNum2 | `17` | 数字格式。使用来自适当计数系统的序列号格式化数字结果。 |
| DBNum3 | `18` | 数字格式。使用来自适当的合法计数系统的序列号格式化数字结果。 |
| DBNum4 | `19` | 数字格式。使用来自适当数字计数系统的序列号格式化数字结果。 |
| DollarText | `20` | 数字格式。美元文本（一、二、三、... + AND 55/100）。 |
| Ganada | `21` | 数字格式。使用韩国 Ganada 格式的序列号格式化数字结果。 |
| GB1 | `22` | 数字格式。使用带句点的十进制编号格式化数字结果，使用 封闭的字母数字字形字符。 |
| GB2 | `23` | 数字格式。使用括在括号中的十进制编号格式化数字结果， 使用封闭的字母数字字形字符。 |
| GB3 | `24` | 数字格式。使用包围在圆圈中的十进制编号格式化数字结果，使用 封闭的字母数字字形字符。 |
| GB4 | `25` | 数字格式。使用包围在圆圈中的十进制编号格式化数字结果，使用 封闭的字母数字字形字符。 |
| Hebrew1 | `26` | 数字格式。使用希伯来数字格式化数字结果。 |
| Hebrew2 | `27` | 数字格式。使用希伯来字母格式化数字结果。 |
| Hex | `28` | 数字格式。使用大写十六进制数字格式化数值结果。 |
| HindiArabic | `29` | 数字格式。使用印地语数字格式化数字结果。 |
| HindiCardText | `30` | 数字格式。使用印地语计数系统中的序列号格式化数字结果。 |
| HindiLetter1 | `31` | 数字格式。使用印地语元音格式化数字结果。 |
| HindiLetter2 | `32` | 数字格式。使用印地语辅音格式化数字结果。 |
| Iroha | `33` | 数字格式。使用日语 iroha 格式化数字结果。 |
| KanjiNum1 | `34` | 数字格式。使用适当的计数系统使用日式样式格式化数字结果。 |
| KanjiNum2 | `35` | 数字格式。使用适当的计数系统格式化数字结果。 |
| KanjiNum3 | `36` | 数字格式。使用适当的计数系统格式化数字结果。 |
| Ordinal | `37` | 数字格式。序数（第 1、第 2、第 3、...）。 |
| OrdText | `38` | 数字格式。序数文本（第一，第二，第三，...）。 |
| UppercaseRoman | `39` | 数字格式。大写罗马字母 (I, II, III, ...)。 |
| LowercaseRoman | `40` | 数字格式。小写罗马字母 (i, ii, iii, ...)。 |
| SBChar | `41` | 数字格式。使用单字节阿拉伯编号格式化数字结果。 |
| ThaiArabic | `42` | 数字格式。使用泰语数字格式化数字结果。 |
| ThaiCardText | `43` | 数字格式。使用泰语计数系统中的序列号格式化数字结果。 |
| ThaiLetter | `44` | 数字格式。使用泰语字母格式化数字结果。 |
| VietCardText | `45` | 数字格式。使用越南数字格式化数字结果。 |
| Zodiac1 | `46` | 数字格式。使用顺序数字传统表意文字格式化数字结果。 |
| Zodiac2 | `47` | 数字格式。使用顺序生肖象形文字格式化数字结果。 |
| Zodiac3 | `48` | 数字格式。使用连续的传统生肖表意文字格式化数字结果。 |
| Caps | `49` | 文本格式。将每个单词的第一个字母大写。 |
| FirstCap | `50` | 文本格式。将第一个单词的第一个字母大写。 |
| Lower | `51` | 文本格式。所有字母都是小写的。 |
| Upper | `52` | 文本格式。所有字母都是大写的。 |
| CharFormat | `53` | 字段结果格式。 CHARFORMAT 指令。 |
| MergeFormat | `54` | 字段结果格式。 MERGEFORMAT 指令。 |
| MergeFormatInet | `55` | 字段结果格式。 MERGEFORMATINET 指令。 |

### 例子

显示如何格式化字段结果。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 使用文档构建器插入一个显示未应用格式的结果的字段。
Field field = builder.InsertField("= 2 + 3");

Assert.AreEqual("= 2 + 3", field.GetFieldCode());
Assert.AreEqual("5", field.Result);

// 我们可以使用字段的属性将格式应用于字段的结果。
// 下面是我们可以应用于字段结果的三种格式。
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

// 我们可以删除格式以将字段的结果恢复为原始形式。
format.GeneralFormats.Remove(GeneralFormat.LowercaseRoman);
format.GeneralFormats.RemoveAt(0);
Assert.AreEqual(0, format.GeneralFormats.Count);
field.Update();

Assert.AreEqual("= 25 + 33  ", field.GetFieldCode());
Assert.AreEqual("58", field.Result);
Assert.AreEqual(0, format.GeneralFormats.Count);
```

### 也可以看看

* namespace [Aspose.Words.Fields](../../aspose.words.fields)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
