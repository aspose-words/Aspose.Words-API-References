---
title: TextWrapping Enum
linktitle: TextWrapping
articleTitle: TextWrapping
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Aspose.Words.Tables.TextWrapping لتغليف النصوص بكفاءة حول الجداول. حسّن تنسيق مستنداتك بسهولة!
type: docs
weight: 7230
url: /ar/net/aspose.words.tables/textwrapping/
---
## TextWrapping enumeration

يحدد كيفية لف النص حول الجدول.

```csharp
public enum TextWrapping
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | يتم عرض النص والجدول حسب ترتيب ظهورهما في المستند. |
| Around | `1` | يتم لف النص حول الجدول ويشغل المساحة الجانبية المتاحة. |
| Default | `0` | القيمة الافتراضية. |

## أمثلة

يوضح كيفية العمل مع التفاف نص الجدول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

builder.Font.Size = 16;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// قم بتعيين خاصية "TextWrapping" إلى "TextWrapping.Around" لجعل الجدول يلتف حول النص،
// ثم ادفعه إلى الأسفل في الفقرة أدناه عن طريق تعيين الموضع.
table.TextWrapping = TextWrapping.Around;
table.AbsoluteHorizontalDistance = 100;
table.AbsoluteVerticalDistance = 20;

doc.Save(ArtifactsDir + "Table.WrapText.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Tables](../../aspose.words.tables/)
* المجسم [Aspose.Words](../../)
