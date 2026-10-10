---
title: "Aspose::Words::NodeImporter class"
linktitle: "NodeImporter"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::NodeImporter class. يسمح بأداء استيراد متكرر للعقد من مستند إلى آخر بكفاءة. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 44000
url: /ar/cpp/aspose.words/nodeimporter/
---
## NodeImporter class


يسمح بأداء استيراد متكرر للعقد من مستند إلى آخر بكفاءة. لمعرفة المزيد، زر مقالة الوثائق [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/)

```cpp
class NodeImporter : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | يستورد عقدة من مستند إلى آخر. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeImporter](./nodeimporter/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode) | يُنشئ مثيلاً جديدًا من الفئة [NodeImporter](./). |
| [NodeImporter](./nodeimporter/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | يُنشئ مثيلاً جديدًا من الفئة [NodeImporter](./). |
| static [Type](./type/)() |  |
## ملاحظات


توفر Aspose.Words وظائف لنسخ وتحريك القطع بسهولة بين مستندات Microsoft Word. يُعرف هذا بـ "استيراد العقد". قبل أن تتمكن من إدراج قطعة من مستند إلى آخر، تحتاج إلى "استيراد"ها. يُنشئ الاستيراد نسخة عميقة من العقدة الأصلية، جاهزة للإدراج في المستند الهدف.

أسهل طريقة لاستيراد عقدة هي استخدام الطريقة [ImportNode()](../) المقدمة من كائن [DocumentBase](../documentbase/).

مع ذلك، عندما تحتاج إلى استيراد عقد من مستند إلى آخر عدة مرات، من الأفضل استخدام الفئة [NodeImporter](./). تسمح الفئة [NodeImporter](./) بتقليل عدد الأنماط والقوائم التي تُنشأ في المستند الهدف.

إن نسخ أو نقل القطع من مستند Microsoft Word إلى آخر يطرح عددًا من التحديات التقنية لـ Aspose.Words. في مستند Word، يتم تخزين الأنماط وتنسيق القوائم مركزيًا، منفصلًا عن نص المستند. الفقرات وتدفقات النص تشير إلى الأنماط فقط عبر معرفات داخلية فريدة.

تنشأ التحديات من اختلاف الأنماط والقوائم بين المستندات المختلفة. على سبيل المثال، لنسخ فقرة مُنسقة بنمط Heading 1 من مستند إلى آخر، يجب مراعاة عدة أمور: تحديد ما إذا كان يجب نسخ نمط Heading 1 من المستند المصدر إلى المستند الهدف، استنساخ الفقرة، وتحديث الفقرة المستنسخة لتشير إلى نمط Heading 1 الصحيح في المستند الهدف. إذا كان يجب نسخ النمط، يجب تحليل جميع الأنماط التي يشير إليها (استنادًا إلى النمط ونمط الفقرة التالية) وربما نسخها أيضًا وهكذا. توجد مشكلات مماثلة عند نسخ الفقرات ذات النقاط أو الترقيم لأن Microsoft Word يخزن تعريفات القوائم بشكل منفصل عن النص.

الفئة [NodeImporter](./) تشبه السياق، الذي يحتفظ بـ "جداول الترجمة" أثناء الاستيراد. إنها تُترجم بشكل صحيح بين الأنماط والقوائم في المستندات المصدر والهدف.

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
