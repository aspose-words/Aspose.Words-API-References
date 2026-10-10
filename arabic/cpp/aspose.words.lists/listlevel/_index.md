---
title: "Aspose::Words::Lists::ListLevel فئة"
linktitle: "ListLevel"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Lists::ListLevel فئة. تُعرّف تنسيق مستوى القائمة. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.lists/listlevel/
---
## ListLevel class


يحدد تنسيق مستوى القائمة. لمعرفة المزيد، زر مقالة الوثائق [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class ListLevel : public Aspose::Words::IRunAttrSource
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [CreatePictureBullet](./createpicturebullet/)() | ينشئ شكل تعداد صورة للمستوى الحالي من القائمة. |
| [DeletePictureBullet](./deletepicturebullet/)() | يحذف تعداد الصورة للمستوى الحالي من القائمة. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Lists::ListLevel\>\&) | يقارن مع [ListLevel](./) المحدد. |
| [get_Alignment](./get_alignment/)() const | يحصل أو يضبط محاذاة الرقم الفعلي لعنصر القائمة. |
| [get_CustomNumberStyleFormat](./get_customnumberstyleformat/)() | يحصل أو يضبط تنسيق نمط الرقم المخصص لهذا المستوى من القائمة. على سبيل المثال: "a, ç, ĝ, ...". |
| [get_Font](./get_font/)() | يحدد تنسيق الأحرف المستخدم لتسمية القائمة. |
| [get_ImageData](./get_imagedata/)() | يعيد بيانات الصورة لشكل الرصاصة المصورة للمستوى الحالي من القائمة. |
| [get_IsLegal](./get_islegal/)() const | صحيح إذا كان المستوى يحول جميع الأرقام الموروثة إلى عربية، خطأ إذا كان يحافظ على نمط أرقامها. |
| [get_LinkedStyle](./get_linkedstyle/)() | يحصل أو يضبط نمط الفقرة المرتبط بهذا المستوى من القائمة. |
| [get_NumberFormat](./get_numberformat/)() const | يعيد أو يضبط تنسيق الرقم للمستوى من القائمة. |
| [get_NumberPosition](./get_numberposition/)() const | يعيد أو يضبط موضع (بالنقاط) الرقم أو الرصاصة للمستوى من القائمة. |
| [get_NumberStyle](./get_numberstyle/)() const | يعيد أو يضبط نمط الرقم لهذا المستوى من القائمة. |
| [get_RestartAfterLevel](./get_restartafterlevel/)() const | يضبط أو يعيد المستوى الذي يجب أن يظهر قبل المستوى المحدد لإعادة بدء الترقيم. |
| [get_StartAt](./get_startat/)() | يعيد أو يضبط الرقم الابتدائي لهذا المستوى من القائمة. |
| [get_TabPosition](./get_tabposition/)() const | يعيد أو يضبط موضع التبويب (بالنقاط) للمستوى من القائمة. |
| [get_TextPosition](./get_textposition/)() const | يعيد أو يضبط الموضع (بالنقاط) للسطر الثاني من النص المتفافٍ للمستوى من القائمة. |
| [get_TrailingCharacter](./get_trailingcharacter/)() const | يعيد أو يضبط الحرف المُدرج بعد الرقم للمستوى من القائمة. |
| static [GetEffectiveValue](./geteffectivevalue/)(int32_t, Aspose::Words::NumberStyle, const System::String\&) | يُبلغ عن تمثيل السلسلة لكائن [ListLevel](./) للمؤشر المحدد لعنصر القائمة. تُحدد المعلمات الـ[NumberStyle](../../aspose.words/numberstyle/) وسلسلة تنسيق اختيارية تُستخدم عندما يتم تحديد [Custom](../../aspose.words/numberstyle/). |
| [GetHashCode](./gethashcode/)() const override | يحسب قيمة التجزئة لهذا الكائن. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveTabStop](./removetabstop/)() | يزيل علامة التبويب من المستوى من القائمة. |
| [set_Alignment](./set_alignment/)(Aspose::Words::Lists::ListLevelAlignment) | مُعيّن لـ [Aspose::Words::Lists::ListLevel::get_Alignment](./get_alignment/). |
| [set_CustomNumberStyleFormat](./set_customnumberstyleformat/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Lists::ListLevel::get_CustomNumberStyleFormat](./get_customnumberstyleformat/). |
| [set_IsLegal](./set_islegal/)(bool) | مُعيّن لـ [Aspose::Words::Lists::ListLevel::get_IsLegal](./get_islegal/). |
| [set_LinkedStyle](./set_linkedstyle/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | مُعيّن لـ [Aspose::Words::Lists::ListLevel::get_LinkedStyle](./get_linkedstyle/). |
| [set_NumberFormat](./set_numberformat/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Lists::ListLevel::get_NumberFormat](./get_numberformat/). |
| [set_NumberPosition](./set_numberposition/)(double) | مُعيّن لـ [Aspose::Words::Lists::ListLevel::get_NumberPosition](./get_numberposition/). |
| [set_NumberStyle](./set_numberstyle/)(Aspose::Words::NumberStyle) | مُعيّن لـ [Aspose::Words::Lists::ListLevel::get_NumberStyle](./get_numberstyle/). |
| [set_RestartAfterLevel](./set_restartafterlevel/)(int32_t) | المُعيّن لـ [Aspose::Words::Lists::ListLevel::get_RestartAfterLevel](./get_restartafterlevel/). |
| [set_StartAt](./set_startat/)(int32_t) | المُعيّن لـ [Aspose::Words::Lists::ListLevel::get_StartAt](./get_startat/). |
| [set_TabPosition](./set_tabposition/)(double) | المُعيّن لـ [Aspose::Words::Lists::ListLevel::get_TabPosition](./get_tabposition/). |
| [set_TextPosition](./set_textposition/)(double) | المُعيّن لـ [Aspose::Words::Lists::ListLevel::get_TextPosition](./get_textposition/). |
| [set_TrailingCharacter](./set_trailingcharacter/)(Aspose::Words::Lists::ListTrailingCharacter) | المُعيّن لـ [Aspose::Words::Lists::ListLevel::get_TrailingCharacter](./get_trailingcharacter/). |
| static [Type](./type/)() |  |
## ملاحظات


أنت لا تنشئ كائنات من هذه الفئة. يتم إنشاء كائنات مستوى [List](../list/) تلقائيًا عند إنشاء قائمة. يمكنك الوصول إلى كائنات [ListLevel](./) عبر مجموعة [ListLevelCollection](../listlevelcollection/).

استخدم خصائص [ListLevel](./) لتحديد تنسيق القوائم للمستويات الفردية.

## أمثلة



يوضح كيفية تطبيق تنسيق قائمة مخصص على الفقرات عند استخدام [DocumentBuilder](../../aspose.words/documentbuilder/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// تتيح لنا القائمة تنظيم وتزيين مجموعات الفقرات باستخدام رموز البادئة والمسافات البادئة.
// يمكننا إنشاء قوائم متداخلة بزيادة مستوى المسافة البادئة.
// يمكننا بدء وإنهاء قائمة باستخدام خاصية "ListFormat" لكائن Document Builder.
// كل فقرة نضيفها بين بداية القائمة ونهايتها ستصبح عنصرًا في القائمة.
// إنشاء قائمة من قالب Microsoft Word، وتخصيص أول مستويين من مستوياتها.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = list->get_ListLevels()->idx_get(0);
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Red());
listLevel->get_Font()->set_Size(24);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::OrdinalText);
listLevel->set_StartAt(21);
listLevel->set_NumberFormat(u"\x0000");

listLevel->set_NumberPosition(-36);
listLevel->set_TextPosition(144);
listLevel->set_TabPosition(144);

listLevel = list->get_ListLevels()->idx_get(1);
listLevel->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::Bullet);
listLevel->get_Font()->set_Name(u"Wingdings");
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Blue());
listLevel->get_Font()->set_Size(24);

// ستُنشئ قيمة NumberFormat هذه رموز تعداد نقطية على شكل نجمة.
listLevel->set_NumberFormat(u"\xf0af");
listLevel->set_TrailingCharacter(Aspose::Words::Lists::ListTrailingCharacter::Space);
listLevel->set_NumberPosition(144);

// إنشاء فقرات وتطبيق كلا مستويي القائمة من تنسيقنا المخصص علىها.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->set_List(list);
builder->Writeln(u"The quick brown fox...");
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->ListIndent();
builder->Writeln(u"jumped over the lazy dog.");
builder->Writeln(u"jumped over the lazy dog.");

builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateCustomList.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
