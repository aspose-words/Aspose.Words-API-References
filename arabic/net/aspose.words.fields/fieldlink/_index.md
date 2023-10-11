---
title: Class FieldLink
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fields.FieldLink فصل. ينفذ حقل LINK.
type: docs
weight: 2110
url: /ar/net/aspose.words.fields/fieldlink/
---
## FieldLink class

ينفذ حقل LINK.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class FieldLink : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldLink](fieldlink/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [AutoUpdate](../../aspose.words.fields/fieldlink/autoupdate/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم تحديث هذا الحقل تلقائيًا. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | الحصول على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/) الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [FormatUpdateType](../../aspose.words.fields/fieldlink/formatupdatetype/) { get; set; } | الحصول على أو تعيين الطريقة التي يقوم بها الكائن المرتبط بتحديث تنسيقه. |
| [InsertAsBitmap](../../aspose.words.fields/fieldlink/insertasbitmap/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم إدراج الكائن المرتبط كصورة نقطية. |
| [InsertAsHtml](../../aspose.words.fields/fieldlink/insertashtml/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم إدراج الكائن المرتبط كنص بتنسيق HTML. |
| [InsertAsPicture](../../aspose.words.fields/fieldlink/insertaspicture/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم إدراج الكائن المرتبط كصورة. |
| [InsertAsRtf](../../aspose.words.fields/fieldlink/insertasrtf/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم إدراج الكائن المرتبط بتنسيق نص منسق (RTF). |
| [InsertAsText](../../aspose.words.fields/fieldlink/insertastext/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم إدراج الكائن المرتبط بتنسيق نص فقط. |
| [InsertAsUnicode](../../aspose.words.fields/fieldlink/insertasunicode/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم إدراج الكائن المرتبط كنص Unicode. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | الحصول على أو تعيين ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب تعديلات أخرى تم إجراؤها على المستند. |
| [IsLinked](../../aspose.words.fields/fieldlink/islinked/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم تقليل حجم الملف من خلال عدم تخزين بيانات الرسومات مع المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | الحصول على أو تعيين ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب النتيجة). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | الحصول على أو تعيين LCID الخاص بالحقل. |
| [ProgId](../../aspose.words.fields/fieldlink/progid/) { get; set; } | الحصول على أو تعيين نوع التطبيق لمعلومات الارتباط. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقول. يمكن ان يكون`باطل` . |
| [SourceFullName](../../aspose.words.fields/fieldlink/sourcefullname/) { get; set; } | الحصول على أو تعيين اسم وموقع الملف المصدر. |
| [SourceItem](../../aspose.words.fields/fieldlink/sourceitem/) { get; set; } | الحصول على أو تعيين جزء الملف المصدر الذي يتم ربطه. |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | الحصول على نوع حقل Microsoft Word. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [Remove](../../aspose.words.fields/field/remove/)() | إزالة الحقل من المستند. إرجاع عقدة مباشرة بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير للعقدة الأصلية، فسيتم إرجاع الفقرة الأصلية الخاصة به. إذا تمت إزالة الحقل بالفعل، فسيتم إرجاعه`باطل` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يقوم بإجراء التحديث الميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(bool) | إجراء تحديث ميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |

### ملاحظات

بالنسبة للمعلومات المنسوخة من تطبيق آخر، يقوم هذا الحقل بربط تلك المعلومات بملفها الأصلي المصدر.

### أمثلة

يوضح كيفية استخدام أنواع الحقول المختلفة للارتباط بالمستندات الأخرى في نظام الملفات المحلي وعرض محتوياتها.

```csharp
public void FieldLinkedObjectsAsText(InsertLinkedObjectAs insertLinkedObjectAs)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // فيما يلي ثلاثة أنواع من الحقول التي يمكننا استخدامها لعرض محتويات مستند مرتبط في شكل نص.
    // 1 - حقل الرابط:
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

public void FieldLinkedObjectsAsImage(InsertLinkedObjectAs insertLinkedObjectAs)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // فيما يلي ثلاثة أنواع من الحقول التي يمكننا استخدامها لعرض محتويات مستند مرتبط في شكل صورة.
    // 1 - حقل الرابط:
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
/// استخدم منشئ المستندات لإدراج حقل LINK وتعيين خصائصه وفقًا للمعلمات.
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
/// استخدم منشئ المستندات لإدراج حقل DDE وتعيين خصائصه وفقًا للمعلمات.
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
/// استخدم منشئ المستندات لإدراج حقل DDEAUTO وتعيين خصائصه وفقًا للمعلمات.
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


