---
title: "طريقة Aspose::Words::NodeCollection::Contains"
linktitle: "Contains"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::NodeCollection::Contains. تحدد ما إذا كانت العقدة موجودة في المجموعة في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/nodecollection/contains/
---
## NodeCollection::Contains method


يحدد ما إذا كانت العقدة موجودة في المجموعة.

```cpp
bool Aspose::Words::NodeCollection::Contains(const System::SharedPtr<Aspose::Words::Node> &node)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| node | const System::SharedPtr\<Aspose::Words::Node\>\& | العقدة التي سيتم تحديد موقعها. |

### ReturnValue

**true** if item is found in the collection; otherwise, **false**.
## ملاحظات


تنفّذ هذه الطريقة بحثًا خطيًا؛ وبالتالي، يكون متوسط زمن التنفيذ متناسبًا مع [Count](../get_count/).

## أمثلة



يعرض كيفية العمل مع [NodeCollection](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أضف نصًا إلى المستند عن طريق إدراج Run باستخدام DocumentBuilder.
builder->Write(u"Run 1. ");
builder->Write(u"Run 2. ");

// كل استدعاء لطريقة "Write" ينشئ Run جديد،
// ثم يظهر ذلك في مجموعة RunCollection للفقرة الأب.
System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();

ASSERT_EQ(2, runs->get_Count());

// يمكننا أيضًا إدراج عقدة في RunCollection يدويًا.
auto newRun = System::MakeObject<Aspose::Words::Run>(doc, u"Run 3. ");
runs->Insert(3, newRun);

ASSERT_TRUE(runs->Contains(newRun));
ASSERT_EQ(u"Run 1. Run 2. Run 3.", doc->GetText().Trim());

// الوصول إلى Run الفردية وإزالتها لإزالة نصها من المستند.
System::SharedPtr<Aspose::Words::Run> run = runs->idx_get(1);
runs->Remove(run);

ASSERT_EQ(u"Run 1. Run 3.", doc->GetText().Trim());
ASSERT_FALSE(System::TestTools::IsNull(run));
ASSERT_FALSE(runs->Contains(run));
```

## انظر أيضًا

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
