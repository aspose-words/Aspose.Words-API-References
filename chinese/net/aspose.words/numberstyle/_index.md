---
title: Enum NumberStyle
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.NumberStyle 枚举. 指定列表脚注和尾注页码的编号样式
type: docs
weight: 4310
url: /zh/net/aspose.words/numberstyle/
---
## NumberStyle enumeration

指定列表、脚注和尾注、页码的编号样式。

```csharp
public enum NumberStyle
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Arabic | `0` | 阿拉伯编号 (1, 2, 3, ...) |
| UppercaseRoman | `1` | 大写罗马字母（I、II、III、...） |
| LowercaseRoman | `2` | 小写罗马 (i, ii, iii, ...) |
| UppercaseLetter | `3` | 大写字母（A、B、C、...） |
| LowercaseLetter | `4` | 小写字母 (a, b, c, ...) |
| Ordinal | `5` | 序数（第 1、第 2、第 3、...） |
| Number | `6` | 编号（一、二、三……） |
| OrdinalText | `7` | 序数（文本）（第一、第二、第三……） |
| Hex | `8` | 十六进制：8、9、A、B、C、D、E、F、10、11、12 |
| ChicagoManual | `9` | 芝加哥风格手册：*、†、† |
| Kanji | `10` | 表意文字-数字 |
| KanjiDigit | `11` | 日本计数 |
| AiueoHalfWidth | `12` | Aiueo |
| IrohaHalfWidth | `13` | 伊吕波 |
| ArabicFullWidth | `14` | 全角阿拉伯语：1、2、3、4 |
| ArabicHalfWidth | `15` | 半角阿拉伯语：1, 2, 3, 4 |
| KanjiTraditional | `16` | 日本法律 |
| KanjiTraditional2 | `17` | 日本数字万 |
| NumberInCircle | `18` | 封闭圆圈 |
| DecimalFullWidth | `19` | 十进制全角：1, 2, 3, 4 |
| Aiueo | `20` | Aiueo 全宽 |
| Iroha | `21` | 伊吕波全幅 |
| LeadingZero | `22` | 前导零（01、02、...、09、10、11、...、99、100、101、...） |
| Bullet | `23` | 项目符号（检查文本中的字符代码） |
| Ganada | `24` | 韩国加纳达 |
| Chosung | `25` | 韩国朝鲜 |
| GB1 | `26` | 封闭式句号 |
| GB2 | `27` | 带括号 |
| GB3 | `28` | 封闭圆 中文 |
| GB4 | `29` | 表意文字封闭圆圈 |
| Zodiac1 | `30` | 表意文字传统 |
| Zodiac2 | `31` | 表意文字生肖 |
| Zodiac3 | `32` | 表意文字生肖传统 |
| TradChinNum1 | `33` | 台湾计数 |
| TradChinNum2 | `34` | 表意文字合法繁体 |
| TradChinNum3 | `35` | 台湾人数千 |
| TradChinNum4 | `36` | 台湾数码 |
| SimpChinNum1 | `37` | 中文计数 |
| SimpChinNum2 | `38` | 简体中文法律 |
| SimpChinNum3 | `39` | 中国数千 |
| SimpChinNum4 | `40` | 中文（未实现） |
| HanjaRead | `41` | 韩国数字 |
| HanjaReadDigit | `42` | 韩语计数 |
| Hangul | `43` | 韩国法律 |
| Hanja | `44` | 韩国digital2 |
| Hebrew1 | `45` | 希伯来语-1 |
| Arabic1 | `46` | 阿拉伯字母 |
| Hebrew2 | `47` | 希伯来语-2 |
| Arabic2 | `48` | 阿拉伯语 abjad |
| HindiLetter1 | `49` | 印地语元音 |
| HindiLetter2 | `50` | 印地语辅音 |
| HindiArabic | `51` | 印地语数字 |
| HindiCardinalText | `52` | 印地语描述性（红衣主教） |
| ThaiLetter | `53` | 泰语字母 |
| ThaiArabic | `54` | 泰国数字 |
| ThaiCardinalText | `55` | 泰语描述性（红衣主教） |
| VietCardinalText | `56` | 越南语描述性（红衣主教） |
| NumberInDash | `57` | 页码格式： - 1 -、 - 2 -、 - 3 -、 - 4 - |
| LowercaseRussian | `58` | 小写俄语字母 |
| UppercaseRussian | `59` | 大写俄语字母 |
| None | `255` | 无项目符号或编号。 |
| Custom | `65280` | 自定义数字格式。仅支持 DOCX 格式。 |

### 例子

演示如何在使用 DocumentBuilder 时将自定义列表格式应用于段落。

```csharp
Document doc = new Document();

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集。
 // 我们可以通过增加缩进级别来创建嵌套列表。
 // 我们可以使用文档构建器的“ListFormat”属性来开始和结束列表。
// 我们在列表的开头和结尾之间添加的每个段落都将成为列表中的一个项目。
// 从 Microsoft Word 模板创建列表，并自定义其列表的前两个级别。
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

// 创建段落并将自定义列表格式的两个列表级别应用到它们。
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


