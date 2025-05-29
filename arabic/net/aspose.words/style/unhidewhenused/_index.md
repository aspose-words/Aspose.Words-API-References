---
title: Style.UnhideWhenUsed
linktitle: UnhideWhenUsed
articleTitle: UnhideWhenUsed
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية إدارة خاصية "إظهار عند الاستخدام" للأنماط. تحكّم في الرؤية في معرض الأنماط ولوحة المهام لتحسين تصميم مستندك.
type: docs
weight: 210
url: /ar/net/aspose.words/style/unhidewhenused/
---
## Style.UnhideWhenUsed property

يحصل/يحدد ما إذا كان النمط المستخدم في المستند الحالي يظهر من معرض الأنماط ومن جزء مهام الأنماط. صحيح عندما يجب إظهار النمط المستخدم في معرض الأنماط.

```csharp
public bool UnhideWhenUsed { get; set; }
```

## أمثلة

يوضح كيفية تحديد أولويات النمط وإخفائه.

```csharp
Document doc = new Document();
Style styleTitle = doc.Styles[StyleIdentifier.Subtitle];

if (styleTitle.Priority == 9)
    styleTitle.Priority = 10;

if (!styleTitle.UnhideWhenUsed)
    styleTitle.UnhideWhenUsed = true;

if (styleTitle.SemiHidden)
    styleTitle.SemiHidden = true;

doc.Save(ArtifactsDir + "Styles.StylePriority.docx");
```

### أنظر أيضا

* class [Style](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
