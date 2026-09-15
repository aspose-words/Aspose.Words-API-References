---
title: "طريقة Aspose::Words::Document::UpdateFields"
linktitle: "UpdateFields"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::UpdateFields. تقوم بتحديث قيم الحقول في المستند بأكمله في C++."
type: docs
weight: 96000
url: /ar/cpp/aspose.words/document/updatefields/
---
## Document::UpdateFields method


يحدّث قيم الحقول في كامل المستند.

```cpp
void Aspose::Words::Document::UpdateFields()
```

## ملاحظات


عند فتحك وتعديلك ثم حفظ مستند، لا تقوم Aspose.Words بتحديث الحقول تلقائيًا، بل تحتفظ بها كما هي. لذلك، عادةً ما ترغب في استدعاء هذه الطريقة قبل الحفظ إذا قمت بتعديل المستند برمجيًا وتريد التأكد من ظهور القيم الصحيحة (المُحسوبة) للحقول في المستند المحفوظ.

ليس هناك حاجة لتحديث الحقول بعد تنفيذ دمج البريد لأن دمج البريد هو نوع من تحديث الحقول ويقوم تلقائيًا بتحديث جميع الحقول في المستند.

هذه الطريقة لا تقوم بتحديث جميع أنواع الحقول. للحصول على القائمة التفصيلية لأنواع الحقول المدعومة، راجع دليل المبرمجين.

هذه الطريقة لا تقوم بتحديث الحقول المتعلقة بخوارزميات تخطيط الصفحة (مثل PAGE، PAGES، PAGEREF). يتم تحديث الحقول المتعلقة بتخطيط الصفحة عندما تقوم بتصيير مستند أو تستدعي [UpdatePageLayout](../updatepagelayout/).

استخدم طريقة [NormalizeFieldTypes](../normalizefieldtypes/) قبل تحديث الحقول إذا كانت هناك تغييرات في المستند أثرت على أنواع الحقول.

لتحديث الحقول في جزء محدد من المستند، استخدم [UpdateFields](../../range/updatefields/).

## أمثلة



يوضح كيفية إدراج جدول محتويات (TOC) في مستند باستخدام أنماط العناوين كمدخلات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إدراج جدول محتويات للصفحة الأولى من المستند.
// تكوين الجدول لالتقاط الفقرات التي تحتوي على عناوين من المستوى 1 إلى 3.
// أيضًا، اضبط مدخلاته لتكون روابط تشعبية ستأخذنا
// إلى موقع العنوان عند النقر بزر الفأرة الأيسر في Microsoft Word.
builder->InsertTableOfContents(u"\\o \"1-3\" \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// قم بملء جدول المحتويات بإضافة فقرات باستخدام أنماط العناوين.
// كل عنوان من هذا النوع بمستوى بين 1 و 3 سيُنشئ مدخلاً في الجدول.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 2");
builder->Writeln(u"Heading 3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);
builder->Writeln(u"Heading 3.1.1");
builder->Writeln(u"Heading 3.1.2");
builder->Writeln(u"Heading 3.1.3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading4);
builder->Writeln(u"Heading 3.1.3.1");
builder->Writeln(u"Heading 3.1.3.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.2");
builder->Writeln(u"Heading 3.3");

// جدول المحتويات هو حقل من نوع يحتاج إلى تحديث لإظهار نتيجة محدثة.
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertToc.docx");
```


يُظهر كيفية استخدام حقل QUOTE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج حقل QUOTE، الذي سيعرض قيمة خاصية Text الخاصة به.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
field->set_Text(u"\"Quoted text\"");

ASSERT_EQ(u" QUOTE  \"\\\"Quoted text\\\"\"", field->GetFieldCode());

// أدرج حقل QUOTE وضمّن داخله حقل DATE.
// تُحدّث حقول DATE قيمتها إلى التاريخ الحالي في كل مرة نفتح فيها المستند باستخدام Microsoft Word.
// إدراج حقل DATE داخل حقل QUOTE بهذه الطريقة سيجمد قيمته
// إلى التاريخ الذي أنشأنا فيه المستند.
builder->Write(u"\nDocument creation date: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
builder->MoveTo(field->get_Separator());
builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true);

ASSERT_EQ(System::String(u" QUOTE \u0013 DATE \u0014") + System::DateTime::get_Now().get_Date().ToShortDateString() + u"\u0015", field->GetFieldCode());

// حدّث جميع الحقول لعرض نتائجها الصحيحة.
doc->UpdateFields();

ASSERT_EQ(u"\"Quoted text\"", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.QUOTE.docx");
```


يعرض كيفية تعيين تفاصيل المستخدم وعرضها باستخدام الحقول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أنشئ كائن UserInformation واضبطه كمصدر بيانات للحقول التي تعرض معلومات المستخدم.
auto userInformation = System::MakeObject<Aspose::Words::Fields::UserInformation>();
userInformation->set_Name(u"John Doe");
userInformation->set_Initials(u"J. D.");
userInformation->set_Address(u"123 Main Street");
doc->get_FieldOptions()->set_CurrentUser(userInformation);

// أدرج حقول USERNAME و USERINITIALS و USERADDRESS، التي تعرض قيم
// الخصائص المقابلة لكائن UserInformation الذي أنشأناه أعلاه.
ASSERT_EQ(userInformation->get_Name(), builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(userInformation->get_Initials(), builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(userInformation->get_Address(), builder->InsertField(u" USERADDRESS ")->get_Result());

// كائن خيارات الحقل يحتوي أيضًا على مستخدم افتراضي ثابت يمكن للحقول في جميع المستندات الإشارة إليه.
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Name(u"Default User");
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Initials(u"D. U.");
Aspose::Words::Fields::UserInformation::get_DefaultUser()->set_Address(u"One Microsoft Way");
doc->get_FieldOptions()->set_CurrentUser(Aspose::Words::Fields::UserInformation::get_DefaultUser());

ASSERT_EQ(u"Default User", builder->InsertField(u" USERNAME ")->get_Result());
ASSERT_EQ(u"D. U.", builder->InsertField(u" USERINITIALS ")->get_Result());
ASSERT_EQ(u"One Microsoft Way", builder->InsertField(u" USERADDRESS ")->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.CurrentUser.docx");
```

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
