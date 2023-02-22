---
title: Class FieldDdeAuto
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fields.FieldDdeAuto فصل. ينفذ حقل DDEAUTO .
type: docs
weight: 1640
url: /ar/net/aspose.words.fields/fieldddeauto/
---
## FieldDdeAuto class

ينفذ حقل DDEAUTO .

```csharp
public class FieldDdeAuto : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldDdeAuto](fieldddeauto/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على أ[`FieldFormat`](../fieldformat/) كائن يوفر وصولاً مكتوبًا إلى تنسيق الحقل. |
| [InsertAsBitmap](../../aspose.words.fields/fieldddeauto/insertasbitmap/) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم إدراج الكائن المرتبط كصورة نقطية. |
| [InsertAsHtml](../../aspose.words.fields/fieldddeauto/insertashtml/) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم إدراج الكائن المرتبط كنص بتنسيق HTML. |
| [InsertAsPicture](../../aspose.words.fields/fieldddeauto/insertaspicture/) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم إدراج الكائن المرتبط كصورة. |
| [InsertAsRtf](../../aspose.words.fields/fieldddeauto/insertasrtf/) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم إدراج الكائن المرتبط بتنسيق rich-text (RTF). |
| [InsertAsText](../../aspose.words.fields/fieldddeauto/insertastext/) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم إدراج الكائن المرتبط بتنسيق نصي فقط. |
| [InsertAsUnicode](../../aspose.words.fields/fieldddeauto/insertasunicode/) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم إدراج الكائن المرتبط كنص Unicode. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | الحصول على أو تحديد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLinked](../../aspose.words.fields/fieldddeauto/islinked/) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم تقليل حجم الملف من خلال عدم تخزين بيانات الرسومات مع المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | تحديد ما إذا كان الحقل مغلقًا أم لا (يجب عدم إعادة حساب النتيجة). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | الحصول على أو تحديد LCID للحقل. |
| [ProgId](../../aspose.words.fields/fieldddeauto/progid/) { get; set; } | الحصول على أو تحديد نوع التطبيق لمعلومات الارتباط. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل المجال. يمكن أن يكون فارغًا. |
| [SourceFullName](../../aspose.words.fields/fieldddeauto/sourcefullname/) { get; set; } | الحصول على أو تحديد اسم وموقع الملف المصدر. |
| [SourceItem](../../aspose.words.fields/fieldddeauto/sourceitem/) { get; set; } | الحصول على جزء من الملف المصدر الذي يتم ربطه أو تعيينه. |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | يحصل على نوع حقل Microsoft Word . |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) . يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل) . |
| [Remove](../../aspose.words.fields/field/remove/)() | يزيل الحقل من المستند. إرجاع عقدة بعد الحقل مباشرة. إذا كانت نهاية الحقل هي آخر child من العقدة الأصلية ، يتم إرجاع فقرته الأصلية. إذا تمت إزالة الحقل بالفعل ، يعود **لا شيء** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يقوم بالتحديث الميداني. يرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(bool) | يقوم بإجراء تحديث ميداني. يرمي إذا تم تحديث الحقل بالفعل. |

### ملاحظات

للحصول على معلومات منسوخة من تطبيق آخر ، يربط هذا الحقل تلك المعلومات بملفها المصدر الأصلي باستخدام DDE ويتم تحديثها تلقائيًا.

### أمثلة

يوضح كيفية استخدام أنواع الحقول المختلفة للارتباط بمستندات أخرى في نظام الملفات المحلي ، وعرض محتوياتها.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // فيما يلي ثلاثة أنواع من الحقول التي يمكننا استخدامها لعرض محتويات من مستند مرتبط في شكل نص.
    // 1 - حقل LINK:
    builder.Writeln("FieldLink:\n");
    InsertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", MyDir + "Document.docx", null, true);

    // 2 - حقل DDE:
    builder.Writeln("FieldDde:\n");
    InsertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true, true);

    // 3 - حقل DDEAUTO:
    builder.Writeln("FieldDdeAuto:\n");
    InsertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.LINK.DDE.DDEAUTO.docx");
}

{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // فيما يلي ثلاثة أنواع من الحقول التي يمكننا استخدامها لعرض محتويات من مستند مرتبط في شكل صورة.
    // 1 - حقل LINK:
    builder.Writeln("FieldLink:\n");
    InsertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "MySpreadsheet.xlsx",
        "Sheet1!R2C2", true);

    // 2 - حقل DDE:
    builder.Writeln("FieldDde:\n");
    InsertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true, true);

    // 3 - حقل DDEAUTO:
    builder.Writeln("FieldDdeAuto:\n");
    InsertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
}

/// <summary>
/// استخدم أداة إنشاء المستندات لإدراج حقل LINK وتعيين خصائصه وفقًا للمعلمات.
/// </summary>
private static void InsertFieldLink(DocumentBuilder builder, InsertLinkedObjectAs insertLinkedObjectAs,
    string progId, string sourceFullName, string sourceItem, bool shouldAutoUpdate)
{
    FieldLink field = (FieldLink)builder.InsertField(FieldType.FieldLink, true);

    switch (insertLinkedObjectAs)
    {
        case InsertLinkedObjectAs.Text:
            field.InsertAsText = true;
            break;
        case InsertLinkedObjectAs.Unicode:
            field.InsertAsUnicode = true;
            break;
        case InsertLinkedObjectAs.Html:
            field.InsertAsHtml = true;
            break;
        case InsertLinkedObjectAs.Rtf:
            field.InsertAsRtf = true;
            break;
        case InsertLinkedObjectAs.Picture:
            field.InsertAsPicture = true;
            break;
        case InsertLinkedObjectAs.Bitmap:
            field.InsertAsBitmap = true;
            break;
    }

    field.AutoUpdate = shouldAutoUpdate;
    field.ProgId = progId;
    field.SourceFullName = sourceFullName;
    field.SourceItem = sourceItem;

    builder.Writeln("\n");
}

/// <summary>
/// استخدم أداة إنشاء المستندات لإدراج حقل DDE ، وتعيين خصائصه وفقًا للمعلمات.
/// </summary>
private static void InsertFieldDde(DocumentBuilder builder, InsertLinkedObjectAs insertLinkedObjectAs, string progId,
    string sourceFullName, string sourceItem, bool isLinked, bool shouldAutoUpdate)
{
    FieldDde field = (FieldDde)builder.InsertField(FieldType.FieldDDE, true);

    switch (insertLinkedObjectAs)
    {
        case InsertLinkedObjectAs.Text:
            field.InsertAsText = true;
            break;
        case InsertLinkedObjectAs.Unicode:
            field.InsertAsUnicode = true;
            break;
        case InsertLinkedObjectAs.Html:
            field.InsertAsHtml = true;
            break;
        case InsertLinkedObjectAs.Rtf:
            field.InsertAsRtf = true;
            break;
        case InsertLinkedObjectAs.Picture:
            field.InsertAsPicture = true;
            break;
        case InsertLinkedObjectAs.Bitmap:
            field.InsertAsBitmap = true;
            break;
    }

    field.AutoUpdate = shouldAutoUpdate;
    field.ProgId = progId;
    field.SourceFullName = sourceFullName;
    field.SourceItem = sourceItem;
    field.IsLinked = isLinked;

    builder.Writeln("\n");
}

/// <summary>
/// استخدم أداة إنشاء المستندات لإدراج حقل DDEAUTO وتعيين خصائصه وفقًا للمعلمات.
/// </summary>
private static void InsertFieldDdeAuto(DocumentBuilder builder, InsertLinkedObjectAs insertLinkedObjectAs,
    string progId, string sourceFullName, string sourceItem, bool isLinked)
{
    FieldDdeAuto field = (FieldDdeAuto)builder.InsertField(FieldType.FieldDDEAuto, true);

    switch (insertLinkedObjectAs)
    {
        case InsertLinkedObjectAs.Text:
            field.InsertAsText = true;
            break;
        case InsertLinkedObjectAs.Unicode:
            field.InsertAsUnicode = true;
            break;
        case InsertLinkedObjectAs.Html:
            field.InsertAsHtml = true;
            break;
        case InsertLinkedObjectAs.Rtf:
            field.InsertAsRtf = true;
            break;
        case InsertLinkedObjectAs.Picture:
            field.InsertAsPicture = true;
            break;
        case InsertLinkedObjectAs.Bitmap:
            field.InsertAsBitmap = true;
            break;
    }

    field.ProgId = progId;
    field.SourceFullName = sourceFullName;
    field.SourceItem = sourceItem;
    field.IsLinked = isLinked;
}

public enum InsertLinkedObjectAs
{
    // LinkedObjectAsText
    Text,
    Unicode,
    Html,
    Rtf,
    // LinkedObjectAsImage
    Picture,
    Bitmap
}
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)


