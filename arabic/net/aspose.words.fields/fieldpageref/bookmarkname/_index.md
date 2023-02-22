---
title: FieldPageRef.BookmarkName
second_title: Aspose.Words لمراجع .NET API
description: FieldPageRef ملكية. الحصول على اسم الإشارة المرجعية أو تعيينه.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldpageref/bookmarkname/
---
## FieldPageRef.BookmarkName property

الحصول على اسم الإشارة المرجعية أو تعيينه.

```csharp
public string BookmarkName { get; set; }
```

### أمثلة

يظهر لإدراج حقول PAGEREF لعرض الموقع النسبي للإشارات المرجعية.

```csharp
public void FieldPageRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    InsertAndNameBookmark(builder, "MyBookmark1");

    // أدخل حقل PAGEREF الذي يعرض الصفحة التي توجد بها الإشارة المرجعية.
    // قم بتعيين علامة InsertHyperlink لجعل الحقل يعمل أيضًا كارتباط قابل للنقر للإشارة المرجعية.
    Assert.AreEqual(" PAGEREF  MyBookmark3 \\h", 
        InsertFieldPageRef(builder, "MyBookmark3", true, false, "Hyperlink to Bookmark3, on page: ").GetFieldCode());

    // يمكننا استخدام علامة \ p لعرض حقل PAGEREF
    // موضع الإشارة المرجعية بالنسبة لموضع الحقل.
    // Bookmark1 موجودة في نفس الصفحة وفوق هذا الحقل ، لذا ستكون النتيجة المعروضة لهذا الحقل "أعلى".
    Assert.AreEqual(" PAGEREF  MyBookmark1 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark1", true, true, "Bookmark1 is ").GetFieldCode());

    ستكون // Bookmark2 في نفس الصفحة وأسفل هذا الحقل ، لذا ستكون النتيجة المعروضة في هذا الحقل "أدناه".
    Assert.AreEqual(" PAGEREF  MyBookmark2 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark2", true, true, "Bookmark2 is ").GetFieldCode());

    // ستظهر Bookmark3 على صفحة مختلفة ، لذلك سيعرض الحقل "في الصفحة 2".
    Assert.AreEqual(" PAGEREF  MyBookmark3 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark3", true, true, "Bookmark3 is ").GetFieldCode());

    InsertAndNameBookmark(builder, "MyBookmark2");
    builder.InsertBreak(BreakType.PageBreak);
    InsertAndNameBookmark(builder, "MyBookmark3");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.PAGEREF.docx");

/// <summary>
/// يستخدم منشئ المستندات لإدراج حقل PAGEREF وتعيين خصائصه.
/// </summary>
private static FieldPageRef InsertFieldPageRef(DocumentBuilder builder, string bookmarkName, bool insertHyperlink, bool insertRelativePosition, string textBefore)
{
    builder.Write(textBefore);

    FieldPageRef field = (FieldPageRef)builder.InsertField(FieldType.FieldPageRef, true);
    field.BookmarkName = bookmarkName;
    field.InsertHyperlink = insertHyperlink;
    field.InsertRelativePosition = insertRelativePosition;
    builder.Writeln();

    return field;
}

/// <summary>
/// يستخدم منشئ المستندات لإدراج إشارة مرجعية مسماة.
/// </summary>
private static void InsertAndNameBookmark(DocumentBuilder builder, string bookmarkName)
{
    builder.StartBookmark(bookmarkName);
    builder.Writeln($"Contents of bookmark \"{bookmarkName}\".");
    builder.EndBookmark(bookmarkName);
}
```

### أنظر أيضا

* class [FieldPageRef](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldpageref/)
* المجسم [Aspose.Words](../../../)


