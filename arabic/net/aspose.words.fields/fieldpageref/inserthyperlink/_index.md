---
title: FieldPageRef.InsertHyperlink
second_title: Aspose.Words لمراجع .NET API
description: FieldPageRef ملكية. الحصول على أو تعيين ما إذا كان سيتم إدراج ارتباط تشعبي للفقرة ذات الإشارة المرجعية.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldpageref/inserthyperlink/
---
## FieldPageRef.InsertHyperlink property

الحصول على أو تعيين ما إذا كان سيتم إدراج ارتباط تشعبي للفقرة ذات الإشارة المرجعية.

```csharp
public bool InsertHyperlink { get; set; }
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

    // يمكننا استخدام العلامة \p لعرض حقل PAGEREF
    // موضع الإشارة المرجعية بالنسبة لموضع الحقل.
    // الإشارة المرجعية 1 موجودة في نفس الصفحة وفوق هذا الحقل، لذا ستكون النتيجة المعروضة لهذا الحقل "أعلى".
    Assert.AreEqual(" PAGEREF  MyBookmark1 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark1", true, true, "Bookmark1 is ").GetFieldCode());

    // الإشارة المرجعية 2 ستكون في نفس الصفحة وأسفل هذا الحقل، لذا ستكون النتيجة المعروضة لهذا الحقل "أدناه".
    Assert.AreEqual(" PAGEREF  MyBookmark2 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark2", true, true, "Bookmark2 is ").GetFieldCode());

    // الإشارة المرجعية 3 ستكون في صفحة مختلفة، لذا سيعرض الحقل "في الصفحة 2".
    Assert.AreEqual(" PAGEREF  MyBookmark3 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark3", true, true, "Bookmark3 is ").GetFieldCode());

    InsertAndNameBookmark(builder, "MyBookmark2");
    builder.InsertBreak(BreakType.PageBreak);
    InsertAndNameBookmark(builder, "MyBookmark3");

    doc.UpdatePageLayout();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.PAGEREF.docx");
}

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


