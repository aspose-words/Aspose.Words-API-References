---
title: "طريقة Aspose::Words::ImportFormatOptions::get_MergePastedLists"
linktitle: "get_MergePastedLists"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::ImportFormatOptions::get_MergePastedLists. يحصل على أو يعيّن قيمة منطقية تحدد ما إذا كانت القوائم الملصوقة سيتم دمجها مع القوائم المحيطة. القيمة الافتراضية هي false في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words/importformatoptions/get_mergepastedlists/
---
## ImportFormatOptions::get_MergePastedLists method


يحصل أو يضبط قيمة منطقية تحدد ما إذا كانت القوائم الملصوقة ستدمج مع القوائم المحيطة. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_MergePastedLists() const
```


## أمثلة



يظهر كيفية دمج القوائم من مستند.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List destination.docx");

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_MergePastedLists(true);

// قم بتعيين الخاصية "MergePastedLists" إلى "true" سيتم دمج القوائم الملصوقة مع القوائم المحيطة.
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles, options);

dstDoc->Save(get_ArtifactsDir() + u"Document.MergePastedLists.docx");
```

## انظر أيضًا

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
