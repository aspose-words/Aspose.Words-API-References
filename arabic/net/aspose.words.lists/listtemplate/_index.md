---
title: Enum ListTemplate
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Lists.ListTemplate تعداد. يحدد أحد تنسيقات القائمة المحددة مسبقًا والمتوفرة في Microsoft Word.
type: docs
weight: 3530
url: /ar/net/aspose.words.lists/listtemplate/
---
## ListTemplate enumeration

يحدد أحد تنسيقات القائمة المحددة مسبقًا والمتوفرة في Microsoft Word.

```csharp
public enum ListTemplate
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| BulletDefault | `0` | قائمة نقطية افتراضية مكونة من 9 مستويات. رمز نقطي للمستوى الأول عبارة عن قرص، رمز نقطي للمستوى الثاني عبارة عن دائرة، رمز نقطي للمستوى الثالث عبارة عن مربع. ثم يتم تكرار التنسيق للمستويات المتبقية. |
| BulletDisk | `0` | مثلBulletDefault. |
| BulletCircle | `1` | رصاصة المستوى الأول عبارة عن دائرة. المستويات المتبقية هي نفسها كما فيBulletDefault. |
| BulletSquare | `2` | رصاصة المستوى الأول مربعة. المستويات المتبقية هي نفسها كما فيBulletDefault. |
| BulletDiamonds | `3` | رصاصة المستوى الأول عبارة عن شخصية Wingding ذات 4 ماسات. المستويات المتبقية هي نفسها كما فيBulletDefault. |
| BulletArrowHead | `4` | رصاصة المستوى الأول هي حرف Wingding برأس سهم. المستويات المتبقية هي نفسها كما فيBulletDefault. |
| BulletTick | `5` | الرمز النقطي للمستوى الأول هو حرف Wingding. المستويات المتبقية هي نفسها كما فيBulletDefault. |
| NumberDefault | `6` | قائمة مرقمة افتراضية مع 9 مستويات. الترقيم العربي (1.، 2.، 3.، ...) للمستوى الأول، ترقيم الحروف الصغيرة (أ، ب، ج، ...) للمستوى الثاني، ترقيم روماني صغير (i) ., ii., iii., ...) للمستوى الثالث. ثم يتكرر التنسيق للمستويات المتبقية. |
| NumberArabicDot | `6` | مثلNumberDefault. |
| NumberArabicParenthesis | `7` | رقم المستوى الأول هو "1)". المستويات المتبقية هي نفسها كما فيNumberDefault. |
| NumberUppercaseRomanDot | `8` | رقم المستوى الأول هو "أنا". المستويات المتبقية هي نفسها كما فيNumberDefault. |
| NumberUppercaseLetterDot | `9` | رقم المستوى الأول هو "أ". المستويات المتبقية هي نفسها كما فيNumberDefault. |
| NumberLowercaseLetterParenthesis | `10` | رقم المستوى الأول هو "أ)". المستويات المتبقية هي نفسها كما فيNumberDefault. |
| NumberLowercaseLetterDot | `11` | رقم المستوى الأول هو "أ". المستويات المتبقية هي نفسها كما فيNumberDefault. |
| NumberLowercaseRomanDot | `12` | رقم المستوى الأول هو "i." المستويات المتبقية هي نفسها كما فيNumberDefault. |
| OutlineNumbers | `13` | قائمة تفصيلية بالمستويات المرقمة "1)، أ)، ط)، (1)، (أ)، (ط)، 1.، أ.، ط.". |
| OutlineLegal | `14` | يتم ترقيم قائمة المخطط التفصيلي بالمستويات "1.، 1.1.، 1.1.1، ...". |
| OutlineBullets | `15` | يسرد المخطط التفصيلي العديد من الرموز النقطية لمستويات مختلفة. |
| OutlineHeadingsArticleSection | `16` | قائمة مخطط تفصيلي تحتوي على مستويات مرتبطة بأنماط العناوين. |
| OutlineHeadingsLegal | `17` | قائمة مخطط تفصيلي تحتوي على مستويات مرتبطة بأنماط العناوين. |
| OutlineHeadingsNumbers | `18` | قائمة مخطط تفصيلي تحتوي على مستويات مرتبطة بأنماط العناوين. |
| OutlineHeadingsChapter | `19` | قائمة مخطط تفصيلي تحتوي على مستويات مرتبطة بأنماط العناوين. |

### ملاحظات

يتم استخدام قيمة قالب القائمة كمعلمة في the [`Add`](../listcollection/add/) طريقة.

تتوافق قوالب قائمة Aspose.Words مع قوالب القائمة الـ 21 المتوفرة في مربع حوار التعداد النقطي والترقيم في Microsoft Word 2003.

### أمثلة

يوضح كيفية إنشاء مستند يحتوي على كافة قوالب قائمة عناوين المخطط التفصيلي.

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

يوضح كيفية إعادة تشغيل الترقيم في القائمة عن طريق نسخ القائمة.

```csharp
Document doc = new Document();

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات برموز البادئة والمسافات البادئة.
 // يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة.
 // يمكننا بدء القائمة وإنهائها باستخدام خاصية "ListFormat" الخاصة بمنشئ المستندات.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// قم بإنشاء قائمة من قالب Microsoft Word، وقم بتخصيص مستوى القائمة الأول الخاص بها.
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

// يمكننا إضافة نسخة من القائمة الموجودة إلى مجموعة قائمة الوثيقة
// لإنشاء قائمة مماثلة دون إجراء تغييرات على القائمة الأصلية.
List list2 = doc.Lists.AddCopy(list1);
list2.ListLevels[0].Font.Color = Color.Blue;
list2.ListLevels[0].StartAt = 10;

// قم بتطبيق القائمة الثانية على فقرات جديدة.
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

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات برموز البادئة والمسافات البادئة.
 // يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة.
 // يمكننا بدء القائمة وإنهائها باستخدام خاصية "ListFormat" الخاصة بمنشئ المستندات.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// فيما يلي نوعان من القوائم التي يمكننا إنشاؤها باستخدام أداة إنشاء المستندات.
// 1 - قائمة مرقمة:
// تنشئ القوائم المرقمة ترتيبًا منطقيًا لفقراتها عن طريق ترقيم كل عنصر.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// من خلال تعيين خاصية "ListLevelNumber"، يمكننا زيادة مستوى القائمة
// لبدء قائمة فرعية قائمة بذاتها في عنصر القائمة الحالي.
// يستخدم قالب قائمة Microsoft Word المسمى "NumberDefault" الأرقام لإنشاء مستويات القائمة لمستوى القائمة الأول.
 // تستخدم مستويات القائمة الأعمق الحروف والأرقام الرومانية الصغيرة.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - قائمة ذات تعداد نقطي:
// ستطبق هذه القائمة مسافة بادئة ورمز نقطي ("•") قبل كل فقرة.
// ستستخدم المستويات الأعمق لهذه القائمة رموزًا مختلفة، مثل "■" و"○".
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// يمكننا تعطيل تنسيق القائمة لعدم تنسيق أي فقرات لاحقة كقوائم عن طريق إلغاء تعيين علامة "القائمة".
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Lists](../../aspose.words.lists/)
* المجسم [Aspose.Words](../../)


