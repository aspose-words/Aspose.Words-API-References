---
title: Enum HtmlInsertOptions
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.HtmlInsertOptions تعداد. يحدد خياراتInsertHtml الطريقة.
type: docs
weight: 3140
url: /ar/net/aspose.words/htmlinsertoptions/
---
## HtmlInsertOptions enumeration

يحدد خيارات[`InsertHtml`](../documentbuilder/inserthtml/) الطريقة.

```csharp
[Flags]
public enum HtmlInsertOptions
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | استخدم الخيارات الافتراضية عند إدراج HTML. |
| UseBuilderFormatting | `1` | استخدم تنسيق الخط والفقرة المحدد في[`DocumentBuilder`](../documentbuilder/) كتنسيق أساسي للنص المدرج من HTML. |
| RemoveLastEmptyParagraph | `2` | إزالة الفقرة الفارغة التي يتم إدراجها عادةً بعد HTML والتي تنتهي بعنصر على مستوى الكتلة. |
| PreserveBlocks | `4` | الحفاظ على خصائص العناصر على مستوى الكتلة. |

### أمثلة

يوضح كيفية الحفاظ على الحدود والهوامش بشكل أفضل.

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

// قم بتعيين الوضع الجديد لاستيراد عناصر مستوى كتلة HTML.
HtmlInsertOptions insertOptions = HtmlInsertOptions.PreserveBlocks;

DocumentBuilder builder = new DocumentBuilder();
builder.InsertHtml(html, insertOptions);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.PreserveBlocks.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


