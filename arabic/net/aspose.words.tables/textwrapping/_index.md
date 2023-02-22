---
title: Enum TextWrapping
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Tables.TextWrapping تعداد. يحدد كيفية التفاف النص حول الجدول.
type: docs
weight: 6080
url: /ar/net/aspose.words.tables/textwrapping/
---
## TextWrapping enumeration

يحدد كيفية التفاف النص حول الجدول.

```csharp
public enum TextWrapping
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | يتم عرض النص والجدول بترتيب ظهورهما في المستند. |
| Around | `1` | يتم لف النص حول الجدول ويشغل المساحة الجانبية المتاحة. |
| Default | `0` | القيمة الافتراضية . |

### أمثلة

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

// اضبط خاصية "TextWrapping" على "TextWrapping.Around" لجعل الجدول يلتف حول النص ،
// وادفعها لأسفل في الفقرة أدناه عن طريق تحديد الموضع.
table.TextWrapping = TextWrapping.Around;
table.AbsoluteHorizontalDistance = 100;
table.AbsoluteVerticalDistance = 20;

doc.Save(ArtifactsDir + "Table.WrapText.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Tables](../../aspose.words.tables/)
* المجسم [Aspose.Words](../../)


