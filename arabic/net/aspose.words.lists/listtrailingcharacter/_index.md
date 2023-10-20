---
title: ListTrailingCharacter Enum
linktitle: ListTrailingCharacter
articleTitle: ListTrailingCharacter
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Lists.ListTrailingCharacter تعداد. يحدد الحرف الذي يفصل تسمية القائمة عن نص الفقرة في C#.
type: docs
weight: 3540
url: /ar/net/aspose.words.lists/listtrailingcharacter/
---
## ListTrailingCharacter enumeration

يحدد الحرف الذي يفصل تسمية القائمة عن نص الفقرة.

```csharp
public enum ListTrailingCharacter
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Tab | `0` | يتم وضع حرف جدولة بين تسمية القائمة ونص الفقرة. |
| Space | `1` | يتم وضع مسافة بين عنوان القائمة ونص الفقرة. |
| Nothing | `2` | لا يوجد حرف فاصل بين تسمية القائمة ونص الفقرة. |

## ملاحظات

تستخدم كقيمة ل[`TrailingCharacter`](../listlevel/trailingcharacter/) ملكية.

## أمثلة

يوضح كيفية تطبيق تنسيق القائمة المخصصة على الفقرات عند استخدام DocumentBuilder.

```csharp
Document doc = new Document();

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات برموز البادئة والمسافات البادئة.
 // يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة.
 // يمكننا بدء القائمة وإنهائها باستخدام خاصية "ListFormat" الخاصة بمنشئ المستندات.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// أنشئ قائمة من قالب Microsoft Word، وقم بتخصيص المستويين الأولين من قائمتها.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

ListLevel listLevel = list.ListLevels[0];
listLevel.Font.Color = Color.Red;
listLevel.Font.Size = 24;
listLevel.NumberStyle = NumberStyle.OrdinalText;
listLevel.StartAt = 21;
listLevel.NumberFormat = "\x0000";

listLevel.NumberPosition = -36;
listLevel.TextPosition = 144;
listLevel.TabPosition = 144;

listLevel = list.ListLevels[1];
listLevel.Alignment = ListLevelAlignment.Right;
listLevel.NumberStyle = NumberStyle.Bullet;
listLevel.Font.Name = "Wingdings";
listLevel.Font.Color = Color.Blue;
listLevel.Font.Size = 24;

// ستعمل قيمة NumberFormat هذه على إنشاء رموز قائمة نقطية على شكل نجمة.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// قم بإنشاء فقرات وتطبيق كلا مستويي القائمة بتنسيق القائمة المخصص لدينا عليها.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("The quick brown fox...");
builder.Writeln("The quick brown fox...");

builder.ListFormat.ListIndent();
builder.Writeln("jumped over the lazy dog.");
builder.Writeln("jumped over the lazy dog.");

builder.ListFormat.ListOutdent();
builder.Writeln("The quick brown fox...");

builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateCustomList.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Lists](../../aspose.words.lists/)
* المجسم [Aspose.Words](../../)
