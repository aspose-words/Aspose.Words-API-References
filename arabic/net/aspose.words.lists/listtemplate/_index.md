---
title: ListTemplate Enum
linktitle: ListTemplate
articleTitle: ListTemplate
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.Lists.ListTemplate، التي تتميز بتنسيقات قائمة Microsoft Word المحددة مسبقًا لتعزيز عرض مستندك بسهولة.
type: docs
weight: 3980
url: /ar/net/aspose.words.lists/listtemplate/
---
## ListTemplate enumeration

يحدد أحد تنسيقات القائمة المحددة مسبقًا والمتاحة في Microsoft Word.

```csharp
public enum ListTemplate
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| BulletDefault | `0` | قائمة نقطية افتراضية بتسعة مستويات. نقطة المستوى الأول قرص، ونقطة المستوى الثاني دائرة، ونقطة المستوى الثالث مربع. ثم يتكرر التنسيق للمستويات المتبقية. |
| BulletDisk | `0` | نفس الشيءBulletDefault. |
| BulletCircle | `1` | رصاصة المستوى الأول عبارة عن دائرة. المستويات المتبقية هي نفسها كما فيBulletDefault. |
| BulletSquare | `2` | رصاصة المستوى الأول مربعة الشكل. المستويات المتبقية كما فيBulletDefault. |
| BulletDiamonds | `3` | رصاصة المستوى الأول هي شخصية وينغ دينغ ذات الأربع ماسات. بقية المستويات هي نفسها فيBulletDefault. |
| BulletArrowHead | `4` | رصاصة المستوى الأول هي شخصية وينغ دينغ برأس سهم. بقية المستويات هي نفسها فيBulletDefault. |
| BulletTick | `5` | رصاصة المستوى الأول هي شخصية وينغ دينغ. بقية المستويات هي نفسها فيBulletDefault. |
| NumberDefault | `6` | قائمة مرقمة افتراضية تحتوي على 9 مستويات. الترقيم العربي (1، 2، 3، ...) للمستوى الأول، الترقيم بالأحرف الصغيرة (a.، b.، c.، ...) للمستوى الثاني، الترقيم بالأحرف الرومانية الصغيرة (i.، ii.، iii.، ...) للمستوى الثالث. ثم يتكرر التنسيق للمستويات المتبقية. |
| NumberArabicDot | `6` | نفس الشيءNumberDefault. |
| NumberArabicParenthesis | `7` | رقم المستوى الأول هو "1" والمستويات المتبقية كما فيNumberDefault. |
| NumberUppercaseRomanDot | `8` | رقم المستوى الأول هو "I". باقي المستويات هي نفسها كما فيNumberDefault. |
| NumberUppercaseLetterDot | `9` | رقم المستوى الأول هو "أ". باقي المستويات كما فيNumberDefault. |
| NumberLowercaseLetterParenthesis | `10` | رقم المستوى الأول هو "أ" والمستويات المتبقية هي نفسها كما فيNumberDefault. |
| NumberLowercaseLetterDot | `11` | رقم المستوى الأول هو "أ". باقي المستويات كما فيNumberDefault. |
| NumberLowercaseRomanDot | `12` | رقم المستوى الأول هو "i". باقي المستويات كما فيNumberDefault. |
| OutlineNumbers | `13` | قائمة تفصيلية تحتوي على مستويات مرقمة "1)، أ)، ي)، (1)، (أ)، (ي)، 1، أ، ي". |
| OutlineLegal | `14` | قائمة تفصيلية تحتوي على مستويات مرقمة "1.، 1.1.، 1.1.1، ...". |
| OutlineBullets | `15` | تحتوي القائمة على نقاط مختلفة لمستويات مختلفة. |
| OutlineHeadingsArticleSection | `16` | قائمة تفصيلية تحتوي على مستويات مرتبطة بأنماط العنوان. |
| OutlineHeadingsLegal | `17` | قائمة تفصيلية تحتوي على مستويات مرتبطة بأنماط العنوان. |
| OutlineHeadingsNumbers | `18` | قائمة تفصيلية تحتوي على مستويات مرتبطة بأنماط العنوان. |
| OutlineHeadingsChapter | `19` | قائمة تفصيلية تحتوي على مستويات مرتبطة بأنماط العنوان. |

## ملاحظات

يتم استخدام قيمة قالب القائمة كمعلمة في [`Add`](../listcollection/add/) طريقة.

تتوافق قوالب قائمة Aspose.Words مع قوالب القائمة الـ 21 المتوفرة في مربع الحوار النقاط والترقيم في Microsoft Word 2003.

## أمثلة

يوضح كيفية إنشاء مستند يحتوي على كافة قوالب قائمة العناوين التفصيلية.

```csharp
public void OutlineHeadingTemplates()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    List list = doc.Lists.Add(ListTemplate.OutlineHeadingsArticleSection);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Article Section\"");

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsLegal);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Legal\"");

    builder.InsertBreak(BreakType.PageBreak);

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsNumbers);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Numbers\"");

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsChapter);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Chapters\"");

    doc.Save(ArtifactsDir + "Lists.OutlineHeadingTemplates.docx");
}

