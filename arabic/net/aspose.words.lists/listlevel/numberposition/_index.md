---
title: ListLevel.NumberPosition
second_title: Aspose.Words لمراجع .NET API
description: ListLevel ملكية. إرجاع أو تعيين موضع الرقم أو الرمز النقطي لمستوى القائمة بالنقاط.
type: docs
weight: 80
url: /ar/net/aspose.words.lists/listlevel/numberposition/
---
## ListLevel.NumberPosition property

إرجاع أو تعيين موضع الرقم أو الرمز النقطي لمستوى القائمة (بالنقاط).

```csharp
public double NumberPosition { get; set; }
```

### ملاحظات

`NumberPosition` يتوافق مع LeftIndent بالإضافة إلى FirstLineIndent للفقرة.

### أمثلة

يوضح كيفية تطبيق تنسيق قائمة مخصص على الفقرات عند استخدام DocumentBuilder.

```csharp
Document doc = new Document();

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات برموز بادئة ومسافات بادئة.
// يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة. 
// يمكننا بدء قائمة وإنهائها باستخدام خاصية "تنسيق القائمة" الخاصة بمنشئ المستندات. 
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// إنشاء قائمة من قالب Microsoft Word ، وتخصيص أول مستويين من القائمة.
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

// ستنشئ قيمة NumberFormat هذه رموز قائمة ذات تعداد نقطي على شكل نجمة.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// أنشئ فقرات وقم بتطبيق كلا مستويي القائمة لتنسيق قائمتنا المخصص عليها.
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

* class [ListLevel](../)
* مساحة الاسم [Aspose.Words.Lists](../../listlevel/)
* المجسم [Aspose.Words](../../../)


