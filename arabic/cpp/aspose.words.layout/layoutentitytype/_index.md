---
title: "Aspose::Words::Layout::LayoutEntityType تعداد"
linktitle: "LayoutEntityType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Layout::LayoutEntityType تعداد. أنواع الكيانات التخطيطية في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.layout/layoutentitytype/
---
## LayoutEntityType enum


أنواع كيانات التخطيط.

```cpp
enum class LayoutEntityType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | n/a | القيمة الافتراضية. |
| Page | n/a | يمثل صفحة من مستند. قد تحتوي الصفحة على كيانات فرعية مثل [Column](./)، [HeaderFooter](./) و[Comment](./). |
| Column | n/a | يمثل عمودًا من النص على صفحة. قد يحتوي العمود على نفس الكيانات الفرعية مثل [Cell](./)، بالإضافة إلى كيانات [Footnote](./)، [Endnote](./) و[NoteSeparator](./). |
| Row | n/a | يمثل صفًا في جدول. قد يحتوي الصف على [Cell](./) ككيانات فرعية. |
| Cell | n/a | يمثل خلية جدول. قد تحتوي الخلية على كيانات فرعية مثل [Line](./) و[Row](./). |
| Line | n/a | يمثل سطرًا من أحرف النص والكائنات المضمنة. قد يحتوي السطر على كيانات فرعية مثل [Span](./). |
| Span | n/a | يمثل حرفًا واحدًا أو أكثر في سطر. يتضمن ذلك أحرفًا خاصة مثل علامات بدء/إنهاء الحقل، والإشارات المرجعية، والتعليقات. لا يمكن أن يحتوي Span على كيانات فرعية. |
| Footnote | n/a | يمثل عنصرًا نائبًا لمحتوى الحاشية السفلية. قد يحتوي Footnote على كيانات فرعية من نوع [Note](./). |
| Endnote | n/a | يمثل عنصرًا نائبًا لمحتوى الحاشية الختامية. قد يحتوي Endnote على كيانات فرعية من نوع [Note](./). |
| Note | n/a | يمثل عنصرًا نائبًا لمحتوى الملاحظة. قد يحتوي Note على كيانات فرعية من نوع [Line](./) و[Row](./). |
| HeaderFooter | n/a | يمثل عنصرًا نائبًا لمحتوى الرأس/التذييل في الصفحة. قد يحتوي [HeaderFooter](../../aspose.words/headerfooter/) على كيانات فرعية من نوع [Line](./) و[Row](./). |
| TextBox | n/a | يمثل منطقة نص داخل شكل. قد يحتوي Textbox على كيانات فرعية من نوع [Line](./) و[Row](./). |
| Comment | n/a | يمثل عنصرًا نائبًا لمحتوى التعليق. قد يحتوي [Comment](../../aspose.words/comment/) على كيانات فرعية من نوع [Line](./) و[Row](./). |
| NoteSeparator | n/a | يمثل فاصل الحاشية السفلية/الحاشية الختامية. قد يحتوي NoteSeparator على كيانات فرعية من نوع [Line](./) و[Row](./). |

## انظر أيضًا

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
