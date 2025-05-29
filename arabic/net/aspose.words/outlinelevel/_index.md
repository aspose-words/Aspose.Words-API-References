---
title: OutlineLevel Enum
linktitle: OutlineLevel
articleTitle: OutlineLevel
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.OutlineLevel enum لإدارة مستويات مخطط الفقرة في مستنداتك بسهولة لتحسين التنظيم والوضوح.
type: docs
weight: 5060
url: /ar/net/aspose.words/outlinelevel/
---
## OutlineLevel enumeration

يحدد مستوى المخطط التفصيلي للفقرة في المستند.

```csharp
public enum OutlineLevel
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Level1 | `0` | الفقرة موجودة في مستوى المخطط التفصيلي 1 (المستوى الأعلى). |
| Level2 | `1` | الفقرة موجودة في مستوى المخطط التفصيلي 2. |
| Level3 | `2` | الفقرة موجودة في مستوى المخطط التفصيلي 3. |
| Level4 | `3` | الفقرة موجودة في مستوى المخطط التفصيلي 4. |
| Level5 | `4` | الفقرة موجودة في مستوى المخطط التفصيلي 5. |
| Level6 | `5` | الفقرة موجودة في مستوى المخطط التفصيلي 6. |
| Level7 | `6` | الفقرة موجودة في مستوى المخطط التفصيلي 7. |
| Level8 | `7` | الفقرة موجودة في مستوى المخطط التفصيلي 8. |
| Level9 | `8` | الفقرة موجودة في مستوى المخطط التفصيلي 9. |
| BodyText | `9` | الفقرة موجودة على مستوى النص الرئيسي. |

## أمثلة

يوضح كيفية تكوين مستويات مخطط الفقرة لإنشاء نص قابل للطي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تحتوي كل فقرة على OutlineLevel، والذي يمكن أن يكون أي رقم من 1 إلى 9، أو قيمة "BodyText" الافتراضية.
// سيؤدي تعيين الخاصية إلى إحدى القيم المرقمة إلى إظهار سهم إلى اليسار
// من بداية الفقرة.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level1;
builder.Writeln("Paragraph outline level 1.");

// المستوى ١ هو المستوى الأعلى. إذا كانت هناك فقرة ذات مستوى أدنى أسفل فقرة ذات مستوى أعلى،
// سيؤدي انهيار الفقرة ذات المستوى الأعلى إلى انهيار الفقرة ذات المستوى الأدنى.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level2;
builder.Writeln("Paragraph outline level 2.");

// لن تنهار فقرتان من نفس المستوى مع بعضهما البعض،
// والسهام لا تنهار الفقرات التي تشير إليها.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level3;
builder.Writeln("Paragraph outline level 3.");
builder.Writeln("Paragraph outline level 3.");

// القيمة الافتراضية لـ "BodyText" هي الأدنى، والتي يمكن لفقرة من أي مستوى أن تنهار عندها.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.BodyText;
builder.Writeln("Paragraph at main text level.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphOutlineLevel.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
