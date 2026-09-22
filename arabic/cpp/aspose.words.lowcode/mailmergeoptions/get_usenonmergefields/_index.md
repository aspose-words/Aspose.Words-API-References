---
title: "طريقة Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields"
linktitle: "get_UseNonMergeFields"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields. عندما تكون true، تحدد أنه بالإضافة إلى حقول MERGEFIELD، يتم إجراء دمج البريد إلى بعض الأنواع الأخرى من الحقول وأيضًا إلى وسوم \"{{fieldName}}\" في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words.lowcode/mailmergeoptions/get_usenonmergefields/
---
## MailMergeOptions::get_UseNonMergeFields method


عند **true**، يحدد أنه بالإضافة إلى حقول MERGEFIELD، يتم تنفيذ دمج البريد في بعض الأنواع الأخرى من الحقول وأيضًا في وسوم "{{fieldName}}".

```cpp
bool Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields() const
```

## ملاحظات


عادةً، يتم تنفيذ دمج البريد فقط في حقول MERGEFIELD، لكن عدة عملاء بنوا تقاريرهم باستخدام حقول أخرى وكان لديهم العديد من المستندات التي تم إنشاؤها بهذه الطريقة. لتبسيط الترحيل (وبسبب أن هذا النهج استخدمه عدة عملاء بشكل مستقل) تم تقديم القدرة على دمج البريد في حقول أخرى.

عندما يتم تعيين [UseNonMergeFields](./) إلى **true**، سيقوم Aspose.Words بتنفيذ دمج البريد في الحقول التالية:

MERGEFIELD FieldName

MACROBUTTON NOMACRO FieldName

IF 0 = 0 "{FieldName}" ""

أيضًا، عندما يتم تعيين [UseNonMergeFields](./) إلى **true**، سيقوم Aspose.Words بتنفيذ دمج البريد في وسوم النص "{{fieldName}}". هذه ليست حقولًا، بل مجرد وسوم نصية.
## انظر أيضًا

* Class [MailMergeOptions](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
