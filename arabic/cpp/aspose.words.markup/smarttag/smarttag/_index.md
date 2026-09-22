---
title: "منشئ Aspose::Words::Markup::SmartTag::SmartTag"
linktitle: "SmartTag"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "منشئ Aspose::Words::Markup::SmartTag::SmartTag. يهيئ نسخة جديدة من فئة SmartTag في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.markup/smarttag/smarttag/
---
## SmartTag::SmartTag constructor


يهيئ نسخة جديدة من الفئة [SmartTag](../).

```cpp
Aspose::Words::Markup::SmartTag::SmartTag(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | المستند المالك. |
## ملاحظات


عند إنشاء عقدة جديدة، تحتاج إلى تحديد المستند الذي تنتمي إليه العقدة. لا يمكن للعقدة أن توجد بدون مستند لأنها تعتمد على هياكل المستند العامة مثل القوائم والأنماط. على الرغم من أن العقدة دائمًا ما تنتمي إلى مستند، قد تكون العقدة جزءًا من شجرة المستند أو لا تكون.

عند إنشاء عقدة، تنتمي إلى مستند، لكنها ليست بعد جزءًا من شجرة المستند و[ParentNode](../../../aspose.words/node/get_parentnode/) يساوي null. لإدراج عقدة في المستند، استخدم طرق [InsertAfter1()</see> أو <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)\">InsertBefore1()](../) على العقدة الأصل.

## انظر أيضًا

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [SmartTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
