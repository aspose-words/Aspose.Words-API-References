---
title: Font.HasDmlEffect
linktitle: HasDmlEffect
articleTitle: HasDmlEffect
second_title: Aspose.Words لـ .NET
description: اكتشف ما إذا كان تأثير نص DrawingML مُطبّقًا باستخدام طريقة Font HasDmlEffect. حسّن مظهر مستندك البصري بسهولة!
type: docs
weight: 570
url: /ar/net/aspose.words/font/hasdmleffect/
---
## Font.HasDmlEffect method

يتحقق مما إذا كان يتم تطبيق تأثير نص DrawingML معين.

```csharp
public bool HasDmlEffect(TextDmlEffect dmlEffectType)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| dmlEffectType | TextDmlEffect | نوع تأثير النص DrawingML. |

### قيمة الإرجاع

`حقيقي` إذا تم تطبيق تأثير نص DrawingML معين.

## أمثلة

يوضح كيفية التحقق مما إذا كان التشغيل يعرض تأثير نص DrawingML.

```csharp
Document doc = new Document(MyDir + "DrawingML text effects.docx");

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.True(runs[0].Font.HasDmlEffect(TextDmlEffect.Shadow));
Assert.True(runs[1].Font.HasDmlEffect(TextDmlEffect.Shadow));
Assert.True(runs[2].Font.HasDmlEffect(TextDmlEffect.Reflection));
Assert.True(runs[3].Font.HasDmlEffect(TextDmlEffect.Effect3D));
Assert.True(runs[4].Font.HasDmlEffect(TextDmlEffect.Fill));
```

### أنظر أيضا

* enum [TextDmlEffect](../../textdmleffect/)
* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
