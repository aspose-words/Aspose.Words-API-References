---
title: "طريقة Aspose::Words::Fonts::FolderFontSource::get_FolderPath"
linktitle: "get_FolderPath"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fonts::FolderFontSource::get_FolderPath. المسار إلى المجلد في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.fonts/folderfontsource/get_folderpath/
---
## FolderFontSource::get_FolderPath method


المسار إلى المجلد.

```cpp
System::String Aspose::Words::Fonts::FolderFontSource::get_FolderPath() const
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

* Class [FolderFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
