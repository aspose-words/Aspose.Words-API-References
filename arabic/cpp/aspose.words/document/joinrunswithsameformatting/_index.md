---
title: "Aspose::Words::Document::JoinRunsWithSameFormatting method"
linktitle: "JoinRunsWithSameFormatting"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Document::JoinRunsWithSameFormatting method. يجمع المقاطع ذات التنسيق المتطابق في جميع فقرات المستند بلغة C++."
type: docs
weight: 65000
url: /ar/cpp/aspose.words/document/joinrunswithsameformatting/
---
## Document::JoinRunsWithSameFormatting method


يجمع المقاطع ذات التنسيق نفسه في جميع فقرات المستند.

```cpp
int32_t Aspose::Words::Document::JoinRunsWithSameFormatting()
```


### ReturnValue

عدد عمليات الجمع التي تم تنفيذها. عندما يتم جمع **N** مقاطع متجاورة تُحسب كـ **N - 1** عمليات جمع.
## ملاحظات


هذه طريقة تحسين. بعض المستندات تحتوي على مقاطع متجاورة ذات تنسيق متطابق. عادةً ما يحدث ذلك إذا تم تعديل المستند يدوياً بشكل مكثف. يمكنك تقليل حجم المستند وتسريع المعالجة اللاحقة عن طريق جمع هذه المقاطع.

تتحقق العملية من كل عقدة [Paragraph](../../paragraph/) في المستند للعثور على عقد [Run](../../run/) المتجاورة التي لها خصائص متطابقة. تتجاهل المعرفات الفريدة المستخدمة لتتبع جلسات تحرير إنشاء وتعديل المقاطع. يجمّع أول مقطع في كل سلسلة جمع كل النص. تُحذف المقاطع المتبقية من المستند.

## أمثلة



يظهر كيفية جمع المقاطع في مستند لتقليل المقاطع غير الضرورية.
```cpp
// افتح مستندًا يحتوي على مقاطع نصية متجاورة ذات تنسيق متطابق،
// وهو ما يحدث عادةً إذا قمنا بتحرير الفقرة نفسها عدة مرات في Microsoft Word.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// إذا كان أي عدد من هذه المقاطع متجاورًا بتنسيق متطابق،
// فإن المستند قد يُبسّط.
ASSERT_EQ(317, doc->GetChildNodes(Aspose::Words::NodeType::Run, true)->get_Count());

// اجمع هذه المقاطع باستخدام هذه الطريقة وتحقق من عدد عمليات الجمع التي ستجري.
ASSERT_EQ(121, doc->JoinRunsWithSameFormatting());

// عدد عمليات الجمع وعدد المقاطع التي لدينا بعد الجمع
// يجب أن يساوي مجموع عدد المقاطع التي كان لدينا في البداية.
ASSERT_EQ(196, doc->GetChildNodes(Aspose::Words::NodeType::Run, true)->get_Count());
```

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
