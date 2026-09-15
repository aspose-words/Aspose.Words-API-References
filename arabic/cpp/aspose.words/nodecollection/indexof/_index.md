---
title: "طريقة Aspose::Words::NodeCollection::IndexOf"
linktitle: "IndexOf"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::NodeCollection::IndexOf. تُرجع الفهرس الصفري للعقدة المحددة في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words/nodecollection/indexof/
---
## NodeCollection::IndexOf method


يعيد الفهرس الصفري للعقدة المحددة.

```cpp
int32_t Aspose::Words::NodeCollection::IndexOf(const System::SharedPtr<Aspose::Words::Node> &node)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| node | const System::SharedPtr\<Aspose::Words::Node\>\& | العقدة التي سيتم تحديد موقعها. |

### ReturnValue

الفهرس الصفري للعقدة داخل المجموعة، إذا وُجد؛ وإلا -1.
## ملاحظات


تنفّذ هذه الطريقة بحثًا خطيًا؛ وبالتالي، يكون متوسط زمن التنفيذ متناسبًا مع [Count](../get_count/).

## أمثلة



يظهر كيفية الحصول على فهرس عقدة في مجموعة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::NodeCollection> allTables = doc->GetChildNodes(Aspose::Words::NodeType::Table, true);

ASSERT_EQ(0, allTables->IndexOf(table));

System::SharedPtr<Aspose::Words::Tables::Row> row = table->get_Rows()->idx_get(2);

ASSERT_EQ(2, table->IndexOf(row));

System::SharedPtr<Aspose::Words::Tables::Cell> cell = row->get_LastCell();

ASSERT_EQ(4, row->IndexOf(cell));
```

## انظر أيضًا

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
