---
title: "Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels method"
linktitle: "get_SimplifyListLabels"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels method. يحدد ما إذا كان يجب على البرنامج تبسيط تسميات القوائم في حالة عدم تمثيل تنسيق التسميات المعقد بشكل كافٍ في النص العادي. إذا تم تعيينه إلى true، تُكتب تسميات القوائم المرقمة بتنسيق رقمي بسيط وتُكتب تسميات القوائم النقطية كحروف ASCII بسيطة. القيمة الافتراضية هي false في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.saving/txtsaveoptions/get_simplifylistlabels/
---
## TxtSaveOptions::get_SimplifyListLabels method


يحدد ما إذا كان البرنامج يجب أن يبسط تسميات القوائم في حالة عدم تمثيل تنسيق التسميات المعقد بشكل كافٍ في النص العادي. إذا تم ضبطه على **true**، تُكتب تسميات القوائم المرقمة بصيغة رقمية بسيطة وتُكتب تسميات القوائم النقطية كحروف ASCII بسيطة. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptions::get_SimplifyListLabels() const
```


## أمثلة



يظهر كيفية تغيير مظهر القوائم عند حفظ المستند كنص عادي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إنشاء قائمة نقطية بخمس مستويات من المسافات البادئة.
builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Item 1");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 2");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 3");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 4");
builder->get_ListFormat()->ListIndent();
builder->Write(u"Item 5");

// إنشاء كائن "TxtSaveOptions"، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل طريقة حفظ المستند كنص عادي.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// عيّن خاصية "SimplifyListLabels" إلى "true" لتحويل بعض القوائم
// الرموز إلى أحرف ASCII أبسط، مثل '*', 'o', '+', '>', إلخ.
// عيّن خاصية "SimplifyListLabels" إلى "false" للحفاظ على أكبر عدد ممكن من رموز القوائم الأصلية.
txtSaveOptions->set_SimplifyListLabels(simplifyListLabels);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.SimplifyListLabels.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.SimplifyListLabels.txt");

System::String newLine = System::Environment::get_NewLine();
if (simplifyListLabels)
{
    ASSERT_EQ(System::String::Format(u"* Item 1{0}", newLine) + System::String::Format(u"  > Item 2{0}", newLine) + System::String::Format(u"    + Item 3{0}", newLine) + System::String::Format(u"      - Item 4{0}", newLine) + System::String::Format(u"        o Item 5{0}", newLine), docText);
}
else
{
    ASSERT_EQ(System::String::Format(u"· Item 1{0}", newLine) + System::String::Format(u"o Item 2{0}", newLine) + System::String::Format(u"§ Item 3{0}", newLine) + System::String::Format(u"· Item 4{0}", newLine) + System::String::Format(u"o Item 5{0}", newLine), docText);
}
```

## انظر أيضًا

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
