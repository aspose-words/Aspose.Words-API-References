---
title: HtmlInsertOptions Enum
linktitle: HtmlInsertOptions
articleTitle: HtmlInsertOptions
second_title: Aspose.Words لـ .NET
description: استكشف Aspose.Words.HtmlInsertOptions لتخصيص إدراج HTML باستخدام طريقة InsertHtml، مما يعزز كفاءة معالجة المستندات.
type: docs
weight: 3570
url: /ar/net/aspose.words/htmlinsertoptions/
---
## HtmlInsertOptions enumeration

يحدد الخيارات لـ[`InsertHtml`](../documentbuilder/inserthtml/) الطريقة.

```csharp
[Flags]
public enum HtmlInsertOptions
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | استخدم الخيارات الافتراضية عند إدراج HTML. |
| UseBuilderFormatting | `1` | استخدم تنسيق الخط والفقرة المحدد في[`DocumentBuilder`](../documentbuilder/) كتنسيق أساسي لـ text المدرج من HTML. |
| RemoveLastEmptyParagraph | `2` | قم بإزالة الفقرة الفارغة التي يتم إدراجها عادةً بعد HTML والتي تنتهي بعنصر على مستوى الكتلة. |
| PreserveBlocks | `4` | الحفاظ على خصائص عناصر مستوى الكتلة. |

## أمثلة

يوضح كيفية الحفاظ على الحدود والهوامش المرئية بشكل أفضل.

```csharp
const string html = @"
    <html>
        <div style='border:dotted'>
        <div style='border:solid'>
            <p>paragraph 1</p>
            <p>paragraph 2</p>
        </div>
        </div>
    </html>";

// تعيين الوضع الجديد لاستيراد عناصر مستوى كتلة HTML.
HtmlInsertOptions insertOptions = HtmlInsertOptions.PreserveBlocks;

DocumentBuilder builder = new DocumentBuilder();
builder.InsertHtml(html, insertOptions);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.PreserveBlocks.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
