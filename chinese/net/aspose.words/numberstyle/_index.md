---
title: NumberStyle Enum
linktitle: NumberStyle
articleTitle: NumberStyle
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.NumberStyle 枚举来自定义脚注和尾注页码，轻松增强文档格式。
type: docs
weight: 5040
url: /zh/net/aspose.words/numberstyle/
---
## NumberStyle enumeration

指定列表、脚注、尾注和页码的数字样式。

```csharp
public enum NumberStyle
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Arabic | `0` | 阿拉伯数字（1、2、3……） |
| UppercaseRoman | `1` | 大写罗马字母（I、II、III……） |
| LowercaseRoman | `2` | 小写罗马字母（i、ii、iii、...） |
| UppercaseLetter | `3` | 大写字母（A、B、C、...） |
| LowercaseLetter | `4` | 小写字母（a、b、c、...） |
| Ordinal | `5` | 序数（第 1、第 2、第 3、...） |
| Number | `6` | 编号（一、二、三……） |
| OrdinalText | `7` | 序数（文本）（第一、第二、第三……） |
| Hex | `8` | 十六进制：8、9、A、B、C、D、E、F、10、11、12 |
| ChicagoManual | `9` | 芝加哥格式手册：*、†、† |
| Kanji | `10` | 表意文字-数字 |
| KanjiDigit | `11` | 日语计数 |
| AiueoHalfWidth | `12` | Aiueo |
| IrohaHalfWidth | `13` | 伊吕波 |
| ArabicFullWidth | `14` | 全角阿拉伯语：1、2、3、4 |
| ArabicHalfWidth | `15` | 半角阿拉伯语：1、2、3、4 |
| KanjiTraditional | `16` | 日本合法 |
| KanjiTraditional2 | `17` | 日本数字万 |
| NumberInCircle | `18` | 封闭的圆圈 |
| DecimalFullWidth | `19` | 小数全角：1、2、3、4 |
| Aiueo | `20` | Aiueo 全宽 |
| Iroha | `21` | Iroha 全宽 |
| LeadingZero | `22` | 前导零（01、02、...、09、10、11、...、99、100、101、...） |
| Bullet | `23` | 项目符号（检查文本中的字符代码） |
| Ganada | `24` | 韩语 Ganada |
| Chosung | `25` | 朝鲜 |
| GB1 | `26` | 包含句号 |
| GB2 | `27` | 括号 |
| GB3 | `28` | 封闭的圆圈中文 |
| GB4 | `29` | 象形文字包围的圆圈 |
| Zodiac1 | `30` | 表意文字传统 |
| Zodiac2 | `31` | 象形文字十二宫 |
| Zodiac3 | `32` | 象形文字十二生肖传统 |
| TradChinNum1 | `33` | 台湾计数 |
| TradChinNum2 | `34` | 表意文字合法传统 |
| TradChinNum3 | `35` | 台湾人数千 |
| TradChinNum4 | `36` | 台湾数码 |
| SimpChinNum1 | `37` | 中国计数 |
| SimpChinNum2 | `38` | 简体中文合法 |
| SimpChinNum3 | `39` | 中国千数 |
| SimpChinNum4 | `40` | 中文（未实现） |
| HanjaRead | `41` | 韩语数字 |
| HanjaReadDigit | `42` | 韩语计数 |
| Hangul | `43` | 韩国合法 |
| Hanja | `44` | 韩国 digital2 |
| Hebrew1 | `45` | 希伯来语-1 |
| Arabic1 | `46` | 阿拉伯语 alpha |
| Hebrew2 | `47` | 希伯来语-2 |
| Arabic2 | `48` | 阿拉伯语辅音字母表 |
| HindiLetter1 | `49` | 印地语元音 |
| HindiLetter2 | `50` | 印地语辅音 |
| HindiArabic | `51` | 印地语数字 |
| HindiCardinalText | `52` | 印地语描述（基数） |
| ThaiLetter | `53` | 泰语字母 |
| ThaiArabic | `54` | 泰语数字 |
| ThaiCardinalText | `55` | 泰语描述（基数） |
| VietCardinalText | `56` | 越南语描述（基数） |
| NumberInDash | `57` | 页码格式：-1-、-2-、-3-、-4- |
| LowercaseRussian | `58` | 小写俄语字母 |
| UppercaseRussian | `59` | 大写俄语字母 |
| None | `255` | 没有项目符号或编号。 |
| Custom | `65280` | 自定义数字格式。仅 DOCX 格式支持。 |

## 例子

展示如何在使用 DocumentBuilder 时将自定义列表格式应用于段落。

```csharp
Document doc = new Document();

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集。
 // 我们可以通过增加缩进级别来创建嵌套列表。
 // 我们可以使用文档构建器的“ListFormat”属性来开始和结束列表。
// 我们在列表的开始和结束之间添加的每个段落都将成为列表中的一个项目。
// 从 Microsoft Word 模板创建列表，并自定义其列表级别的前两个。
List list = doc.Lists.Add(ListTemplate.NumberDefault);

ListLevel listLevel = list.ListLevels[0];
listLevel.Font.Color = Color.Red;
listLevel.Font.Size = 24;
listLevel.NumberStyle = NumberStyle.OrdinalText;
listLevel.StartAt = 21;
listLevel.NumberFormat = "\x0000";

listLevel.NumberPosition = -36;
listLevel.TextPosition = 144;
listLevel.TabPosition = 144;

listLevel = list.ListLevels[1];
listLevel.Alignment = ListLevelAlignment.Right;
listLevel.NumberStyle = NumberStyle.Bullet;
listLevel.Font.Name = "Wingdings";
listLevel.Font.Color = Color.Blue;
listLevel.Font.Size = 24;

// 此 NumberFormat 值将创建星形项目符号列表符号。
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// 创建段落并将我们的自定义列表格式的两个列表级别应用于它们。
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("The quick brown fox...");
builder.Writeln("The quick brown fox...");

builder.ListFormat.ListIndent();
builder.Writeln("jumped over the lazy dog.");
builder.Writeln("jumped over the lazy dog.");

builder.ListFormat.ListOutdent();
builder.Writeln("The quick brown fox...");

builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateCustomList.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
