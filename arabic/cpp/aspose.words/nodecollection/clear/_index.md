---
title: "Aspose::Words::NodeCollection::Clear طريقة"
linktitle: "Clear"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::NodeCollection::Clear طريقة. يزيل جميع العقد من هذه المجموعة ومن المستند في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/nodecollection/clear/
---
## NodeCollection::Clear method


يزيل جميع العقد من هذه المجموعة ومن المستند.

```cpp
void Aspose::Words::NodeCollection::Clear()
```


## أمثلة



يظهر كيفية إزالة جميع الأقسام من مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// هذا المستند يحتوي على قسم واحد مع بعض العقد الفرعية التي تحتوي وتعرض جميع محتويات المستند.
ASSERT_EQ(1, doc->get_Sections()->get_Count());
ASSERT_EQ(17, doc->get_Sections()->idx_get(0)->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
ASSERT_EQ(u"Hello World!\r\rHello Word!\r\r\rHello World!", doc->GetText().Trim());

// امسح مجموعة الأقسام، مما سيزيل جميع عناصر المستند الفرعية.
doc->get_Sections()->Clear();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
ASSERT_EQ(System::String::Empty, doc->GetText().Trim());
```

## انظر أيضًا

* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
