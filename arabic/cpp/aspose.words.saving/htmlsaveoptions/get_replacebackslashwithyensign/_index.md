---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ReplaceBackslashWithYenSign طريقة"
linktitle: "get_ReplaceBackslashWithYenSign"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ReplaceBackslashWithYenSign طريقة. يحدد ما إذا كان يجب استبدال أحرف الشرطة المائلة (\\\\) بعلامات الين. القيمة الافتراضية هي false في C++."
type: docs
weight: 41500
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_replacebackslashwithyensign/
---
## HtmlSaveOptions::get_ReplaceBackslashWithYenSign method


يحدد ما إذا كان يجب استبدال أحرف الشرطة المائلة الخلفية بعلامات الين. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ReplaceBackslashWithYenSign() const
```


## أمثلة



يوضح كيفية استبدال أحرف الشرطة المائلة بعلامات الين (Html).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Korean backslash symbol.docx");

// بشكل افتراضي، تحاكي Aspose.Words سلوك MS Word ولا تستبدل أحرف الشرطة المائلة بعلامات الين في
// مستندات HTML التي تم إنشاؤها. ومع ذلك، قامت الإصدارات السابقة من Aspose.Words بإجراء مثل هذه الاستبدالات في بعض
// السيناريوهات. يتيح هذا العلم التوافقية الرجعية مع الإصدارات السابقة من Aspose.Words.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_ReplaceBackslashWithYenSign(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ReplaceBackslashWithYenSign.html", saveOptions);
```

## انظر أيضًا

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
