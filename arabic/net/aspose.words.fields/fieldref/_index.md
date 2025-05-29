---
title: FieldRef Class
linktitle: FieldRef
articleTitle: FieldRef
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fields.FieldRef لتطبيق حقول REF بسلاسة. حسّن أتمتة مستنداتك وحسّن سير عملك اليوم!
type: docs
weight: 2740
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
| [BookmarkName](../../aspose.words.fields/fieldref/bookmarkname/) { get; set; } | يحصل على اسم الإشارة المرجعية أو يعينه. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [End](../../aspose.words.fields/field/end/) { get; } | يحصل على العقدة التي تمثل نهاية الحقل. |
| [Format](../../aspose.words.fields/field/format/) { get; } | يحصل على[`FieldFormat`](../fieldformat/)الكائن الذي يوفر الوصول المكتوب إلى تنسيق الحقل. |
| [IncludeNoteOrComment](../../aspose.words.fields/fieldref/includenoteorcomment/) { get; set; } | يحصل على أو يعين ما إذا كان سيتم زيادة أرقام الحواشي السفلية والحواشي النهائية والتعليقات التوضيحية التي تم وضع علامة عليها بواسطة الإشارة المرجعية، وإدراج نص الحاشية السفلية والحاشية النهائية والتعليق المقابل. |
| [InsertHyperlink](../../aspose.words.fields/fieldref/inserthyperlink/) { get; set; } | يحصل على أو يحدد ما إذا كان سيتم إنشاء ارتباط تشعبي إلى الفقرة المرجعية. |
| [InsertParagraphNumber](../../aspose.words.fields/fieldref/insertparagraphnumber/) { get; set; } | يحصل على أو يحدد ما إذا كان سيتم إدراج رقم الفقرة للفقرة المشار إليها تمامًا كما يظهر في المستند. |
| [InsertParagraphNumberInFullContext](../../aspose.words.fields/fieldref/insertparagraphnumberinfullcontext/) { get; set; } | يحصل على أو يحدد ما إذا كان سيتم إدراج رقم الفقرة للفقرة المشار إليها في السياق الكامل. |
| [InsertParagraphNumberInRelativeContext](../../aspose.words.fields/fieldref/insertparagraphnumberinrelativecontext/) { get; set; } | يحصل على أو يحدد ما إذا كان سيتم إدراج رقم الفقرة للفقرة المشار إليها في السياق النسبي. |
| [InsertRelativePosition](../../aspose.words.fields/fieldref/insertrelativeposition/) { get; set; } | يحصل على أو يحدد ما إذا كان سيتم إدراج الموضع النسبي للفقرة المشار إليها. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | يحصل على أو يحدد ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | يحصل على أو يحدد ما إذا كان الحقل مقفلاً (لا ينبغي إعادة حساب نتيجته). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | يحصل على أو يعين LCID للحقل. |
| [NumberSeparator](../../aspose.words.fields/fieldref/numberseparator/) { get; set; } | يحصل على أو يعين تسلسل الأحرف المستخدم لفصل أرقام التسلسل وأرقام الصفحات. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | يحصل على النص الموجود بين فاصل الحقل ونهاية الحقل أو يعينه. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن يكون`باطل` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | يحصل على العقدة التي تمثل بداية الحقل. |
| [SuppressNonDelimiters](../../aspose.words.fields/fieldref/suppressnondelimiters/) { get; set; } | يحصل على أو يحدد ما إذا كان سيتم قمع الأحرف غير الفاصلة. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | يحصل على نوع حقل Microsoft Word. |

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

يقوم بإدراج النص أو الرسومات التي يمثلها الإشارة المرجعية المحددة.

## أمثلة

يوضح كيفية إنشاء نص مرجعي باستخدام حقل SET، ثم عرضه في المستند باستخدام حقل REF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // قم بتسمية النص المضاف إليه إشارة مرجعية باستخدام حقل SET.
// يشير هذا الحقل إلى "الإشارة المرجعية" وليس إلى بنية الإشارة المرجعية التي تظهر داخل النص، بل إلى متغير مسمى.
FieldSet fieldSet = (FieldSet)builder.InsertField(FieldType.FieldSet, false);
fieldSet.BookmarkName = "MyBookmark";
fieldSet.BookmarkText = "Hello world!";
fieldSet.Update();

Assert.AreEqual(" SET  MyBookmark \"Hello world!\"", fieldSet.GetFieldCode());

// قم بالإشارة إلى الإشارة المرجعية بالاسم في حقل REF وعرض محتوياتها.
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

    // سوف نطبق تنسيق قائمة مخصص، حيث يشير عدد الأقواس الزاوية إلى مستوى القائمة الذي نحن فيه حاليًا.
    builder.ListFormat.ApplyNumberDefault();
    builder.ListFormat.ListLevel.NumberFormat = "> \x0000";

    // قم بإدراج حقل REF الذي سيحتوي على النص الموجود داخل الإشارة المرجعية لدينا، وسيعمل كارتباط تشعبي، ويستنسخ حواشي الإشارة المرجعية.
    FieldRef field = InsertFieldRef(builder, "MyBookmark", "", "\n");
    field.IncludeNoteOrComment = true;
    field.InsertHyperlink = true;

    Assert.AreEqual(" REF  MyBookmark \\f \\h", field.GetFieldCode());

    // أدخل حقل REF، واعرض ما إذا كانت الإشارة المرجعية أعلى أو أسفله.
    field = InsertFieldRef(builder, "MyBookmark", "The referenced paragraph is ", " this field.\n");
    field.InsertRelativePosition = true;

    Assert.AreEqual(" REF  MyBookmark \\p", field.GetFieldCode());

    // عرض رقم قائمة الإشارة المرجعية كما يظهر في المستند.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number is ", "\n");
    field.InsertParagraphNumber = true;

    Assert.AreEqual(" REF  MyBookmark \\n", field.GetFieldCode());

    // عرض رقم قائمة الإشارة المرجعية، ولكن مع حذف الأحرف غير الفاصلة، مثل الأقواس الزاوية.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number, non-delimiters suppressed, is ", "\n");
    field.InsertParagraphNumber = true;
    field.SuppressNonDelimiters = true;

    Assert.AreEqual(" REF  MyBookmark \\n \\t", field.GetFieldCode());

    //الانتقال إلى أسفل مستوى واحد في القائمة.
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">> \x0001";

    // عرض رقم قائمة الإشارة المرجعية وأرقام جميع مستويات القائمة الموجودة أعلى منها.
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
/// احصل على منشئ المستندات لإدراج حقل REF، والإشارة إلى إشارة مرجعية به، وإضافة نص قبله وبعده.
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
