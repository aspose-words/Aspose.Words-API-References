---
title: "طريقة Aspose::Words::CompositeNode::SelectSingleNode"
linktitle: "SelectSingleNode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::CompositeNode::SelectSingleNode. تحدد أول Node يطابق تعبير XPath في C++."
type: docs
weight: 23000
url: /ar/cpp/aspose.words/compositenode/selectsinglenode/
---
## CompositeNode::SelectSingleNode method


تحدد أول [Node](../../node/) يطابق تعبير XPath.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::SelectSingleNode(const System::String &xpath)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| xpath | const System::String\& | تعبير XPath. |

### ReturnValue

أول [Node](../../node/) يطابق استعلام XPath أو **null** إذا لم يتم العثور على أي Node مطابق.
## ملاحظات


في الوقت الحالي يتم دعم التعبيرات التي تحتوي على أسماء العناصر فقط. لا يتم دعم التعبيرات التي تستخدم أسماء السمات.

## انظر أيضًا

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
