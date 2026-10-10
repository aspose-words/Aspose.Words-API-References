---
title: "Aspose::Words::Saving::Zip64Mode enum"
linktitle: "Zip64Mode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::Zip64Mode enum. يحدد متى يتم استخدام امتدادات تنسيق ZIP64 لملفات OOXML في C++."
type: docs
weight: 88000
url: /ar/cpp/aspose.words.saving/zip64mode/
---
## Zip64Mode enum


يحدد متى يتم استخدام امتدادات تنسيق ZIP64 لملفات OOXML.

```cpp
enum class Zip64Mode
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| أبدًا | 0 | لا تستخدم امتدادات تنسيق ZIP64. |
| IfNecessary | 1 | إذا لزم الأمر، استخدم امتدادات تنسيق ZIP64. |
| دائمًا | 2 | استخدم دائمًا امتدادات تنسيق ZIP64. |


## أمثلة



يظهر كيفية استخدام امتدادات تنسيق ZIP64.
```cpp
System::Random random;
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

for (int32_t i = 0; i < 10000; i++)
{
    {
        auto bmp = System::MakeObject<System::Drawing::Bitmap>(5, 5);
        {
            System::SharedPtr<System::Drawing::Graphics> g = System::Drawing::Graphics::FromImage(bmp);
            g->Clear(System::Drawing::Color::FromArgb(random.Next(0, 254), random.Next(0, 254), random.Next(0, 254)));
            {
                auto ms = System::MakeObject<System::IO::MemoryStream>();
                bmp->Save(ms, System::Drawing::Imaging::ImageFormat::get_Png());
                builder->InsertImage(ms->ToArray());
            }
        }
    }
}
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Zip64Mode(Aspose::Words::Saving::Zip64Mode::Always);

builder->get_Document()->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Zip64ModeOption.docx", saveOptions);
```

## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
