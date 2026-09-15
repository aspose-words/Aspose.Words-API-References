---
title: "Aspose::Words::Saving::OoxmlSaveOptions::get_KeepLegacyControlChars طريقة"
linktitle: "get_KeepLegacyControlChars"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_KeepLegacyControlChars طريقة. يحافظ على التمثيل الأصلي لأحرف التحكم القديمة في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.saving/ooxmlsaveoptions/get_keeplegacycontrolchars/
---
## OoxmlSaveOptions::get_KeepLegacyControlChars method


يحافظ على تمثيل الأحرف التحكمية القديمة الأصلي.

```cpp
bool Aspose::Words::Saving::OoxmlSaveOptions::get_KeepLegacyControlChars() const
```


## أمثلة



يوضح كيفية دعم أحرف التحكم القديمة عند التحويل إلى .docx.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Legacy control character.doc");

// عند حفظ المستند بتنسيق OOXML، يمكننا إنشاء كائن OoxmlSaveOptions
// ثم نمرره إلى طريقة حفظ المستند لتعديل طريقة حفظ المستند.
// عيّن الخاصية "KeepLegacyControlChars" إلى "true" للحفاظ على
// حرف "ShortDateTime" القديم أثناء الحفظ.
// عيّن الخاصية "KeepLegacyControlChars" إلى "false" لإزالة
// حرف "ShortDateTime" القديم من المستند الناتج.
auto so = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
so->set_KeepLegacyControlChars(keepLegacyControlChars);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx");

ASSERT_EQ(keepLegacyControlChars ? System::String(u"\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f") : System::String(u"\u001e\f"), doc->get_FirstSection()->get_Body()->GetText());
```

## انظر أيضًا

* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
