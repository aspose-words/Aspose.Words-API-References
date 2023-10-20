---
title: Document.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: Aspose.Words لـ .NET
description: Document UpdateFields طريقة. يقوم بتحديث قيم الحقول في المستند بأكمله في C#.
type: docs
weight: 750
url: /ar/net/aspose.words/document/updatefields/
---
## Document.UpdateFields method

يقوم بتحديث قيم الحقول في المستند بأكمله.

```csharp
public void UpdateFields()
```

## ملاحظات

عند فتح مستند وتعديله ثم حفظه، لا يقوم Aspose.Words بتحديث الحقول تلقائيًا، بل يبقيها سليمة. لذلك، عادةً ما تريد استدعاء هذه الطريقة قبل الحفظ إذا قمت بتعديل document برمجيًا وتريد التأكد تظهر قيم الحقول المناسبة (المحسوبة) في المستند المحفوظ.

ليست هناك حاجة لتحديث الحقول بعد تنفيذ دمج البريد لأن دمج البريد هو نوع من تحديث الحقل ويقوم تلقائيًا بتحديث كافة الحقول في المستند.

لا يقوم هذا الأسلوب بتحديث كافة أنواع الحقول. للحصول على قائمة مفصلة بأنواع الحقول المدعومة، راجع دليل المبرمجين.

لا تقوم هذه الطريقة بتحديث الحقول المرتبطة بخوارزميات تخطيط الصفحة (مثل PAGE وPAGES وPAGEREF). يتم تحديث الحقول المرتبطة بتخطيط الصفحة عند عرض مستند أو الاتصال[`UpdatePageLayout`](../updatepagelayout/).

استخدم ال[`NormalizeFieldTypes`](../normalizefieldtypes/) الطريقة قبل تحديث الحقول إذا كانت هناك تغييرات في المستندات أثرت على أنواع الحقول.

لتحديث الحقول في جزء معين من استخدام المستند[`UpdateFields`](../../range/updatefields/).

## أمثلة

يظهر كيفية استخدام حقل عرض الأسعار.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل حقل عرض أسعار، والذي سيعرض قيمة خاصية النص الخاصة به.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// أدخل حقل عرض أسعار وقم بدمج حقل التاريخ بداخله.
// تقوم حقول التاريخ بتحديث قيمتها إلى التاريخ الحالي في كل مرة نفتح فيها المستند باستخدام Microsoft Word.
// سيؤدي تداخل حقل التاريخ داخل حقل عرض الأسعار بهذه الطريقة إلى تجميد قيمته
// حتى التاريخ الذي أنشأنا فيه المستند.
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

// قم بإنشاء كائن معلومات المستخدم وقم بتعيينه كمصدر بيانات للحقول التي تعرض معلومات المستخدم.
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// أدخل حقول اسم المستخدم، ومعلومات المستخدم، وعنوان المستخدم، التي تعرض قيم
 // الخصائص الخاصة بكائن UserInformation الذي قمنا بإنشائه أعلاه.
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// يحتوي كائن خيارات الحقل أيضًا على مستخدم افتراضي ثابت يمكن أن تشير إليه الحقول من جميع المستندات.
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

يوضح كيفية إدراج جدول محتويات (TOC) في مستند باستخدام أنماط العناوين كإدخالات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل جدول محتويات للصفحة الأولى من المستند.
// قم بتكوين الجدول لالتقاط الفقرات ذات العناوين من المستويات 1 إلى 3.
// أيضًا، قم بتعيين إدخالاته لتكون روابط تشعبية ستأخذنا
// إلى موقع العنوان عند النقر بزر الماوس الأيسر في Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// قم بملء جدول المحتويات عن طريق إضافة فقرات بأنماط العناوين.
// كل عنوان بمستوى يتراوح بين 1 و 3 سيُنشئ مُدخلاً في الجدول.
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

// جدول المحتويات هو حقل من النوع الذي يحتاج إلى التحديث لإظهار نتيجة محدثة.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
