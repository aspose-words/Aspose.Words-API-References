---
title: PatternType Enum
linktitle: PatternType
articleTitle: PatternType
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.Drawing.PatternType لتحسين أشكالك بأنماط تعبئة قابلة للتخصيص. ارتقِ بتصميم مستندك بسلاسة!
type: docs
weight: 1550
url: /ar/net/aspose.words.drawing/patterntype/
---
## PatternType enumeration

يحدد نمط التعبئة الذي سيتم استخدامه لملء الشكل.

```csharp
public enum PatternType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `-1` | لا يوجد نمط. |
| Percent10 | `1` | 10% من لون المقدمة. |
| Percent20 | `2` | 20% من لون المقدمة. |
| Percent25 | `3` | 25% من لون المقدمة. |
| Percent30 | `4` | 30% من لون المقدمة. |
| Percent40 | `5` | 40% من لون المقدمة |
| Percent50 | `6` | 50% من لون المقدمة |
| Percent5 | `7` | 5% من لون المقدمة. |
| Percent60 | `8` | 60% من لون المقدمة. |
| Percent70 | `9` | 70% من لون المقدمة. |
| Percent75 | `10` | 75% من لون المقدمة. |
| Percent80 | `11` | 80% من لون المقدمة. |
| Percent90 | `12` | 90% من لون المقدمة. |
| Cross | `13` | الصليب. |
| DarkDownwardDiagonal | `14` | قطري داكن متجه للأسفل. |
| DarkHorizontal | `15` | أفقي داكن. |
| DarkUpwardDiagonal | `16` | قطري داكن لأعلى. |
| DarkVertical | `17` | عمودي داكن. |
| DashedDownwardDiagonal | `18` | قطري متقطع لأسفل. |
| DashedHorizontal | `19` | أفقي متقطع. |
| DashedUpwardDiagonal | `20` | قطري متقطع صاعدًا. |
| DashedVertical | `21` | عمودي متقطع. |
| DiagonalBrick | `22` | طوبة قطرية. |
| DiagonalCross | `23` | صليب قطري. |
| Divot | `24` | نمط divot. |
| DottedDiamond | `25` | ماسة منقطه. |
| DottedGrid | `26` | شبكة منقطة. |
| DownwardDiagonal | `27` | قطريًا للأسفل. |
| Horizontal | `28` | أفقي. |
| HorizontalBrick | `29` | طوبة أفقية. |
| LargeCheckerBoard | `30` | رقعة شطرنج كبيرة. |
| LargeConfetti | `31` | قصاصات ورقية كبيرة. |
| LargeGrid | `32` | شبكة كبيرة. |
| LightDownwardDiagonal | `33` | ضوء قطري متجه للأسفل. |
| LightHorizontal | `34` | ضوء أفقي. |
| LightUpwardDiagonal | `36` | ضوء قطري صاعد. |
| LightVertical | `37` | ضوء عمودي. |
| NarrowHorizontal | `38` | أفقي ضيق. |
| NarrowVertical | `39` | عمودي ضيق. |
| OutlinedDiamond | `40` | ماسة محددة. |
| Plaid | `41` | منقوش. |
| Shingle | `42` | شينجل. |
| SmallCheckerBoard | `43` | رقعة شطرنج صغيرة. |
| SmallConfetti | `44` | قطع صغيرة من الورق الملون. |
| SmallGrid | `45` | شبكة صغيرة. |
| SolidDiamond | `46` | الماس الصلب. |
| Sphere | `47` | كرة. |
| Trellis | `48` | تعريشة. |
| UpwardDiagonal | `49` | قطريًا لأعلى. |
| Vertical | `50` | عمودي. |
| Wave | `51` | موجة. |
| Weave | `52` | نسج. |
| WideDownwardDiagonal | `53` | قطري عريض متجه للأسفل. |
| WideUpwardDiagonal | `54` | قطري عريض لأعلى. |
| ZigZag | `55` | متعرج. |

## أمثلة

يوضح كيفية تعيين نمط لشكل ما.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// هناك عدة طرق محددة لتعبئة النمط.
// 1 - تطبيق النمط على تعبئة الشكل:
fill.Patterned(PatternType.DiagonalBrick);

// 2 - تطبيق النمط بألوان المقدمة والخلفية على تعبئة الشكل:
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
