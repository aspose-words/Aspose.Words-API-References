---
title: FieldPageRef
second_title: Aspose.Words لمراجع .NET API
description: تنفيذ حقل PAGEREF .
type: docs
weight: 2120
url: /ar/net/aspose.words.fields/fieldpageref/
---
## FieldPageRef class

تنفيذ حقل PAGEREF .

```csharp
public class FieldPageRef : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldPageRef](fieldpageref)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldpageref/bookmarkname) { get; set; } | الحصول على اسم الإشارة المرجعية أو تعيينه. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format) { get; } | يحصل على أ[`FieldFormat`](../fieldformat) كائن يوفر وصولاً مكتوبًا إلى تنسيق الحقل. |
| [InsertHyperlink](../../aspose.words.fields/fieldpageref/inserthyperlink) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم إدراج ارتباط تشعبي بالفقرة التي تم وضع إشارة مرجعية عليها. |
| [InsertRelativePosition](../../aspose.words.fields/fieldpageref/insertrelativeposition) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم إدراج موضع نسبي للفقرة التي تم وضع إشارة مرجعية عليها. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | الحصول على أو تحديد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | تحديد ما إذا كان الحقل مغلقًا أم لا (يجب عدم إعادة حساب النتيجة). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | الحصول على أو تحديد LCID للحقل. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | يحصل على العقدة التي تمثل فاصل المجال. يمكن أن يكون فارغًا. |
| [Start](../../aspose.words.fields/field/start) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | يحصل على نوع حقل Microsoft Word . |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) ._ x000d_ يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) ._ x000d_ |
| [Remove](../../aspose.words.fields/field/remove)() | يزيل الحقل من المستند. إرجاع عقدة بعد الحقل مباشرة. إذا كانت نهاية الحقل هي آخر child من العقدة الأصلية ، يتم إرجاع فقرته الأصلية. إذا تمت إزالة الحقل بالفعل ، يعود **لا شيء** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update)() | يقوم بالتحديث الميداني. يرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update)(bool) | يقوم بإجراء تحديث ميداني. يرمي إذا تم تحديث الحقل بالفعل. |

### ملاحظات

يُدرج رقم الصفحة التي تحتوي على الإشارة المرجعية المحددة كمرجع تبادلي ._ x000d_

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

* class [Field](../field)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
