---
title: FieldNoteRef.InsertHyperlink
linktitle: InsertHyperlink
articleTitle: InsertHyperlink
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية InsertHyperlink في FieldNoteRef، وقم بإدارة إدراج الارتباط التشعبي بسهولة للفقرات المرجعية لتحسين تفاعلية مستندك.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldnoteref/inserthyperlink/
---
## FieldNoteRef.InsertHyperlink property

يحصل على أو يحدد ما إذا كان سيتم إدراج ارتباط تشعبي إلى الفقرة المرجعية.

```csharp
public bool InsertHyperlink { get; set; }
```

## أمثلة

يوضح كيفية إدراج حقول NOTEREF وتعديل مظهرها.

```csharp
public void FieldNoteRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // قم بإنشاء إشارة مرجعية تحتوي على حاشية سفلية سيشير إليها حقل NOTREF.
    InsertBookmarkWithFootnote(builder, "MyBookmark1", "Contents of MyBookmark1", "Footnote from MyBookmark1");

    // سيعرض حقل NOTEREF هذا رقم الحاشية السفلية داخل الإشارة المرجعية.
    // يتيح لنا تعيين خاصية InsertHyperlink الانتقال إلى الإشارة المرجعية عن طريق الضغط على Ctrl والنقر فوق الحقل في Microsoft Word.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h",
        InsertFieldNoteRef(builder, "MyBookmark2", true, false, false, "Hyperlink to Bookmark2, with footnote number ").GetFieldCode());

    // عند استخدام علامة \p، بعد رقم الحاشية السفلية، يعرض الحقل أيضًا موضع الإشارة المرجعية بالنسبة للحقل.
    // Bookmark1 يقع أعلى هذا الحقل ويحتوي على رقم الحاشية السفلية 1، لذا ستكون النتيجة "1 أعلى" عند التحديث.
    Assert.AreEqual(" NOTEREF  MyBookmark1 \\h \\p",
        InsertFieldNoteRef(builder, "MyBookmark1", true, true, false, "Bookmark1, with footnote number ").GetFieldCode());

    // Bookmark2 يقع أسفل هذا الحقل ويحتوي على رقم الحاشية السفلية 2، لذا سيعرض الحقل "2 أدناه".
    // يجعل العلم \f الرقم 2 يظهر بنفس تنسيق تسمية رقم الحاشية السفلية في النص الفعلي.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h \\p \\f",
        InsertFieldNoteRef(builder, "MyBookmark2", true, true, true, "Bookmark2, with footnote number ").GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);
    InsertBookmarkWithFootnote(builder, "MyBookmark2", "Contents of MyBookmark2", "Footnote from MyBookmark2");

    doc.UpdatePageLayout();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.NOTEREF.docx");
}

/// <summary>
/// يستخدم منشئ المستندات لإدراج حقل NOTEREF بالخصائص المحددة.
/// </summary>
private static FieldNoteRef InsertFieldNoteRef(DocumentBuilder builder, string bookmarkName, bool insertHyperlink, bool insertRelativePosition, bool insertReferenceMark, string textBefore)
{
    builder.Write(textBefore);

    FieldNoteRef field = (FieldNoteRef)builder.InsertField(FieldType.FieldNoteRef, true);
    field.BookmarkName = bookmarkName;
    field.InsertHyperlink = insertHyperlink;
    field.InsertRelativePosition = insertRelativePosition;
    field.InsertReferenceMark = insertReferenceMark;
    builder.Writeln();

    return field;
}

/// <summary>
/// يستخدم منشئ المستندات لإدراج إشارة مرجعية مسماة مع حاشية سفلية في النهاية.
/// </summary>
private static void InsertBookmarkWithFootnote(DocumentBuilder builder, string bookmarkName, string bookmarkText, string footnoteText)
{
    builder.StartBookmark(bookmarkName);
    builder.Write(bookmarkText);
    builder.InsertFootnote(FootnoteType.Footnote, footnoteText);
    builder.EndBookmark(bookmarkName);
    builder.Writeln();
}
```

### أنظر أيضا

* class [FieldNoteRef](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
