---
title: "Aspose::Words::Fonts::FolderFontSource::FolderFontSource constructor"
linktitle: "FolderFontSource"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fonts::FolderFontSource::FolderFontSource constructor. منشئ في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fonts/folderfontsource/folderfontsource/
---
## FolderFontSource::FolderFontSource(const System::String\&, bool) constructor


منشئ.

```cpp
Aspose::Words::Fonts::FolderFontSource::FolderFontSource(const System::String &folderPath, bool scanSubfolders)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| folderPath | const System::String\& | المسار إلى المجلد. |
| scanSubfolders | bool | يحدد ما إذا كان يجب مسح المجلدات الفرعية أم لا. |

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
## FolderFontSource::FolderFontSource(const System::String\&, bool, int32_t) constructor


منشئ.

```cpp
Aspose::Words::Fonts::FolderFontSource::FolderFontSource(const System::String &folderPath, bool scanSubfolders, int32_t priority)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| folderPath | const System::String\& | المسار إلى المجلد. |
| scanSubfolders | bool | يحدد ما إذا كان يجب مسح المجلدات الفرعية أم لا. |
| priority | int32_t | [Font](../../../aspose.words/font/) أولوية المصدر. راجع وصف خاصية [Priority](../../fontsourcebase/get_priority/) لمزيد من المعلومات. |

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
