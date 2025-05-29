---
title: Document.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: Aspose.Words لـ .NET
description: قم بتجديد مستندك باستخدام طريقة UpdateFields—قم بتحديث جميع قيم الحقول بكفاءة لتحسين الدقة والتحرير السلس.
type: docs
weight: 810
url: /ar/net/aspose.words/document/updatefields/
---
## Document.UpdateFields method

تحديث قيم الحقول في المستند بأكمله.

```csharp
public void UpdateFields()
```

## ملاحظات

عند فتح مستند وتعديله ثم حفظه، لا يقوم Aspose.Words بتحديث الحقول تلقائيًا، بل يبقيها سليمة. لذلك، قد ترغب عادةً في استدعاء هذه الطريقة قبل الحفظ إذا قمت بتعديل document برمجيًا وتريد التأكد من ظهور قيم الحقول الصحيحة (المحسوبة) في المستند المحفوظ.

ليست هناك حاجة لتحديث الحقول بعد تنفيذ دمج البريد لأن دمج البريد هو نوع من تحديث الحقول ويقوم تلقائيًا بتحديث جميع الحقول في المستند.

لا تُحدِّث هذه الطريقة جميع أنواع الحقول. للاطلاع على قائمة مُفصَّلة بأنواع الحقول المدعومة، راجع دليل المبرمجين.

لا تقوم هذه الطريقة بتحديث الحقول المرتبطة بخوارزميات تخطيط الصفحة (على سبيل المثال PAGE وPAGES وPAGEREF). يتم تحديث الحقول المرتبطة بتخطيط الصفحة عند عرض مستند أو استدعاء[`UpdatePageLayout`](../updatepagelayout/).

استخدم[`NormalizeFieldTypes`](../normalizefieldtypes/) الطريقة قبل تحديث الحقول إذا كانت هناك تغييرات في المستند أثرت على أنواع الحقول.

لتحديث الحقول في جزء معين من المستند استخدم[`UpdateFields`](../../range/updatefields/).

## أمثلة

يظهر كيفية استخدام حقل الاقتباس.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج حقل QUOTE، والذي سيعرض قيمة خاصية النص الخاصة به.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// أدخل حقل QUOTE وقم بتضمين حقل DATE بداخله.
// تقوم حقول التاريخ بتحديث قيمتها إلى التاريخ الحالي في كل مرة نفتح فيها المستند باستخدام Microsoft Word.
// سيؤدي تعشيش حقل DATE داخل حقل QUOTE على هذا النحو إلى تجميد قيمته
// إلى التاريخ الذي أنشأنا فيه المستند.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// قم بتحديث كافة الحقول لعرض نتائجها الصحيحة.
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

يوضح كيفية تعيين تفاصيل المستخدم وعرضها باستخدام الحقول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء كائن UserInformation وقم بتعيينه كمصدر بيانات للحقول التي تعرض معلومات المستخدم.
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// أدخل حقول اسم المستخدم، والأحرف الأولى للمستخدم، وعنوان المستخدم، والتي تعرض قيم
 // الخصائص الخاصة بكائن UserInformation الذي أنشأناه أعلاه.
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// يحتوي كائن خيارات الحقل أيضًا على مستخدم افتراضي ثابت يمكن للحقول من كافة المستندات الرجوع إليه.
UserInformation.DefaultUser.Name = "Default User";
UserInformation.DefaultUser.Initials = "D. U.";
UserInformation.DefaultUser.Address = "One Microsoft Way";
doc.FieldOptions.CurrentUser = UserInformation.DefaultUser;

Assert.AreEqual("Default User", builder.InsertField(" USERNAME ").Result);
Assert.AreEqual("D. U.", builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual("One Microsoft Way", builder.InsertField(" USERADDRESS ").Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.CurrentUser.docx");
```

يوضح كيفية إدراج جدول المحتويات (TOC) في مستند باستخدام أنماط العناوين كإدخالات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//إدراج جدول المحتويات للصفحة الأولى من المستند.
// قم بتكوين الجدول لالتقاط الفقرات التي تحتوي على عناوين من المستويات 1 إلى 3.
// أيضًا، قم بتعيين إدخالاتها لتكون روابط تشعبية تأخذنا
// إلى موقع العنوان عند النقر بزر الماوس الأيسر في Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// قم بملء جدول المحتويات عن طريق إضافة فقرات ذات أنماط عناوين.
// كل عنوان من هذا القبيل بمستوى بين 1 و3 سوف ينشئ إدخالاً في الجدول.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 2");
builder.Writeln("Heading 3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;
builder.Writeln("Heading 3.1.1");
builder.Writeln("Heading 3.1.2");
builder.Writeln("Heading 3.1.3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;
builder.Writeln("Heading 3.1.3.1");
builder.Writeln("Heading 3.1.3.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.2");
builder.Writeln("Heading 3.3");

// جدول المحتويات هو حقل من نوع يحتاج إلى التحديث لإظهار نتيجة محدثة.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
