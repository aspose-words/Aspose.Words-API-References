---
title: ListLevel.RestartAfterLevel
linktitle: RestartAfterLevel
articleTitle: RestartAfterLevel
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ListLevel RestartAfterLevel لإدارة ترقيم القوائم في مستنداتك بسهولة. بسّط التنظيم وحسّن الوضوح اليوم!
type: docs
weight: 100
url: /ar/net/aspose.words.lists/listlevel/restartafterlevel/
---
## ListLevel.RestartAfterLevel property

تعيين أو إرجاع مستوى القائمة الذي يجب أن يظهر قبل إعادة تشغيل الترقيم بمستوى القائمة المحدد.

```csharp
public int RestartAfterLevel { get; set; }
```

## ملاحظات

قيمة -1 تعني أن الترقيم سيستمر.

## أمثلة

يعرض طرقًا متقدمة لتخصيص تسميات القائمة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات باستخدام رموز البادئة والمسافات البادئة.
 //يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة.
 // يمكننا أن نبدأ وننهي القائمة باستخدام خاصية "ListFormat" الموجودة في منشئ المستندات.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

// سيتم تنسيق تسميات المستوى 1 وفقًا لنمط الفقرة "العنوان 1" وسيكون لها بادئة.
//ستبدو مثل "الملحق أ"، "الملحق ب"...
list.ListLevels[0].NumberFormat = "Appendix \x0000";
list.ListLevels[0].NumberStyle = NumberStyle.UppercaseLetter;
list.ListLevels[0].LinkedStyle = doc.Styles["Heading 1"];

// ستعرض تسميات المستوى 2 الأرقام الحالية لمستويات القائمة الأولى والثانية وتحتوي على أصفار رئيسية.
// إذا كان مستوى القائمة الأول عند 1، فستبدو تسميات القائمة من هذه المستويات مثل "القسم (1.01)"، "القسم (1.02)"...
list.ListLevels[1].NumberFormat = "Section (\x0000.\x0001)";
list.ListLevels[1].NumberStyle = NumberStyle.LeadingZero;

// لاحظ أن المستوى الأعلى يستخدم ترقيم الأحرف الكبيرة.
// يمكننا تعيين خاصية "IsLegal" لاستخدام الأرقام العربية لمستويات القائمة الأعلى.
list.ListLevels[1].IsLegal = true;
list.ListLevels[1].RestartAfterLevel = 0;

// ستكون تسميات المستوى 3 عبارة عن أرقام رومانية بأحرف كبيرة مع بادئة ولاحقة وسيتم إعادة التشغيل عند كل عنصر من عناصر القائمة على المستوى 1.
// ستبدو تسميات القائمة هذه مثل "-I-"، "-II-"...
list.ListLevels[2].NumberFormat = "-\x0002-";
list.ListLevels[2].NumberStyle = NumberStyle.UppercaseRoman;
list.ListLevels[2].RestartAfterLevel = 1;

// اجعل علامات جميع مستويات القائمة غامقة.
foreach (ListLevel level in list.ListLevels)
    level.Font.Bold = true;

// تطبيق تنسيق القائمة على الفقرة الحالية.
builder.ListFormat.List = list;

// قم بإنشاء عناصر القائمة التي ستعرض جميع مستويات القائمة الثلاثة لدينا.
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
