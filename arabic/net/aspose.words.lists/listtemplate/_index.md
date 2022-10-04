---
title: ListTemplate
second_title: Aspose.Words لمراجع .NET API
description: تحديد أحد تنسيقات القائمة المحددة مسبقًا المتوفرة في Microsoft Word .
type: docs
weight: 3330
url: /ar/net/aspose.words.lists/listtemplate/
---
## ListTemplate enumeration

تحديد أحد تنسيقات القائمة المحددة مسبقًا المتوفرة في Microsoft Word .

```csharp
public enum ListTemplate
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| BulletDefault | `0` | قائمة نقطية افتراضية مع 9 مستويات. رمز المستوى الأول عبارة عن قرص ، رمز المستوى الثاني عبارة عن دائرة ، ورصاصة المستوى الثالث عبارة عن مربع. ثم يتكرر التنسيق للمستويات المتبقية. |
| BulletDisk | `0` | نفس BulletDefault. |
| BulletCircle | `1` | رصاصة المستوى الأول هي دائرة. المستويات المتبقية هي نفسها الموجودة في BulletDefault. |
| BulletSquare | `2` | رصاصة المستوى الأول مربع. المستويات المتبقية هي نفسها الموجودة في BulletDefault. |
| BulletDiamonds | `3` | رصاصة المستوى الأول هي شخصية جناح 4 ماسات. المستويات المتبقية هي نفسها الموجودة في BulletDefault. |
| BulletArrowHead | `4` | رمز المستوى الأول عبارة عن حرف جناح برأس سهم. المستويات المتبقية هي نفسها الموجودة في BulletDefault. |
| BulletTick | `5` | الرمز النقطي للمستوى الأول هو حرف جناح التجزئة. المستويات المتبقية هي نفسها الموجودة في BulletDefault. |
| NumberDefault | `6` | قائمة ذات تعداد رقمي افتراضي مع 9 مستويات. الترقيم العربي (1. ، 2. ، 3. ، ...) للمستوى الأول ، ترقيم الأحرف الصغيرة (a. ، b. ، c. ، ...) للمستوى الثاني ، ترقيم روماني صغير (i . ، ii. ، iii. ، ...) للمستوى الثالث. ثم يتكرر التنسيق للمستويات المتبقية. |
| NumberArabicDot | `6` | مثل NumberDefault. |
| NumberArabicParenthesis | `7` | رقم المستوى الأول هو "1)". المستويات المتبقية هي نفسها الموجودة في NumberDefault. |
| NumberUppercaseRomanDot | `8` | رقم المستوى الأول هو "I.". المستويات المتبقية هي نفسها الموجودة في NumberDefault. |
| NumberUppercaseLetterDot | `9` | رقم المستوى الأول هو "أ". المستويات المتبقية هي نفسها الموجودة في NumberDefault. |
| NumberLowercaseLetterParenthesis | `10` | رقم المستوى الأول هو "أ)". المستويات المتبقية هي نفسها الموجودة في NumberDefault. |
| NumberLowercaseLetterDot | `11` | رقم المستوى الأول هو "أ". المستويات المتبقية هي نفسها الموجودة في NumberDefault. |
| NumberLowercaseRomanDot | `12` | رقم المستوى الأول هو "أنا". المستويات المتبقية هي نفسها الموجودة في NumberDefault. |
| OutlineNumbers | `13` | قائمة مخطط تفصيلي بمستويات مرقمة "1) ، أ) ، ط) ، (1) ، (أ) ، (ط) ، 1. ، أ. ، ط". |
| OutlineLegal | `14` | يتم ترقيم قائمة المخطط التفصيلي مع المستويات "1. ، 1.1. ، 1.1.1 ، ...". |
| OutlineBullets | `15` | يسرد المخطط التفصيلي برموز نقطية مختلفة لمستويات مختلفة. |
| OutlineHeadingsArticleSection | `16` | قائمة مخطط تفصيلي بمستويات مرتبطة بأنماط العنوان. |
| OutlineHeadingsLegal | `17` | قائمة مخطط تفصيلي بمستويات مرتبطة بأنماط العنوان. |
| OutlineHeadingsNumbers | `18` | قائمة مخطط تفصيلي بمستويات مرتبطة بأنماط العنوان. |
| OutlineHeadingsChapter | `19` | قائمة مخطط تفصيلي بمستويات مرتبطة بأنماط العنوان. |

### ملاحظات

يتم استخدام قيمة قالب القائمة كمعامل في [`Add`](../listcollection/add/) طريقة.

تتوافق قوالب قائمة Aspose.Words مع قوالب القائمة الـ 21 المتوفرة في مربع حوار التعداد النقطي والرقمي في Microsoft Word 2003.

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

يوضح كيفية إعادة تشغيل الترقيم في قائمة عن طريق نسخ قائمة.

```csharp
Document doc = new Document();

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات برموز بادئة ومسافات بادئة.
// يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة. 
// يمكننا بدء قائمة وإنهائها باستخدام خاصية "تنسيق القائمة" الخاصة بمنشئ المستندات. 
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// أنشئ قائمة من قالب Microsoft Word ، وخصص مستوى القائمة الأول.
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

// يمكننا إضافة نسخة من قائمة موجودة إلى مجموعة قائمة المستندات
// لإنشاء قائمة مماثلة دون إجراء تغييرات على الأصل.
List list2 = doc.Lists.AddCopy(list1);
list2.ListLevels[0].Font.Color = Color.Blue;
list2.ListLevels[0].StartAt = 10;

// تطبيق القائمة الثانية على الفقرات الجديدة.
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

// تسمح لنا القائمة بتنظيم وتزيين مجموعات من الفقرات برموز بادئة ومسافات بادئة.
// يمكننا إنشاء قوائم متداخلة عن طريق زيادة مستوى المسافة البادئة. 
// يمكننا بدء قائمة وإنهائها باستخدام خاصية "تنسيق القائمة" الخاصة بمنشئ المستندات. 
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// يوجد أدناه نوعان من القوائم التي يمكننا إنشاؤها باستخدام أداة إنشاء المستندات.
// 1 - قائمة ذات تعداد رقمي:
// تقوم القوائم المرقمة بإنشاء ترتيب منطقي لفقراتها عن طريق ترقيم كل عنصر.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// من خلال تعيين خاصية "ListLevelNumber" ، يمكننا زيادة مستوى القائمة
// لبدء قائمة فرعية قائمة بذاتها في عنصر القائمة الحالي.
// يستخدم قالب قائمة Microsoft Word المسمى "NumberDefault" الأرقام لإنشاء مستويات القائمة لمستوى القائمة الأول.
// تستخدم مستويات القائمة الأعمق أحرفًا وأرقامًا رومانية صغيرة. 
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - قائمة نقطية:
// ستطبق هذه القائمة مسافة بادئة ورمز نقطي ("•") قبل كل فقرة.
// ستستخدم المستويات الأعمق من هذه القائمة رموزًا مختلفة ، مثل "■" و "".
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
