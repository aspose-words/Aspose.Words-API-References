---
title: FieldNoteRef.InsertRelativePosition
second_title: Aspose.Words لمراجع .NET API
description: FieldNoteRef ملكية. الحصول على أو تحديد ما إذا كان سيتم إدراج موضع نسبي للفقرة التي تم وضع إشارة مرجعية عليها.
type: docs
weight: 50
url: /ar/net/aspose.words.fields/fieldnoteref/insertrelativeposition/
---
## FieldNoteRef.InsertRelativePosition property

الحصول على أو تحديد ما إذا كان سيتم إدراج موضع نسبي للفقرة التي تم وضع إشارة مرجعية عليها.

```csharp
public bool InsertRelativePosition { get; set; }
```

### أمثلة

يظهر لإدراج حقول NOTEREF وتعديل مظهرها.

```csharp
public void FieldNoteRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // قم بإنشاء إشارة مرجعية مع حاشية سفلية سيرجع إليها حقل NOTEREF.
    InsertBookmarkWithFootnote(builder, "MyBookmark1", "Contents of MyBookmark1", "Footnote from MyBookmark1");

    // سيعرض حقل NOTEREF هذا رقم الحاشية السفلية داخل الإشارة المرجعية المرجعية.
    // يتيح لنا تعيين خاصية InsertHyperlink الانتقال إلى الإشارة المرجعية عن طريق Ctrl + النقر فوق الحقل في Microsoft Word.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h",
        InsertFieldNoteRef(builder, "MyBookmark2", true, false, false, "Hyperlink to Bookmark2, with footnote number ").GetFieldCode());

    // عند استخدام علامة \ p ، بعد رقم الحاشية السفلية ، يعرض الحقل أيضًا موضع الإشارة المرجعية بالنسبة للحقل.
    // Bookmark1 أعلى هذا الحقل وتحتوي على رقم 1 في الحاشية السفلية ، وبالتالي ستكون النتيجة "1 أعلاه" عند التحديث.
    Assert.AreEqual(" NOTEREF  MyBookmark1 \\h \\p",
        InsertFieldNoteRef(builder, "MyBookmark1", true, true, false, "Bookmark1, with footnote number ").GetFieldCode());

    // Bookmark2 أسفل هذا الحقل وتحتوي على رقم 2 في الحاشية السفلية ، لذلك سيعرض الحقل "2 أدناه".
    // تجعل العلامة \ f يظهر الرقم 2 بنفس تنسيق تسمية رقم الحاشية السفلية في النص الفعلي.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h \\p \\f",
        InsertFieldNoteRef(builder, "MyBookmark2", true, true, true, "Bookmark2, with footnote number ").GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);
    InsertBookmarkWithFootnote(builder, "MyBookmark2", "Contents of MyBookmark2", "Footnote from MyBookmark2");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.NOTEREF.docx");

/// <summary>
/// يستخدم أداة إنشاء المستندات لإدراج حقل NOTEREF بخصائص محددة.
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
* مساحة الاسم [Aspose.Words.Fields](../../fieldnoteref/)
* المجسم [Aspose.Words](../../../)


