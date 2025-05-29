---
title: FieldPageRef.InsertHyperlink
linktitle: InsertHyperlink
articleTitle: InsertHyperlink
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية FieldPageRef InsertHyperlink على تعزيز مستنداتك من خلال الارتباط بسهولة بالفقرات المرجعية للتنقل بسلاسة.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldpageref/inserthyperlink/
---
## FieldPageRef.InsertHyperlink property

يحصل على أو يحدد ما إذا كان سيتم إدراج ارتباط تشعبي إلى الفقرة المرجعية.

```csharp
public bool InsertHyperlink { get; set; }
```

## أمثلة

يُظهر كيفية إدراج حقول PAGEREF لعرض الموقع النسبي للإشارات المرجعية.

```csharp
public void FieldPageRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    InsertAndNameBookmark(builder, "MyBookmark1");

    // أدخل حقل PAGEREF الذي يعرض الصفحة التي يوجد بها الإشارة المرجعية.
    // قم بتعيين علم InsertHyperlink لجعل الحقل يعمل أيضًا كارتباط قابل للنقر إلى الإشارة المرجعية.
    Assert.AreEqual(" PAGEREF  MyBookmark3 \\h", 
        InsertFieldPageRef(builder, "MyBookmark3", true, false, "Hyperlink to Bookmark3, on page: ").GetFieldCode());

    // يمكننا استخدام علامة \p لعرض حقل PAGEREF
    // موضع الإشارة المرجعية بالنسبة لموضع الحقل.
    // Bookmark1 موجود في نفس الصفحة وفوق هذا الحقل، لذا فإن نتيجة هذا الحقل المعروضة ستكون "أعلى".
    Assert.AreEqual(" PAGEREF  MyBookmark1 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark1", true, true, "Bookmark1 is ").GetFieldCode());

    // سيكون Bookmark2 على نفس الصفحة وأسفل هذا الحقل، لذا فإن نتيجة هذا الحقل المعروضة ستكون "أسفل".
    Assert.AreEqual(" PAGEREF  MyBookmark2 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark2", true, true, "Bookmark2 is ").GetFieldCode());

    // ستكون الإشارة المرجعية 3 في صفحة مختلفة، لذا سيعرض الحقل "في الصفحة 2".
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
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
