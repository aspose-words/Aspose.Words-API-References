---
title: PageSetup.SuppressEndnotes
linktitle: SuppressEndnotes
articleTitle: SuppressEndnotes
second_title: Aspose.Words لـ .NET
description: PageSetup SuppressEndnotes ملكية. صحيح إذا تمت طباعة التعليقات الختامية في نهاية القسم التالي وهذا لا يمنع التعليقات الختامية. تتم طباعة التعليقات الختامية المحذوفة قبل التعليقات الختامية في هذا القسم في C#.
type: docs
weight: 410
url: /ar/net/aspose.words/pagesetup/suppressendnotes/
---
## PageSetup.SuppressEndnotes property

صحيح إذا تمت طباعة التعليقات الختامية في نهاية القسم التالي، وهذا لا يمنع التعليقات الختامية. تتم طباعة التعليقات الختامية المحذوفة قبل التعليقات الختامية في هذا القسم.

```csharp
public bool SuppressEndnotes { get; set; }
```

## أمثلة

يبين كيفية تخزين الحواشي الختامية في نهاية كل قسم، وتعديل مواضعها.

```csharp
public void SuppressEndnotes()
{
    Document doc = new Document();
    doc.RemoveAllChildren();

     // بشكل افتراضي، يقوم المستند بتجميع كافة التعليقات الختامية في نهايته.
    Assert.AreEqual(EndnotePosition.EndOfDocument, doc.EndnoteOptions.Position);

    // نستخدم خاصية "الموضع" لكائن "EndnoteOptions" الخاص بالمستند
     // لجمع الحواشي الختامية في نهاية كل قسم بدلاً من ذلك.
    doc.EndnoteOptions.Position = EndnotePosition.EndOfSection;

    InsertSectionWithEndnote(doc, "Section 1", "Endnote 1, will stay in section 1");
    InsertSectionWithEndnote(doc, "Section 2", "Endnote 2, will be pushed down to section 3");
    InsertSectionWithEndnote(doc, "Section 3", "Endnote 3, will stay in section 3");

    // أثناء جعل الأقسام تعرض الحواشي الختامية الخاصة بها، يمكننا تعيين علامة "SuppressEndnotes".
    // تحويل كائن "PageSetup" الخاص بالقسم إلى "صحيح" للعودة إلى السلوك الافتراضي وتمرير التعليقات الختامية الخاصة به
    // في القسم التالي.
    PageSetup pageSetup = doc.Sections[1].PageSetup;
    pageSetup.SuppressEndnotes = true;

    doc.Save(ArtifactsDir + "PageSetup.SuppressEndnotes.docx");
}

/// <summary>
/// إلحاق قسم بنص وتعليق ختامي للمستند.
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

* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
