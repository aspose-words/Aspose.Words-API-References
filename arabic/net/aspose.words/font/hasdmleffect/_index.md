---
title: Font.HasDmlEffect
second_title: Aspose.Words لمراجع .NET API
description: Font طريقة. للتحقق من تطبيق تأثير نص معين لـ DrawML.
type: docs
weight: 560
url: /ar/net/aspose.words/font/hasdmleffect/
---
## Font.HasDmlEffect method

للتحقق من تطبيق تأثير نص معين لـ DrawML.

```csharp
public bool HasDmlEffect(TextDmlEffect dmlEffectType)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| dmlEffectType | TextDmlEffect | نوع تأثير النص DrawML. |

### قيمة الإرجاع

`حقيقي` إذا تم تطبيق تأثير نص معين لـ DrawML.

### أمثلة

يوضح كيفية التحقق مما إذا كان التشغيل يعرض تأثير نص DrawML.

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
* مساحة الاسم [Aspose.Words](../../font/)
* المجسم [Aspose.Words](../../../)


