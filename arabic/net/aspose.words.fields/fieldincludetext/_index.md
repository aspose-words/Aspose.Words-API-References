---
title: Class FieldIncludeText
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fields.FieldIncludeText فصل. تنفيذ حقل INCLUDETEXT .
type: docs
weight: 1900
url: /ar/net/aspose.words.fields/fieldincludetext/
---
## FieldIncludeText class

تنفيذ حقل INCLUDETEXT .

```csharp
public class FieldIncludeText : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldIncludeText](fieldincludetext/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldincludetext/bookmarkname/) { get; set; } | الحصول على أو تحديد اسم الإشارة المرجعية في المستند المراد تضمينه . |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروض. |
| [Encoding](../../aspose.words.fields/fieldincludetext/encoding/) { get; set; } | الحصول على أو تعيين الترميز المطبق على البيانات داخل الملف المرجعي. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على أ[`FieldFormat`](../fieldformat/) كائن يوفر وصولاً مكتوبًا إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | الحصول على أو تحديد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | تحديد ما إذا كان الحقل مغلقًا أم لا (يجب عدم إعادة حساب النتيجة). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | الحصول على أو تحديد LCID للحقل. |
| [LockFields](../../aspose.words.fields/fieldincludetext/lockfields/) { get; set; } | يحصل أو يحدد ما إذا كان سيتم منع تحديث الحقول في المستند المضمن. |
| [MimeType](../../aspose.words.fields/fieldincludetext/mimetype/) { get; set; } | الحصول على أو تعيين نوع MIME للملف المشار إليه. |
| [NamespaceMappings](../../aspose.words.fields/fieldincludetext/namespacemappings/) { get; set; } | الحصول على أو تعيين تعيينات مساحة الاسم لاستعلامات XPath. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل المجال. يمكن أن يكون فارغًا. |
| [SourceFullName](../../aspose.words.fields/fieldincludetext/sourcefullname/) { get; set; } | الحصول على أو تحديد موقع المستند باستخدام IRI . |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| [TextConverter](../../aspose.words.fields/fieldincludetext/textconverter/) { get; set; } | الحصول على أو تحديد اسم محول النص لتنسيق الملف المضمن. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | يحصل على نوع حقل Microsoft Word . |
| [XPath](../../aspose.words.fields/fieldincludetext/xpath/) { get; set; } | الحصول على XPath أو تعيينه للجزء المطلوب من ملف XML. |
| [XslTransformation](../../aspose.words.fields/fieldincludetext/xsltransformation/) { get; set; } | الحصول على أو تعيين موقع تحويل XSL لتنسيق بيانات XML. |

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

إدراج كل أو جزء من النص والرسومات المضمنة في مستند آخر.

### أمثلة

يوضح كيفية إنشاء حقل INCLUDETEXT وتعيين خصائصه.

```csharp
public void FieldIncludeText()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // فيما يلي طريقتان لاستخدام حقول INCLUDETEXT لعرض محتويات ملف XML في نظام الملفات المحلي.
    // 1 - إجراء تحويل XSL على مستند XML:
    FieldIncludeText fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.XslTransformation = MyDir + "CD collection XSL transformation.xsl";

    builder.Writeln();

    // 2 - استخدم XPath لأخذ عناصر محددة من مستند XML:
    fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.NamespaceMappings = "xmlns:n='myNamespace'";
    fieldIncludeText.XPath = "/catalog/cd/title";

    doc.Save(ArtifactsDir + "Field.INCLUDETEXT.docx");

/// <summary>
/// استخدم أداة إنشاء المستندات لإدراج حقل INCLUDETEXT بخصائص مخصصة.
/// </summary>
public FieldIncludeText CreateFieldIncludeText(DocumentBuilder builder, string sourceFullName, bool lockFields, string mimeType, string textConverter, string encoding)
{
    FieldIncludeText fieldIncludeText = (FieldIncludeText)builder.InsertField(FieldType.FieldIncludeText, true);
    fieldIncludeText.SourceFullName = sourceFullName;
    fieldIncludeText.LockFields = lockFields;
    fieldIncludeText.MimeType = mimeType;
    fieldIncludeText.TextConverter = textConverter;
    fieldIncludeText.Encoding = encoding;

    return fieldIncludeText;
}
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)


