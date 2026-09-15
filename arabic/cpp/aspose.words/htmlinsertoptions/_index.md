---
title: "Aspose::Words::HtmlInsertOptions enum"
linktitle: "HtmlInsertOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::HtmlInsertOptions enum. يحدد الخيارات لـ طريقة InsertHtml() في C++."
type: docs
weight: 92000
url: /ar/cpp/aspose.words/htmlinsertoptions/
---
## HtmlInsertOptions enum


يحدد الخيارات لطريقة [InsertHtml()](../).

```cpp
enum class HtmlInsertOptions
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | 0 | استخدم الخيارات الافتراضية عند إدراج HTML. |
| UseBuilderFormatting | 1 | استخدم تنسيق الخط والفقرة المحدد في [DocumentBuilder](../documentbuilder/) كتنسيق أساسي للنص المُدرج من HTML. |
| RemoveLastEmptyParagraph | 2 | أزل الفقرة الفارغة التي تُدرج عادةً بعد HTML التي تنتهي بعنصر على مستوى الكتلة. |
| PreserveBlocks | 4 | احفظ خصائص العناصر على مستوى الكتلة. |


## أمثلة



يوضح كيفية السماح بحفظ أفضل للحدود والهوامش المرئية.
```cpp
const System::String html = u"\r\n                <html>\r\n                    <div style='border:dotted'>\r\n                    <div style='border:solid'>\r\n                        <p>paragraph 1</p>\r\n                        <p>paragraph 2</p>\r\n                    </div>\r\n                    </div>\r\n                </html>";

// قم بتعيين وضع الاستيراد الجديد لعناصر HTML على مستوى الكتلة.
Aspose::Words::HtmlInsertOptions insertOptions = Aspose::Words::HtmlInsertOptions::PreserveBlocks;

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();
builder->InsertHtml(html, insertOptions);
builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.PreserveBlocks.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
