---
title: ListLevel.IsLegal
linktitle: IsLegal
articleTitle: IsLegal
second_title: Aspose.Words لـ .NET
description: ListLevel IsLegal ملكية. صحيح إذا كان المستوى يحول جميع الأرقام الموروثة إلى اللغة العربية وخطأ إذا احتفظ بنمط أرقامها في C#.
type: docs
weight: 50
url: /ar/net/aspose.words.lists/listlevel/islegal/
---
## ListLevel.IsLegal property

صحيح إذا كان المستوى يحول جميع الأرقام الموروثة إلى اللغة العربية، وخطأ إذا احتفظ بنمط أرقامها.

```csharp
public bool IsLegal { get; set; }
```

## أمثلة

يعرض طرقًا متقدمة لتخصيص تسميات القائمة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات برموز البادئة والمسافات البادئة.
 // يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة.
 // يمكننا بدء القائمة وإنهائها باستخدام خاصية "ListFormat" الخاصة بمنشئ المستندات.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

// سيتم تنسيق تسميات المستوى 1 وفقًا لنمط الفقرة "العنوان 1" وستكون لها بادئة.
// ستبدو هذه مثل "الملحق أ" و"الملحق ب"...
list.ListLevels[0].NumberFormat = "Appendix \x0000";
list.ListLevels[0].NumberStyle = NumberStyle.UppercaseLetter;
list.ListLevels[0].LinkedStyle = doc.Styles["Heading 1"];

// ستعرض تسميات المستوى 2 الأرقام الحالية لمستويات القائمة الأولى والثانية ولها أصفار بادئة.
// إذا كان مستوى القائمة الأول عند 1، فستبدو تسميات القائمة مثل "القسم (1.01)"، "القسم (1.02)"...
list.ListLevels[1].NumberFormat = "Section (\x0000.\x0001)";
list.ListLevels[1].NumberStyle = NumberStyle.LeadingZero;

// لاحظ أن المستوى الأعلى يستخدم ترقيم الحروف الكبيرة.
// يمكننا ضبط الخاصية "IsLegal" لاستخدام الأرقام العربية لمستويات القائمة الأعلى.
list.ListLevels[1].IsLegal = true;
list.ListLevels[1].RestartAfterLevel = 0;

// ستكون تسميات المستوى 3 عبارة عن أرقام رومانية بأحرف كبيرة مع بادئة ولاحقة وسيتم إعادة تشغيلها عند كل عنصر من عناصر المستوى 1 في القائمة.
// ستبدو تسميات القائمة هذه بالشكل "-I-"، "-II-"...
list.ListLevels[2].NumberFormat = "-\x0002-";
list.ListLevels[2].NumberStyle = NumberStyle.UppercaseRoman;
list.ListLevels[2].RestartAfterLevel = 1;

// جعل التسميات لجميع مستويات القائمة جريئة.
foreach (ListLevel level in list.ListLevels)
    level.Font.Bold = true;

// تطبيق تنسيق القائمة على الفقرة الحالية.
builder.ListFormat.List = list;

// قم بإنشاء عناصر القائمة التي ستعرض مستويات القائمة الثلاثة جميعها.
for (int n = 0; n < 2; n++)
{
    for (int i = 0; i < 3; i++)
    {
        builder.ListFormat.ListLevelNumber = i;
        builder.Writeln("Level " + i);
    }
}

builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.CreateListRestartAfterHigher.docx");
```

### أنظر أيضا

* class [ListLevel](../)
* مساحة الاسم [Aspose.Words.Lists](../../../aspose.words.lists/)
* المجسم [Aspose.Words](../../../)
