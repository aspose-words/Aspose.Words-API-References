---
title: FieldRef Class
linktitle: FieldRef
articleTitle: FieldRef
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Fields.FieldRef فصل. ينفذ حقل REF في C#.
type: docs
weight: 2330
url: /ar/net/aspose.words.fields/fieldref/
---
## FieldRef class

ينفذ حقل REF.

لمعرفة المزيد، قم بزيارة[العمل مع الحقول](https://docs.aspose.com/words/net/working-with-fields/) مقالة توثيقية.

```csharp
public class FieldRef : Field
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FieldRef](fieldref/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldref/bookmarkname/) { get; set; } | الحصول على اسم الإشارة المرجعية أو تعيينه. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | الحصول على النص الذي يمثل نتيجة الحقل المعروض. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/) الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [IncludeNoteOrComment](../../aspose.words.fields/fieldref/includenoteorcomment/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم زيادة أرقام الحواشي السفلية والتعليقات الختامية والتعليقات التوضيحية التي تم وضع علامة عليها بواسطة الإشارة المرجعية، وإدراج الحاشية السفلية والتعليقات الختامية ونص التعليق المقابل. |
| [InsertHyperlink](../../aspose.words.fields/fieldref/inserthyperlink/) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم إنشاء ارتباط تشعبي للفقرة ذات الإشارة المرجعية. |
| [InsertParagraphNumber](../../aspose.words.fields/fieldref/insertparagraphnumber/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم إدراج رقم الفقرة للفقرة المشار إليها تمامًا كما يظهر في المستند. |
| [InsertParagraphNumberInFullContext](../../aspose.words.fields/fieldref/insertparagraphnumberinfullcontext/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم إدراج رقم الفقرة للفقرة المشار إليها في السياق الكامل. |
| [InsertParagraphNumberInRelativeContext](../../aspose.words.fields/fieldref/insertparagraphnumberinrelativecontext/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم إدراج رقم الفقرة للفقرة المشار إليها في السياق النسبي. |
| [InsertRelativePosition](../../aspose.words.fields/fieldref/insertrelativeposition/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم إدراج الموضع النسبي للفقرة المشار إليها. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | الحصول على أو تعيين ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب تعديلات أخرى تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | الحصول على أو تعيين ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب النتيجة). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | الحصول على أو تعيين LCID الخاص بالحقل. |
| [NumberSeparator](../../aspose.words.fields/fieldref/numberseparator/) { get; set; } | الحصول على أو تعيين تسلسل الأحرف المستخدم لفصل أرقام التسلسل وأرقام الصفحات. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | الحصول على أو تعيين النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقول. يمكن ان يكون`باطل` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| [SuppressNonDelimiters](../../aspose.words.fields/fieldref/suppressnondelimiters/) { get; set; } | الحصول على أو تعيين ما إذا كان سيتم منع الأحرف غير المحددة. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | الحصول على نوع حقل Microsoft Word. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من رمز الحقل ونتيجة الحقل للحقول الفرعية. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | إرجاع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [Remove](../../aspose.words.fields/field/remove/)() | إزالة الحقل من المستند. إرجاع عقدة مباشرة بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير للعقدة الأصلية، فسيتم إرجاع الفقرة الأصلية الخاصة به. إذا تمت إزالة الحقل بالفعل، فسيتم إرجاعه`باطل` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | يقوم بإلغاء ربط الحقل. |
| [Update](../../aspose.words.fields/field/update/)() | يقوم بإجراء التحديث الميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | إجراء تحديث ميداني. يتم الرمي إذا تم تحديث الحقل بالفعل. |

## ملاحظات

إدراج النص أو الرسومات التي تمثلها الإشارة المرجعية المحددة.

## أمثلة

يوضح كيفية إنشاء نص ذو إشارة مرجعية باستخدام حقل SET، ثم عرضه في المستند باستخدام حقل REF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // قم بتسمية النص الذي تم وضع إشارة مرجعية عليه بحقل SET.
// يشير هذا الحقل إلى "الإشارة المرجعية" وليس إلى بنية الإشارة المرجعية التي تظهر داخل النص، ولكنه يشير إلى متغير مسمى.
FieldSet fieldSet = (FieldSet)builder.InsertField(FieldType.FieldSet, false);
fieldSet.BookmarkName = "MyBookmark";
fieldSet.BookmarkText = "Hello world!";
fieldSet.Update();

Assert.AreEqual(" SET  MyBookmark \"Hello world!\"", fieldSet.GetFieldCode());

// ارجع إلى الإشارة المرجعية بالاسم في حقل REF واعرض محتوياتها.
FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
fieldRef.BookmarkName = "MyBookmark";
fieldRef.Update();

Assert.AreEqual(" REF  MyBookmark", fieldRef.GetFieldCode());
Assert.AreEqual("Hello world!", fieldRef.Result);

doc.Save(ArtifactsDir + "Field.SET.REF.docx");
```

يوضح كيفية إدراج حقول REF للإشارة إلى الإشارات المرجعية.

```csharp
public void FieldRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");
    builder.InsertFootnote(FootnoteType.Footnote, "MyBookmark footnote #1");
    builder.Write("Text that will appear in REF field");
    builder.InsertFootnote(FootnoteType.Footnote, "MyBookmark footnote #2");
    builder.EndBookmark("MyBookmark");
    builder.MoveToDocumentStart();

    // سوف نقوم بتطبيق تنسيق قائمة مخصص، حيث يشير مقدار الأقواس الزاوية إلى مستوى القائمة الذي نحن فيه حاليًا.
    builder.ListFormat.ApplyNumberDefault();
    builder.ListFormat.ListLevel.NumberFormat = "> \x0000";

    // أدخل حقل REF الذي سيحتوي على النص الموجود داخل الإشارة المرجعية الخاصة بنا، وسيكون بمثابة رابط تشعبي، واستنساخ الحواشي السفلية للإشارة المرجعية.
    FieldRef field = InsertFieldRef(builder, "MyBookmark", "", "\n");
    field.IncludeNoteOrComment = true;
    field.InsertHyperlink = true;

    Assert.AreEqual(" REF  MyBookmark \\f \\h", field.GetFieldCode());

    // أدخل حقل REF، واعرض ما إذا كانت الإشارة المرجعية أعلى أو أسفل منه.
    field = InsertFieldRef(builder, "MyBookmark", "The referenced paragraph is ", " this field.\n");
    field.InsertRelativePosition = true;

    Assert.AreEqual(" REF  MyBookmark \\p", field.GetFieldCode());

    // اعرض رقم قائمة الإشارة المرجعية كما يظهر في المستند.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number is ", "\n");
    field.InsertParagraphNumber = true;

    Assert.AreEqual(" REF  MyBookmark \\n", field.GetFieldCode());

    // عرض رقم قائمة الإشارة المرجعية، ولكن مع حذف الأحرف غير المحددة، مثل الأقواس الزاوية.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number, non-delimiters suppressed, is ", "\n");
    field.InsertParagraphNumber = true;
    field.SuppressNonDelimiters = true;

    Assert.AreEqual(" REF  MyBookmark \\n \\t", field.GetFieldCode());

    // تحرك لأسفل مستوى القائمة بمقدار مستوى واحد.
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">> \x0001";

    // عرض رقم قائمة الإشارة المرجعية وأرقام جميع مستويات القائمة فوقها.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's full context paragraph number is ", "\n");
    field.InsertParagraphNumberInFullContext = true;

    Assert.AreEqual(" REF  MyBookmark \\w", field.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // عرض أرقام مستوى القائمة بين حقل REF هذا والإشارة المرجعية التي يشير إليها.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's relative paragraph number is ", "\n");
    field.InsertParagraphNumberInRelativeContext = true;

    Assert.AreEqual(" REF  MyBookmark \\r", field.GetFieldCode());

    // في نهاية المستند، ستظهر الإشارة المرجعية كعنصر قائمة هنا.
    builder.Writeln("List level above bookmark");
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">>> \x0002";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.REF.docx");
}

/// <summary>
/// اطلب من منشئ المستندات إدراج حقل REF، والإشارة إلى إشارة مرجعية به، وإضافة نص قبله وبعده.
/// </summary>
private static FieldRef InsertFieldRef(DocumentBuilder builder, string bookmarkName, string textBefore, string textAfter)
{
    builder.Write(textBefore);
    FieldRef field = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
    field.BookmarkName = bookmarkName;
    builder.Write(textAfter);
    return field;
}
```

### أنظر أيضا

* class [Field](../field/)
* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)
