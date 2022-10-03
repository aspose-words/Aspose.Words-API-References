---
title: UpdateFields
second_title: Aspose.Words لمراجع .NET API
description: يقوم بتحديث قيم الحقول في المستند بأكمله.
type: docs
weight: 730
url: /ar/net/aspose.words/document/updatefields/
---
## Document.UpdateFields method

يقوم بتحديث قيم الحقول في المستند بأكمله.

```csharp
public void UpdateFields()
```

### ملاحظات

عند فتح مستند وتعديله ثم حفظه ، فإن Aspose.word لا تقوم بتحديث الحقول تلقائيًا ، فهي تحافظ عليها . لذلك ، قد ترغب عادةً في استدعاء هذه الطريقة قبل الحفظ إذا قمت بتعديل document برمجيًا وتريد التأكد تظهر قيم الحقل المناسبة (المحسوبة) في المستند المحفوظ.

ليست هناك حاجة لتحديث الحقول بعد تنفيذ عملية دمج البريد لأن دمج البريد هو نوع من أنواع الحقول update ويقوم تلقائيًا بتحديث كافة الحقول في المستند.

لا تقوم هذه الطريقة بتحديث كافة أنواع الحقول. للحصول على قائمة مفصلة بأنواع الحقول المدعومة ، انظر دليل المبرمجين.

لا تقوم هذه الطريقة بتحديث الحقول المرتبطة بخوارزميات تخطيط الصفحة (مثل PAGE و PAGES و PAGEREF) . يتم تحديث الحقول المتعلقة بتخطيط الصفحة عند عرض مستند أو استدعاء[`UpdatePageLayout`](../updatepagelayout/).

استخدم ال[`NormalizeFieldTypes`](../normalizefieldtypes/) الطريقة قبل تحديث الحقول إذا كانت هناك تغييرات في المستند أثرت على أنواع الحقول.

لتحديث الحقول في جزء معين من الوثيقة استخدم[`UpdateFields`](../../range/updatefields/).

### أمثلة

يظهر استخدام حقل الاقتباس.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل حقل QUOTE ، والذي سيعرض قيمة خاصية Text الخاصة به.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// أدخل حقل QUOTE وقم بتداخل حقل DATE بداخله.
// تقوم حقول التاريخ بتحديث قيمتها إلى التاريخ الحالي في كل مرة نفتح فيها المستند باستخدام Microsoft Word.
// سيؤدي تداخل حقل DATE داخل حقل QUOTE مثل هذا إلى تجميد قيمته
// إلى التاريخ الذي أنشأنا فيه المستند.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// تحديث جميع الحقول لعرض نتائجها الصحيحة.
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

يوضح كيفية تعيين تفاصيل المستخدم ، وعرضها باستخدام الحقول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إنشاء كائن معلومات المستخدم وتعيينه كمصدر بيانات للحقول التي تعرض معلومات المستخدم.
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// أدخل حقول اسم المستخدم والمستخدمين و USERADDRESS التي تعرض قيم
// الخصائص الخاصة بكائن معلومات المستخدم الذي أنشأناه أعلاه. 
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

يوضح كيفية إدراج جدول محتويات (TOC) في مستند باستخدام أنماط العناوين كمدخلات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل جدول محتويات للصفحة الأولى من المستند.
// تكوين الجدول لالتقاط فقرات بعناوين المستويات من 1 إلى 3.
// أيضًا ، قم بتعيين إدخالاتها لتكون ارتباطات تشعبية ستأخذنا
// إلى موقع العنوان عند النقر بزر الماوس الأيسر في Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// ملء جدول المحتويات بإضافة فقرات بأنماط عناوين.
// كل عنوان بمستوى بين 1 و 3 سينشئ إدخالاً في الجدول.
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

// جدول المحتويات هو حقل من النوع يحتاج إلى تحديث لإظهار نتيجة محدثة.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
