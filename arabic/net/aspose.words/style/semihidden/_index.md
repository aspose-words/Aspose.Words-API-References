---
title: Style.SemiHidden
linktitle: SemiHidden
articleTitle: SemiHidden
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تتحكم الخاصية SemiHidden في رؤية النمط في معرض الأنماط وجزء المهام، مما يعزز سير عمل التصميم لديك وكفاءته.
type: docs
weight: 170
url: /ar/net/aspose.words/style/semihidden/
---
## Style.SemiHidden property

يحصل/يحدد ما إذا كان النمط مخفيًا من معرض الأنماط ومن جزء مهام الأنماط.

```csharp
public bool SemiHidden { get; set; }
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
