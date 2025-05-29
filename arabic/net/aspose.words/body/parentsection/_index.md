---
title: Body.ParentSection
linktitle: ParentSection
articleTitle: ParentSection
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Body ParentSection للوصول بسهولة إلى قسم الوالدين في القصة وتعزيز كفاءة إدارة المحتوى لديك.
type: docs
weight: 30
url: /ar/net/aspose.words/body/parentsection/
---
## Body.ParentSection property

يحصل على القسم الرئيسي لهذه القصة.

```csharp
public Section ParentSection { get; }
```

## ملاحظات

`ParentSection` يعادل[`ParentNode`](../../node/parentnode/) تم إلقاؤه إلى[`Section`](../../section/).

## أمثلة

يوضح كيفية تخزين الملاحظات الختامية في نهاية كل قسم، وتعديل مواقعها.

```csharp
public void SuppressEndnotes()
{
    Document doc = new Document();
    doc.RemoveAllChildren();

     // بشكل افتراضي، تقوم الوثيقة بتجميع كل الحواشي الختامية في نهايتها.
    Assert.AreEqual(EndnotePosition.EndOfDocument, doc.EndnoteOptions.Position);

    // نستخدم خاصية "Position" لكائن "EndnoteOptions" الخاص بالمستند
     //لتجميع الحواشي في نهاية كل قسم بدلاً من ذلك.
    doc.EndnoteOptions.Position = EndnotePosition.EndOfSection;

    InsertSectionWithEndnote(doc, "Section 1", "Endnote 1, will stay in section 1");
    InsertSectionWithEndnote(doc, "Section 2", "Endnote 2, will be pushed down to section 3");
    InsertSectionWithEndnote(doc, "Section 3", "Endnote 3, will stay in section 3");

    // أثناء جعل الأقسام تعرض ملاحظاتها الختامية الخاصة بها، يمكننا تعيين علامة "SuppressEndnotes"
    // لكائن "PageSetup" الخاص بالقسم إلى "true" للعودة إلى السلوك الافتراضي وتمرير الحواشي الختامية الخاصة به
    // إلى القسم التالي.
    PageSetup pageSetup = doc.Sections[1].PageSetup;
    pageSetup.SuppressEndnotes = true;

    doc.Save(ArtifactsDir + "PageSetup.SuppressEndnotes.docx");
}

/// <summary>
/// إضافة قسم يحتوي على نص وملاحظة ختامية إلى مستند.
/// </summary>
private static void InsertSectionWithEndnote(Document doc, string sectionBodyText, string endnoteText)
{
    Section section = new Section(doc);

    doc.AppendChild(section);

    Body body = new Body(doc);
    section.AppendChild(body);

    Assert.AreEqual(section, body.ParentNode);

    Paragraph para = new Paragraph(doc);
    body.AppendChild(para);

    Assert.AreEqual(body, para.ParentNode);

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.MoveTo(para);
    builder.Write(sectionBodyText);
    builder.InsertFootnote(FootnoteType.Endnote, endnoteText);
}
```

### أنظر أيضا

* class [Section](../../section/)
* class [Body](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
