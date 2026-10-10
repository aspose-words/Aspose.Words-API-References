---
title: "طريقة Aspose::Words::Fonts::FolderFontSource::get_Type"
linktitle: "get_Type"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fonts::FolderFontSource::get_Type. تُرجع نوع مصدر الخط في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.fonts/folderfontsource/get_type/
---
## FolderFontSource::get_Type method


يعيد نوع مصدر الخط.

```cpp
Aspose::Words::Fonts::FontSourceType Aspose::Words::Fonts::FolderFontSource::get_Type() override
```


## أمثلة



يظهر كيفية استخدام مجلد نظام محلي يحتوي على خطوط كمصدر للخط.
```cpp
// إنشاء مصدر خط من مجلد يحتوي على ملفات الخطوط.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false, 1);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

ASSERT_EQ(get_FontsDir(), folderFontSource->get_FolderPath());
ASPOSE_ASSERT_EQ(false, folderFontSource->get_ScanSubfolders());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontsFolder, folderFontSource->get_Type());
ASSERT_EQ(1, folderFontSource->get_Priority());
```

## انظر أيضًا

* Enum [FontSourceType](../../fontsourcetype/)
* Class [FolderFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
