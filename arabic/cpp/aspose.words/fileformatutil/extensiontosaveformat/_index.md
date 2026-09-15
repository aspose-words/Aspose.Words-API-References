---
title: "طريقة Aspose::Words::FileFormatUtil::ExtensionToSaveFormat"
linktitle: "ExtensionToSaveFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::FileFormatUtil::ExtensionToSaveFormat. تقوم بتحويل امتداد اسم الملف إلى قيمة SaveFormat في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/fileformatutil/extensiontosaveformat/
---
## FileFormatUtil::ExtensionToSaveFormat method


تحول امتداد اسم الملف إلى قيمة [SaveFormat](../../saveformat/).

```cpp
static Aspose::Words::SaveFormat Aspose::Words::FileFormatUtil::ExtensionToSaveFormat(const System::String &extension)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| امتداد | const System::String\& | امتداد الملف. يمكن أن يكون مع نقطة في البداية أو بدونها. غير حساس لحالة الأحرف. |
## ملاحظات


إذا تعذر التعرف على الامتداد، تُعيد [Unknown](../../saveformat/).

## أمثلة



يظهر كيفية استخدام طرق [FileFormatUtil](../) لاكتشاف تنسيق المستند.
```cpp
// حمّل مستندًا من ملف يفتقر إلى امتداد ملف، ثم اكتشف تنسيق الملف.
{
    System::SharedPtr<System::IO::FileStream> docStream = System::IO::File::OpenRead(get_MyDir() + u"Word document with missing file extension");
    System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(docStream);
    Aspose::Words::LoadFormat loadFormat = info->get_LoadFormat();

    ASSERT_EQ(Aspose::Words::LoadFormat::Doc, loadFormat);

    // فيما يلي طريقتان لتحويل LoadFormat إلى SaveFormat المقابل.
    // 1 - احصل على سلسلة امتداد الملف لـ LoadFormat، ثم احصل على SaveFormat المقابل من تلك السلسلة:
    System::String fileExtension = Aspose::Words::FileFormatUtil::LoadFormatToExtension(loadFormat);
    Aspose::Words::SaveFormat saveFormat = Aspose::Words::FileFormatUtil::ExtensionToSaveFormat(fileExtension);

    // 2 - حوّل LoadFormat مباشرةً إلى SaveFormat الخاص به:
    saveFormat = Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat(loadFormat);

    // حمّل مستندًا من الدفق، ثم احفظه بامتداد الملف المكتشف تلقائيًا.
    auto doc = System::MakeObject<Aspose::Words::Document>(docStream);

    ASSERT_EQ(u".doc", Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));

    doc->Save(get_ArtifactsDir() + u"File.SaveToDetectedFileFormat" + Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));
}
```

## انظر أيضًا

* Enum [SaveFormat](../../saveformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
