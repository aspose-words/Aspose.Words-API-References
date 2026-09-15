---
title: "Aspose::Words::StoryType enum"
linktitle: "StoryType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::StoryType enum. يتم تخزين نص مستند Word في قصص. يحدد StoryType قصة في C++."
type: docs
weight: 117000
url: /ar/cpp/aspose.words/storytype/
---
## StoryType enum


يتم تخزين نص مستند Word في قصص. [StoryType](./) يحدد قصة.

```cpp
enum class StoryType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | 0 | القيمة الافتراضية. لا توجد مثل هذه القصة في المستند. |
| MainText | 1 | يحتوي على النص الرئيسي للمستند، ممثلًا بـ [Body](../body/). |
| Footnotes | 2 | يحتوي على نص الحاشية السفلية، ممثلًا بـ [Footnote](../../aspose.words.notes/footnote/). |
| Endnotes | 3 | يحتوي على نص الحواشي الختامية، ممثلًا بـ [Footnote](../../aspose.words.notes/footnote/). |
| Comments | 4 | يحتوي على تعليقات المستند (التعليقات التوضيحية)، ممثلًا بـ [Comment](../comment/). |
| Textbox | 5 | يحتوي على نص الشكل أو مربع النص، ممثلًا بـ [Shape](../../aspose.words.drawing/shape/). |
| EvenPagesHeader | 6 | يحتوي على نص رأس الصفحات الزوجية، ممثلًا بـ [HeaderFooter](../headerfooter/). |
| PrimaryHeader | 7 | يحتوي على نص الرأس الأساسي. عندما يكون الرأس مختلفًا للصفحات الفردية والزوجية، يحتوي على نص رأس الصفحات الفردية. ممثلًا بـ [HeaderFooter](../headerfooter/). |
| EvenPagesFooter | 8 | يحتوي على نص تذييل الصفحات الزوجية، ممثلًا بـ [HeaderFooter](../headerfooter/). |
| PrimaryFooter | 9 | يحتوي على نص التذييل الأساسي. عندما يكون التذييل مختلفًا للصفحات الفردية والزوجية، يحتوي على نص تذييل الصفحات الفردية. ممثلًا بـ [HeaderFooter](../headerfooter/). |
| FirstPageHeader | 10 | يحتوي على نص رأس الصفحة الأولى، ممثلًا بـ [HeaderFooter](../headerfooter/). |
| FirstPageFooter | 11 | يحتوي على نص تذييل الصفحة الأولى، ممثلًا بـ [HeaderFooter](../headerfooter/). |
| FootnoteSeparator | 12 | يحتوي على نص فاصل الحاشية السفلية. |
| فاصل استمرار الحاشية السفلية | 13 | يحتوي على نص فاصل استمرار الحاشية السفلية. |
| إشعار استمرار الحاشية السفلية | 14 | يحتوي على نص فاصل إشعار استمرار الحاشية السفلية. |
| فاصل الحاشية الختامية | 15 | يحتوي على نص فاصل الحاشية السفلية. |
| فاصل استمرار الحاشية الختامية | 16 | يحتوي على نص فاصل استمرارية الحاشية السفلية. |
| إشعار استمرار الحاشية الختامية | 17 | يحتوي على نص فاصل إشعار استمرارية الحاشية السفلية. |


## أمثلة



يُظهر كيفية إزالة جميع الأشكال من عقدة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// استخدم DocumentBuilder لإدراج شكل. هذا شكل مضمن،
// الذي له فقرة أصل، وهي عقدة فرعية لجسم القسم الأول.
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 100.0, 100.0);

ASSERT_EQ(1, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// يمكننا حذف جميع الأشكال من الفقرات الفرعية لهذا الجسم.
ASSERT_EQ(Aspose::Words::StoryType::MainText, doc->get_FirstSection()->get_Body()->get_StoryType());
doc->get_FirstSection()->get_Body()->DeleteShapes();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
