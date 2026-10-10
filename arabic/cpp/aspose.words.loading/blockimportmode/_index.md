---
title: "Aspose::Words::Loading::BlockImportMode enum"
linktitle: "BlockImportMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Loading::BlockImportMode enum. يحدد كيفية استيراد خصائص العناصر على مستوى الكتلة من المستندات المستندة إلى HTML في C++."
type: docs
weight: 12000
url: /ar/cpp/aspose.words.loading/blockimportmode/
---
## BlockImportMode enum


يحدد كيفية استيراد خصائص العناصر على مستوى الكتلة من المستندات المستندة إلى HTML.

```cpp
enum class BlockImportMode
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| Merge | 0 | [Properties](../../aspose.words.properties/) للكتل الأصلية يتم دمجها وتخزينها على العناصر الفرعية (مثل الفقرات أو الجداول). |
| Preserve | 1 | [Properties](../../aspose.words.properties/) للكتل الأصلية يتم استيرادها إلى بنية منطقية خاصة وتُخزن بشكل منفصل عن عقد المستند. |


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

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
