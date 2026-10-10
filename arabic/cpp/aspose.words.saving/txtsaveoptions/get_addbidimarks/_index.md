---
title: "Aspose::Words::Saving::TxtSaveOptions::get_AddBidiMarks method"
linktitle: "get_AddBidiMarks"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::TxtSaveOptions::get_AddBidiMarks method. يحدد ما إذا كان يجب إضافة علامات ثنائية الاتجاه قبل كل تشغيل BiDi عند التصدير بتنسيق النص العادي. القيمة الافتراضية هي false في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.saving/txtsaveoptions/get_addbidimarks/
---
## TxtSaveOptions::get_AddBidiMarks method


يحدد ما إذا كان سيتم إضافة علامات ثنائية الاتجاه قبل كل مقطع BiDi عند التصدير بتنسيق النص العادي. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptions::get_AddBidiMarks() const
```


## أمثلة



يظهر كيفية إدراج حرف Unicode 'RIGHT-TO-LEFT MARK' (U+200F) قبل كل [Run](../../../aspose.words/run/) ثنائي الاتجاه في النص.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->get_ParagraphFormat()->set_Bidi(true);
builder->Writeln(u"שלום עולם!");
builder->Writeln(u"مرحبا بالعالم!");

// إنشاء كائن "TxtSaveOptions"، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل طريقة حفظ المستند كنص عادي.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_Encoding(System::Text::Encoding::get_Unicode());

// عيّن خاصية "AddBidiMarks" إلى "true" لإضافة العلامات قبل التشغيلات
// مع نص من اليمين إلى اليسار لتوضيح ذلك.
// عيّن خاصية "AddBidiMarks" إلى "false" لكتابة جميع النصوص من اليسار إلى اليمين
// والتشغيلات من اليمين إلى اليسار بشكل متساوٍ دون أي شيء لتحديد أيهما أي.
saveOptions->set_AddBidiMarks(addBidiMarks);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.AddBidiMarks.txt", saveOptions);

System::String docText = System::Text::Encoding::get_Unicode()->GetString(System::IO::File::ReadAllBytes(get_ArtifactsDir() + u"TxtSaveOptions.AddBidiMarks.txt"));

if (addBidiMarks)
{
    ASSERT_EQ(u"\ufeffHello world!‎\r\nשלום עולם!‏\r\nمرحبا بالعالم!‏\r\n\r\n", docText);
    ASSERT_TRUE(docText.Contains(u"\u200f"));
}
else
{
    ASSERT_EQ(u"\ufeffHello world!\r\nשלום עולם!\r\nمرحبا بالعالم!\r\n\r\n", docText);
    ASSERT_FALSE(docText.Contains(u"\u200f"));
}
```

## انظر أيضًا

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
