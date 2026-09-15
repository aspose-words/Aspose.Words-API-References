---
title: "Aspose::Words::Notes::FootnoteSeparatorType enum"
linktitle: "نوع فاصل الحاشية السفلية"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Notes::FootnoteSeparatorType enum. يحدد نوع فاصل الحاشية السفلية/الحاشية الختامية في C++."
type: docs
weight: 6500
url: /ar/cpp/aspose.words.notes/footnoteseparatortype/
---
## FootnoteSeparatorType enum


يحدد نوع الفاصل بين الحاشية السفلية/الحاشية الختامية.

```cpp
enum class FootnoteSeparatorType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| FootnoteSeparator | 0 | الفاصل بين النص الرئيسي ونص الحاشية السفلية. |
| فاصل استمرار الحاشية السفلية | 1 | يُطبع فوق نص الحاشية السفلية في الصفحة عندما يجب استمرار النص من صفحة سابقة. |
| إشعار استمرار الحاشية السفلية | 2 | يُطبع أسفل نص الحاشية السفلية في الصفحة عندما يجب استمرار نص الحاشية السفلية في صفحة لاحقة. |
| فاصل الحاشية الختامية | 3 | الفاصل بين النص الرئيسي ونص الحاشية الختامية. |
| فاصل استمرار الحاشية الختامية | 4 | يُطبع فوق نص الحاشية الختامية في الصفحة عندما يجب استمرار النص من صفحة سابقة. |
| إشعار استمرار الحاشية الختامية | 5 | يُطبع أسفل نص الحاشية الختامية في الصفحة عندما يجب استمرار نص الحاشية الختامية في صفحة لاحقة. |


## أمثلة



يعرض كيفية إزالة فاصل الحاشية الختامية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> endnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::EndnoteSeparator);
// إزالة فاصل الحاشية الختامية.
endnoteSeparator->get_FirstParagraph()->get_FirstChild()->Remove();
```


يظهر كيفية إدارة تنسيق فاصل الحاشية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> footnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::FootnoteSeparator);
// محاذاة فاصل الحاشية.
footnoteSeparator->get_FirstParagraph()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
```

## انظر أيضًا

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
