---
title: "طريقة Aspose::Words::FileFormatUtil::SaveFormatToExtension"
linktitle: "SaveFormatToExtension"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::FileFormatUtil::SaveFormatToExtension. تحول قيمة تعداد تنسيق الحفظ إلى امتداد ملف. الامتداد المرتجع هو سلسلة بأحرف صغيرة مع نقطة في البداية في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words/fileformatutil/saveformattoextension/
---
## FileFormatUtil::SaveFormatToExtension method


يحوّل قيمة تعداد صيغة الحفظ إلى امتداد ملف. الامتداد المُرجع هو سلسلة بحروف صغيرة مع نقطة في البداية.

```cpp
static System::String Aspose::Words::FileFormatUtil::SaveFormatToExtension(Aspose::Words::SaveFormat saveFormat)
```

## ملاحظات


قيمة [WordML](../../saveformat/) تُحول إلى ".wml".

قيمة [FlatOpc](../../saveformat/) تُحول إلى ".fopc".

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
