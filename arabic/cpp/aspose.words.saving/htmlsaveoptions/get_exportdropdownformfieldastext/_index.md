---
title: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText"
linktitle: "get_ExportDropDownFormFieldAsText"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText. تتحكم في كيفية حفظ حقول النماذج المنسدلة إلى HTML أو MHTML. القيمة الافتراضية هي false في C++."
type: docs
weight: 15000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_exportdropdownformfieldastext/
---
## HtmlSaveOptions::get_ExportDropDownFormFieldAsText method


يتحكم في كيفية حفظ حقول النموذج المنسدلة إلى HTML أو MHTML. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText() const
```

## ملاحظات


عند الضبط إلى **true**، يتم تصدير حقول النماذج المنسدلة كنص عادي. وعند **false**، يتم تصديرها كعنصر SELECT في HTML.

عند التصدير إلى EPUB، يتم دائمًا حفظ حقول النماذج المنسدلة النصية كنص بسبب متطلبات هذا التنسيق.

## أمثلة



يظهر كيفية دمج حقول نماذج صندوق القوائم المنسدلة مع نص الفقرة عند الحفظ إلى html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// استخدم مُنشئ المستند لإدراج صندوق قوائم مع القيمة "Two" محددة.
builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"One", u"Two", u"Three"}), 1);

// علامة "ExportDropDownFormFieldAsText" لهذا الكائن SaveOptions تسمح لنا بـ
// التحكم في كيفية معالجة حفظ المستند إلى HTML لصناديق القوائم المنسدلة.
// ضبطه على "true" سيحول كل صندوق قوائم إلى نص بسيط
// الذي يعرض القيمة المحددة حاليًا في صندوق القوائم، مما يجعله ثابتًا.
// ضبطه على "false" سيحافظ على وظيفة صندوق القوائم باستخدام وسمي <select> و <option>.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportDropDownFormFieldAsText(exportDropDownFormFieldAsText);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.DropDownFormField.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.DropDownFormField.html");

if (exportDropDownFormFieldAsText)
{
    ASSERT_TRUE(outDocContents.Contains(u"<span>Two</span>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<select name=\"MyComboBox\">") + u"<option>One</option>" + u"<option selected=\"selected\">Two</option>" + u"<option>Three</option>" + u"</select>"));
}
```

## انظر أيضًا

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
