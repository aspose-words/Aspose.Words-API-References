---
title: "Aspose::Words::NodeImporter::ImportNode طريقة"
linktitle: "ImportNode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::NodeImporter::ImportNode طريقة. يستورد عقدة من مستند إلى آخر في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/nodeimporter/importnode/
---
## NodeImporter::ImportNode method


يستورد عقدة من مستند إلى آخر.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::NodeImporter::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | العقدة المراد استيرادها. |
| isImportChildren | bool | **true** لاستيراد جميع العقد الفرعية بشكل متكرر؛ وإلا، **false**. |

### ReturnValue

العقدة المستنسخة والمستوردة. العقدة تنتمي إلى المستند الوجهة، ولكن لا أصل لها.
## ملاحظات


استيراد عقدة ينشئ نسخة من العقدة المصدر التي تنتمي إلى المستند المستورد. العقدة المرتجعة لا تحتوي على أصل. العقدة المصدر لا تُعدَّل أو تُزال من المستند الأصلي.

قبل أن يتم إدراج عقدة من مستند آخر في هذا المستند، يجب استيرادها. أثناء الاستيراد، تُترجم خصائص المستند الخاصة مثل الإشارات إلى الأنماط والقوائم من الأصلي إلى المستند المستورد. بعد استيراد العقدة، يمكن إدراجها في الموضع المناسب في المستند باستخدام [InsertBefore1()</see> أو <see cref=\"Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertAfter1()](../).

إذا كانت العقدة المصدر تنتمي بالفعل إلى المستند الوجهة، فسيتم ببساطة إنشاء نسخة عميقة من العقدة المصدر.

## انظر أيضًا

* Class [Node](../../node/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
