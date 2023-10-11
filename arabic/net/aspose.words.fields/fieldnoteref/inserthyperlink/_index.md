---
title: FieldNoteRef.InsertHyperlink
second_title: Aspose.Words لمراجع .NET API
description: FieldNoteRef ملكية. الحصول على أو تعيين ما إذا كان سيتم إدراج ارتباط تشعبي للفقرة ذات الإشارة المرجعية.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldnoteref/inserthyperlink/
---
## FieldNoteRef.InsertHyperlink property

الحصول على أو تعيين ما إذا كان سيتم إدراج ارتباط تشعبي للفقرة ذات الإشارة المرجعية.

```csharp
public bool InsertHyperlink { get; set; }
```

### أمثلة

يظهر لإدراج حقول NOTREF، وتعديل مظهرها.

```csharp
public void FieldNoteRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // قم بإنشاء إشارة مرجعية مع حاشية سفلية سيشير إليها حقل NOTREF.
    InsertBookmarkWithFootnote(builder, "MyBookmark1", "Contents of MyBookmark1", "Footnote from MyBookmark1");

    // سيعرض حقل NOTREF هذا رقم الحاشية السفلية داخل الإشارة المرجعية المشار إليها.
    // يتيح لنا تعيين خاصية InsertHyperlink الانتقال إلى الإشارة المرجعية عن طريق الضغط على Ctrl + النقر فوق الحقل في Microsoft Word.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h",
        InsertFieldNoteRef(builder, "MyBookmark2", true, false, false, "Hyperlink to Bookmark2, with footnote number ").GetFieldCode());

    // عند استخدام العلامة \p، بعد رقم الحاشية السفلية، يعرض الحقل أيضًا موضع الإشارة المرجعية بالنسبة للحقل.
    // الإشارة المرجعية 1 أعلى هذا الحقل وتحتوي على الحاشية السفلية رقم 1، لذا ستكون النتيجة "1 أعلاه" عند التحديث.
    Assert.AreEqual(" NOTEREF  MyBookmark1 \\h \\p",
        InsertFieldNoteRef(builder, "MyBookmark1", true, true, false, "Bookmark1, with footnote number ").GetFieldCode());

    // الإشارة المرجعية 2 موجودة أسفل هذا الحقل وتحتوي على الحاشية السفلية رقم 2، لذا سيعرض الحقل "2 أدناه".
    // العلامة \f تجعل الرقم 2 يظهر بنفس تنسيق تسمية رقم الحاشية السفلية في النص الفعلي.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h \\p \\f",
        InsertFieldNoteRef(builder, "MyBookmark2", true, true, true, "Bookmark2, with footnote number ").GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);
    InsertBookmarkWithFootnote(builder, "MyBookmark2", "Contents of MyBookmark2", "Footnote from MyBookmark2");

    doc.UpdatePageLayout();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.NOTEREF.docx");
}

/// <summary>
/// يستخدم منشئ المستندات لإدراج حقل NOTREF بخصائص محددة.
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
/// يستخدم أداة إنشاء المستندات لإدراج إشارة مرجعية مسماة مع حاشية سفلية في النهاية.
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
* مساحة الاسم [Aspose.Words.Fields](../../fieldnoteref/)
* المجسم [Aspose.Words](../../../)


