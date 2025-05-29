---
title: SdtAppearance Enum
linktitle: SdtAppearance
articleTitle: SdtAppearance
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Markup.SdtAppearance enum لتخصيص مظهر علامات المستندات المنظمة. حسّن تنسيق مستندك بسهولة!
type: docs
weight: 4680
url: /ar/net/aspose.words.markup/sdtappearance/
---
## SdtAppearance enumeration

يحدد مظهر علامة المستند المنظمة.

```csharp
public enum SdtAppearance
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| BoundingBox | `0` | يمثل علامة مستند منظمة تظهر على شكل مستطيل مظلل أو مربع محيط. |
| Tags | `1` | يمثل علامة مستند منظمة تظهر كعلامات بداية ونهاية. |
| Hidden | `2` | يمثل علامة مستند منظمة غير معروضة. |
| Default | `0` | الافتراضي هوBoundingBox . |

## أمثلة

يوضح كيفية إظهار العلامة حول المحتوى.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");
StructuredDocumentTagRangeStart tag =
    doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true) as StructuredDocumentTagRangeStart;

if (tag.Appearance == SdtAppearance.Hidden)
    tag.Appearance = SdtAppearance.Tags;
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup/)
* المجسم [Aspose.Words](../../)
