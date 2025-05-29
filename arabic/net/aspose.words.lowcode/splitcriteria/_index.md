---
title: SplitCriteria Enum
linktitle: SplitCriteria
articleTitle: SplitCriteria
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.LowCode.SplitCriteria enum لتقسيم مستندات فعّال. حسّن سير عملك مع خيارات متعددة لإدارة الأجزاء بسلاسة.
type: docs
weight: 4400
url: /ar/net/aspose.words.lowcode/splitcriteria/
---
## SplitCriteria enumeration

يحدد كيفية تقسيم المستند إلى أجزاء.

```csharp
public enum SplitCriteria
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Page | `0` | يحدد أن المستند مقسم إلى صفحات. |
| SectionBreak | `1` | يحدد أن المستند مقسم إلى أجزاء عند فاصل القسم من أي نوع. |
| Style | `2` | يحدد أن المستند مقسم إلى أجزاء في فقرة منسقة باستخدام النمط المحدد في[`SplitStyle`](../splitoptions/splitstyle/) . |

## أمثلة

يوضح كيفية تقسيم المستند حسب الصفحات.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../)
