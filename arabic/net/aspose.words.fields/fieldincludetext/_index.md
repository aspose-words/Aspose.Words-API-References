---
title: FieldIncludeText Class
linktitle: FieldIncludeText
articleTitle: FieldIncludeText
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fields.FieldIncludeText لدمج المستندات بسلاسة. حسّن سير عملك من خلال تطبيق حقل INCLUDETEXT بكفاءة.
type: docs
weight: 2460
url: /ar/net/aspose.words.fields/fieldincludetext/
---
## FieldIncludeText class

ينفذ حقل INCLUDETEXT.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

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
| [BookmarkName](../../aspose.words.fields/fieldincludetext/bookmarkname/) { get; set; } | يحصل على اسم الإشارة المرجعية في المستند المراد تضمينها أو يعينه. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [Encoding](../../aspose.words.fields/fieldincludetext/encoding/) { get; set; } | يحصل على أو يعين الترميز المطبق على البيانات داخل الملف المرجعي. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/)الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | يحصل على أو يحدد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | يحصل على أو يحدد ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب نتيجته). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | يحصل على أو يعين LCID للحقل. |
| [LockFields](../../aspose.words.fields/fieldincludetext/lockfields/) { get; set; } | يحصل على أو يحدد ما إذا كان سيتم منع تحديث الحقول في المستند المضمن. |
| [MimeType](../../aspose.words.fields/fieldincludetext/mimetype/) { get; set; } | يحصل على نوع MIME للملف المرجعي أو يعينه. |
| [NamespaceMappings](../../aspose.words.fields/fieldincludetext/namespacemappings/) { get; set; } | يحصل على تعيينات مساحة الأسماء لاستعلامات XPath أو يعينها. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | يحصل على النص الموجود بين فاصل الحقل ونهاية الحقل أو يعينه. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن يكون`باطل` . |
| [SourceFullName](../../aspose.words.fields/fieldincludetext/sourcefullname/) { get; set; } | يحصل على موقع المستند أو يعينه باستخدام IRI. |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| [TextConverter](../../aspose.words.fields/fieldincludetext/textconverter/) { get; set; } | يحصل على اسم محول النص لتنسيق الملف المضمن أو يعينه. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | يحصل على نوع حقل Microsoft Word. |
| [XPath](../../aspose.words.fields/fieldincludetext/xpath/) { get; set; } | يحصل على XPath أو يعينه للجزء المطلوب من ملف XML. |
| [XslTransformation](../../aspose.words.fields/fieldincludetext/xsltransformation/) { get; set; } | يحصل على موقع تحويل XSL لتنسيق بيانات XML أو يعينه. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [Remove](../../aspose.words.fields/field/remove/)() | يُزيل الحقل من المستند. يُرجع عقدة بعد الحقل مباشرةً. إذا كانت نهاية الحقل هي آخر عقدة فرعية للعقدة الأصلية، تُرجع فقرته الأصلية. إذا كان الحقل قد حُذف مُسبقًا، تُرجع`باطل` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يُجري تحديث الحقل. يُطرح هذا الخطأ إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | يُجري تحديثًا للحقل. يُطرح هذا الخطأ إذا كان الحقل قيد التحديث بالفعل. |

## ملاحظات

إدراج كل أو جزء من النص والرسومات الموجودة في مستند آخر.

## أمثلة

يوضح كيفية إنشاء حقل INCLUDETEXT وتعيين خصائصه.

```csharp
public void FieldIncludeText()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // فيما يلي طريقتان لاستخدام حقول INCLUDETEXT لعرض محتويات ملف XML في نظام الملفات المحلي.
    // 1 - تنفيذ تحويل XSL على مستند XML:
    FieldIncludeText fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.XslTransformation = MyDir + "CD collection XSL transformation.xsl";

    builder.Writeln();

    // 2 - استخدام XPath لأخذ عناصر محددة من مستند XML:
    fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.NamespaceMappings = "xmlns:n='myNamespace'";
    fieldIncludeText.XPath = "/catalog/cd/title";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.INCLUDETEXT.docx");
}

/// <summary>
/// استخدم منشئ المستندات لإدراج حقل INCLUDETEXT مع خصائص مخصصة.
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
