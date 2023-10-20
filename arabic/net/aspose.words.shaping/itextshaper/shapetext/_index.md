---
title: ITextShaper.ShapeText
linktitle: ShapeText
articleTitle: ShapeText
second_title: Aspose.Words لـ .NET
description: ITextShaper ShapeText طريقة. إرجاعClusterالكائنات التي تم إنشاؤها من تسلسل أجزاء النص. طول المصفوفة التي تم إرجاعها يساوي طولruns . إذا تم التشغيل على فهرس يحتوي على مجموعات مقابلة فسيتم تسجيل النتائج في نفس الفهرس في C#.
type: docs
weight: 10
url: /ar/net/aspose.words.shaping/itextshaper/shapetext/
---
## ITextShaper.ShapeText method

إرجاع[`Cluster`](../../cluster/)الكائنات التي تم إنشاؤها من تسلسل أجزاء النص. طول المصفوفة التي تم إرجاعها يساوي طول*runs* . إذا تم التشغيل على فهرس يحتوي على مجموعات مقابلة، فسيتم تسجيل النتائج في نفس الفهرس.

```csharp
public Cluster[][] ShapeText(string[] runs, Direction direction, UnicodeScript script, 
    params FontFeature[] fontFeatures)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| runs | String[] | تسلسل أجزاء النص |
| direction | Direction | اتجاه النص |
| script | UnicodeScript | السيناريو |
| fontFeatures | FontFeature[] | مجموعة من الميزات للنظر فيها |

### أنظر أيضا

* class [Cluster](../../cluster/)
* enum [Direction](../../direction/)
* enum [UnicodeScript](../../unicodescript/)
* enum [FontFeature](../../fontfeature/)
* interface [ITextShaper](../)
* مساحة الاسم [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* المجسم [Aspose.Words](../../../)
