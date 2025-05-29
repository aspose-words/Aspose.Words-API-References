---
title: WarningInfo.Source
linktitle: Source
articleTitle: Source
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية مصدر WarningInfo التي تكشف عن أصل التحذيرات، مما يعزز موثوقية تطبيقك وتجربة المستخدم.
type: docs
weight: 20
url: /ar/net/aspose.words/warninginfo/source/
---
## WarningInfo.Source property

يعيد مصدر التحذير.

```csharp
public WarningSource Source { get; }
```

## أمثلة

يوضح كيفية العمل مع مصدر التحذير.

```csharp
Document doc = new Document(MyDir + "Emphases markdown warning.docx");

WarningInfoCollection warnings = new WarningInfoCollection();
doc.WarningCallback = warnings;
doc.Save(ArtifactsDir + "DocumentBuilder.EmphasesWarningSourceMarkdown.md");

foreach (WarningInfo warningInfo in warnings)
{
    if (warningInfo.Source == WarningSource.Markdown)
        Assert.AreEqual("The (*, 0:11) cannot be properly written into Markdown.", warningInfo.Description);
}
```

### أنظر أيضا

* enum [WarningSource](../../warningsource/)
* class [WarningInfo](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
