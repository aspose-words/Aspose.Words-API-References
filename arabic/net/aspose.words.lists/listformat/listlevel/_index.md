---
title: ListFormat.ListLevel
linktitle: ListLevel
articleTitle: ListLevel
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ListFormat ListLevel لتحسين بنية مستندك باستخدام تنسيق القائمة القابل للتخصيص وتجاوزات الفقرات لتحقيق وضوح أفضل.
type: docs
weight: 30
url: /ar/net/aspose.words.lists/listformat/listlevel/
---
## ListFormat.ListLevel property

يعيد تنسيق مستوى القائمة بالإضافة إلى أي تجاوزات تنسيق يتم تطبيقها على الفقرة الحالية.

```csharp
public ListLevel ListLevel { get; }
```

## أمثلة

يوضح كيفية تطبيق تنسيق القائمة المخصصة على الفقرات عند استخدام DocumentBuilder.

```csharp
Document doc = new Document();

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات باستخدام رموز البادئة والمسافات البادئة.
 //يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة.
 // يمكننا أن نبدأ وننهي القائمة باستخدام خاصية "ListFormat" الموجودة في منشئ المستندات.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// قم بإنشاء قائمة من قالب Microsoft Word، ثم قم بتخصيص المستويين الأولين من القائمة.
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

// ستقوم قيمة NumberFormat هذه بإنشاء رموز قائمة نقطية على شكل نجمة.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// قم بإنشاء فقرات ثم قم بتطبيق مستويي القائمة لتنسيق القائمة المخصصة عليها.
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

* class [ListLevel](../../listlevel/)
* class [ListFormat](../)
* مساحة الاسم [Aspose.Words.Lists](../../../aspose.words.lists/)
* المجسم [Aspose.Words](../../../)
