---
title: "طريقة Aspose::Words::Document::AcceptAllRevisions"
linktitle: "AcceptAllRevisions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::AcceptAllRevisions. تقبل جميع التغييرات المتتبعة في المستند في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/document/acceptallrevisions/
---
## Document::AcceptAllRevisions method


يقبل جميع التغييرات المتتبعة في المستند.

```cpp
void Aspose::Words::Document::AcceptAllRevisions()
```


## أمثلة



يظهر كيفية قبول جميع التغييرات المتتبعة في المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// قم بتحرير المستند أثناء تتبع التغييرات لإنشاء بعض المراجعات.
doc->StartTrackRevisions(u"John Doe");
builder->Write(u"Hello world! ");
builder->Write(u"Hello again! ");
builder->Write(u"This is another revision.");
doc->StopTrackRevisions();

ASSERT_EQ(3, doc->get_Revisions()->get_Count());

// يمكننا التنقل عبر كل مراجعة وقبولها/رفضها كجزء من مستندنا.
// إذا كنا نعلم أننا نرغب في قبول كل مراجعة، يمكننا القيام بذلك بطريقة أكثر بساطة عن طريق استدعاء هذه الطريقة.
doc->AcceptAllRevisions();

ASSERT_EQ(0, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"Hello world! Hello again! This is another revision.", doc->GetText().Trim());
```

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
