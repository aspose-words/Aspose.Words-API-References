---
title: ITextShaper.ShapeText
linktitle: ShapeText
articleTitle: ShapeText
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة ShapeText الخاصة بـ iTextShaper، والتي تقوم بإنشاء كائنات Cluster بكفاءة من أجزاء نصية، مما يضمن تنسيق النص ومحاذاته بدقة.
type: docs
weight: 10
url: /ar/net/aspose.words.shaping/itextshaper/shapetext/
---
## ITextShaper.ShapeText method

إرجاع[`Cluster`](../../cluster/)الكائنات التي تم إنشاؤها من تسلسل أجزاء النص. طول المصفوفة المرتجعة يساوي طول*runs* . إذا تم تشغيله عند فهرس يحتوي على مجموعات مقابلة، فإن النتيجة عند نفس الفهرس ستؤدي إلى تسجيلها.

```csharp
public Cluster[][] ShapeText(string[] runs, Direction direction, UnicodeScript script, 
    FontFeature[] enabledFontFeatures, VariationAxisCoordinate[] variations)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| runs | String[] | سلسلة من أجزاء النص |
| direction | Direction | اتجاه النص |
| script | UnicodeScript | نص |
| enabledFontFeatures | FontFeature[] | مجموعة من ميزات OpenType الممكّنة صراحةً للنظر فيها |
| variations | VariationAxisCoordinate[] | قيم محور تباين الخط |

### أنظر أيضا

* class [Cluster](../../cluster/)
* enum [Direction](../../direction/)
* enum [UnicodeScript](../../unicodescript/)
* enum [FontFeature](../../fontfeature/)
* class [VariationAxisCoordinate](../../variationaxiscoordinate/)
* interface [ITextShaper](../)
* مساحة الاسم [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* المجسم [Aspose.Words](../../../)
