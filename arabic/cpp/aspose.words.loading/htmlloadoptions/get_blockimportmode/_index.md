---
title: "طريقة Aspose::Words::Loading::HtmlLoadOptions::get_BlockImportMode"
linktitle: "get_BlockImportMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Loading::HtmlLoadOptions::get_BlockImportMode. يحصل على أو يعيّن قيمة تحدد كيفية استيراد خصائص العناصر ذات المستوى الكتلي. القيمة الافتراضية هي Merge في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.loading/htmlloadoptions/get_blockimportmode/
---
## HtmlLoadOptions::get_BlockImportMode method


يحصل على أو يعيّن قيمة تحدد كيفية استيراد خصائص العناصر ذات المستوى الكتلي. القيمة الافتراضية هي [Merge](../../blockimportmode/).

```cpp
Aspose::Words::Loading::BlockImportMode Aspose::Words::Loading::HtmlLoadOptions::get_BlockImportMode() const
```


## أمثلة



يوضح كيفية استيراد خصائص العناصر على مستوى الكتلة من المستندات المستندة إلى HTML.
```cpp
const System::String html = u"\r\n            <html>\r\n                <div style='border:dotted'>\r\n                    <div style='border:solid'>\r\n                        <p>paragraph 1</p>\r\n                        <p>paragraph 2</p>\r\n                    </div>\r\n                </div>\r\n            </html>";
auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html));

auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
// قم بتعيين وضع الاستيراد الجديد لعناصر HTML على مستوى الكتلة.
loadOptions->set_BlockImportMode(blockImportMode);

auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BlockImport.docx");
```

## انظر أيضًا

* Enum [BlockImportMode](../../blockimportmode/)
* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