private static void AddOutlineHeadingParagraphs(DocumentBuilder builder, List list, string title)
{
    builder.ParagraphFormat.ClearFormatting();
    builder.Writeln(title);

    for (int i = 0; i < 9; i++)
    {
        builder.ListFormat.List = list;
        builder.ListFormat.ListLevelNumber = i;

        string styleName = "Heading " + (i + 1);
        builder.ParagraphFormat.StyleName = styleName;
        builder.Writeln(styleName);
    }

    builder.ListFormat.RemoveNumbers();
}
```

يوضح كيفية إعادة تشغيل الترقيم في قائمة عن طريق نسخ القائمة.

```csharp
Document doc = new Document();

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات باستخدام رموز البادئة والمسافات البادئة.
 //يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة.
 // يمكننا أن نبدأ وننهي القائمة باستخدام خاصية "ListFormat" الموجودة في منشئ المستندات.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// قم بإنشاء قائمة من قالب Microsoft Word، ثم قم بتخصيص المستوى الأول من القائمة.
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// قم بتطبيق قائمتنا على بعض الفقرات.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("List 1 starts below:");
builder.ListFormat.List = list1;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// يمكننا إضافة نسخة من قائمة موجودة إلى مجموعة قوائم المستند
// لإنشاء قائمة مماثلة دون إجراء أي تغييرات على القائمة الأصلية.
List list2 = doc.Lists.AddCopy(list1);
list2.ListLevels[0].Font.Color = Color.Blue;
list2.ListLevels[0].StartAt = 10;

// قم بتطبيق القائمة الثانية على الفقرات الجديدة.
builder.Writeln("List 2 starts below:");
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.RestartNumberingUsingListCopy.docx");
```

يوضح كيفية العمل مع مستويات القائمة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات باستخدام رموز البادئة والمسافات البادئة.
 //يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة.
 // يمكننا أن نبدأ وننهي القائمة باستخدام خاصية "ListFormat" الموجودة في منشئ المستندات.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// فيما يلي نوعان من القوائم التي يمكننا إنشاؤها باستخدام منشئ المستندات.
// 1 - قائمة مرقمة:
// تقوم القوائم المرقمة بإنشاء ترتيب منطقي لفقراتها عن طريق ترقيم كل عنصر.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// من خلال تعيين خاصية "ListLevelNumber"، يمكننا زيادة مستوى القائمة
// لبدء قائمة فرعية مستقلة عند عنصر القائمة الحالي.
// يستخدم قالب قائمة Microsoft Word المسمى "NumberDefault" الأرقام لإنشاء مستويات القائمة للمستوى الأول من القائمة.
 // تستخدم مستويات القائمة الأعمق الأحرف والأرقام الرومانية الصغيرة.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - قائمة نقطية:
// ستطبق هذه القائمة مسافة بادئة ورمز نقطي ("•") قبل كل فقرة.
// ستستخدم المستويات الأعمق من هذه القائمة رموزًا مختلفة، مثل "■" و"○".
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// يمكننا تعطيل تنسيق القائمة لعدم تنسيق أي فقرات لاحقة كقوائم عن طريق إلغاء تعيين علم "القائمة".
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Lists](../../aspose.words.lists/)
* المجسم [Aspose.Words](../../)
