---
title: "طريقة Aspose::Words::FileFormatUtil::LoadFormatToExtension"
linktitle: "LoadFormatToExtension"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::FileFormatUtil::LoadFormatToExtension. تقوم بتحويل قيمة تنسيق التحميل المُعدَّة إلى امتداد ملف. يكون الامتداد المُرجع سلسلة بحروف صغيرة مع نقطة في البداية في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words/fileformatutil/loadformattoextension/
---
## FileFormatUtil::LoadFormatToExtension method


يحوّل قيمة تعداد صيغة التحميل إلى امتداد ملف. الامتداد المُرجع هو سلسلة بحروف صغيرة مع نقطة في البداية.

```cpp
static System::String Aspose::Words::FileFormatUtil::LoadFormatToExtension(Aspose::Words::LoadFormat loadFormat)
```

## ملاحظات


قيمة [WordML](../../saveformat/) تُحول إلى ".wml".

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

* Enum [LoadFormat](../../loadformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
