---
title: Section.AppendContent
linktitle: AppendContent
articleTitle: AppendContent
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل طريقة AppendContent على تعزيز أقسامك من خلال إضافة محتوى المصدر بسلاسة، وتعزيز التنظيم والوضوح في مشاريعك.
type: docs
weight: 100
url: /ar/net/aspose.words/section/appendcontent/
---
## Section.AppendContent method

يقوم بإدراج نسخة من محتوى قسم المصدر في نهاية هذا القسم.

```csharp
public void AppendContent(Section sourceSection)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| sourceSection | Section | القسم الذي سيتم نسخ المحتوى منه. |

## ملاحظات

المحتوى فقط[`Body`](../body/) تم نسخ قسم المصدر، وإعداد الصفحة، ورؤوس الصفحات وتذييلاتها لم يتم نسخها.

سيتم استيراد العقد تلقائيًا إذا كان قسم المصدر ينتمي إلى مستند مختلف.

لم يتم إنشاء قسم جديد في المستند الوجهة.

## أمثلة

يوضح كيفية إضافة محتويات قسم إلى قسم آخر.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

Section section = doc.Sections[2];

Assert.AreEqual("Section 3" + ControlChar.SectionBreak, section.GetText());

//أدخل محتويات القسم الأول في بداية القسم الثالث.
Section sectionToPrepend = doc.Sections[0];
section.PrependContent(sectionToPrepend);

//أدخل محتويات القسم الثاني إلى نهاية القسم الثالث.
Section sectionToAppend = doc.Sections[1];
section.AppendContent(sectionToAppend);

// لم تقم طريقتي "PrependContent" و"AppendContent" بإنشاء أي أقسام جديدة.
Assert.AreEqual(3, doc.Sections.Count);
Assert.AreEqual("Section 1" + ControlChar.ParagraphBreak +
                "Section 3" + ControlChar.ParagraphBreak +
                "Section 2" + ControlChar.SectionBreak, section.GetText());
```

### أنظر أيضا

* class [Section](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
