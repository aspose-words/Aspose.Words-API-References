---
title: Style.Priority
linktitle: Priority
articleTitle: Priority
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية إدارة إعدادات أولوية الأنماط لتحسين فرز الأنماط في لوحة المهام. حسّن سير عملك من خلال تنظيم الأنماط بكفاءة!
type: docs
weight: 160
url: /ar/net/aspose.words/style/priority/
---
## Style.Priority property

يحصل على/يعين قيمة العدد الصحيح التي تمثل الأولوية لفرز الأنماط في جزء مهام الأنماط.

```csharp
public int Priority { get; set; }
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
