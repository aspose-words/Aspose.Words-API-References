---
title: Section.PrependContent
second_title: Aspose.Words لمراجع .NET API
description: Section طريقة. إدراج نسخة من محتوى القسم المصدر في بداية هذا القسم.
type: docs
weight: 160
url: /ar/net/aspose.words/section/prependcontent/
---
## Section.PrependContent method

إدراج نسخة من محتوى القسم المصدر في بداية هذا القسم.

```csharp
public void PrependContent(Section sourceSection)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| sourceSection | Section | القسم المراد نسخ المحتوى منه. |

### ملاحظات

محتوى فقط[`Body`](../body/) تم نسخ القسم المصدر، ولم يتم نسخ إعداد الصفحة، الرؤوس والتذييلات.

يتم استيراد العقد تلقائيًا إذا كان القسم المصدر ينتمي إلى مستند مختلف.

لم يتم إنشاء أي قسم جديد في المستند الوجهة.

### أمثلة

يوضح كيفية إلحاق محتويات قسم بقسم آخر.

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

// أدخل محتويات القسم الأول في بداية القسم الثالث.
Section sectionToPrepend = doc.Sections[0];
section.PrependContent(sectionToPrepend);

// أدخل محتويات القسم الثاني في نهاية القسم الثالث.
Section sectionToAppend = doc.Sections[1];
section.AppendContent(sectionToAppend);

// لم تنشئ طريقتا "PrependContent" و"AppendContent" أي أقسام جديدة.
Assert.AreEqual(3, doc.Sections.Count);
Assert.AreEqual("Section 1" + ControlChar.ParagraphBreak +
                "Section 3" + ControlChar.ParagraphBreak +
                "Section 2" + ControlChar.SectionBreak, section.GetText());
```

### أنظر أيضا

* class [Section](../)
* مساحة الاسم [Aspose.Words](../../section/)
* المجسم [Aspose.Words](../../../)


