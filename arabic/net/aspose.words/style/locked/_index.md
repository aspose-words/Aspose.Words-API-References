---
title: Style.Locked
linktitle: Locked
articleTitle: Locked
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية قفل النمط، وتحكم في قفل النمط لتحسين مرونة التصميم واتساقه في مشاريعك. أطلق العنان لإبداعك اليوم!
type: docs
weight: 120
url: /ar/net/aspose.words/style/locked/
---
## Style.Locked property

يحدد ما إذا كان هذا النمط مقفلاً.

```csharp
public bool Locked { get; set; }
```

## أمثلة

يوضح كيفية قفل الأسلوب.

```csharp
Document doc = new Document();

Style styleHeading1 = doc.Styles[StyleIdentifier.Heading1];
if (!styleHeading1.Locked)
    styleHeading1.Locked = true;

doc.Save(ArtifactsDir + "Styles.LockStyle.docx");
```

### أنظر أيضا

* class [Style](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
