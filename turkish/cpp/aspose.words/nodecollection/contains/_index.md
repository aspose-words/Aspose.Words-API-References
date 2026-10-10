---
title: "Aspose::Words::NodeCollection::Contains yöntemi"
linktitle: "Contains"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::NodeCollection::Contains yöntemi. C++'ta bir düğümün koleksiyonda olup olmadığını belirler."
type: docs
weight: 4000
url: /tr/cpp/aspose.words/nodecollection/contains/
---
## NodeCollection::Contains method


Bir düğümün koleksiyonda olup olmadığını belirler.

```cpp
bool Aspose::Words::NodeCollection::Contains(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| düğüm | const System::SharedPtr\<Aspose::Words::Node\>\& | Bulunacak düğüm. |

### ReturnValue

**true** if item is found in the collection; otherwise, **false**.
## Açıklamalar


Bu yöntem lineer arama yapar; bu nedenle ortalama yürütme süresi [Count](../get_count/) ile orantılıdır.

## Örnekler



Bir [NodeCollection](../) ile nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir DocumentBuilder kullanarak Runs ekleyerek belgeye metin ekleyin.
builder->Write(u"Run 1. ");
builder->Write(u"Run 2. ");

// Her "Write" yöntemi çağrısı yeni bir Run oluşturur,
// bu da daha sonra üst Paragraph'ın RunCollection'ında görünür.
System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();

ASSERT_EQ(2, runs->get_Count());

// RunCollection'a bir düğümü manuel olarak da ekleyebiliriz.
auto newRun = System::MakeObject<Aspose::Words::Run>(doc, u"Run 3. ");
runs->Insert(3, newRun);

ASSERT_TRUE(runs->Contains(newRun));
ASSERT_EQ(u"Run 1. Run 2. Run 3.", doc->GetText().Trim());

// Bireysel run'lara erişin ve belge içindeki metinlerini kaldırmak için onları silin.
System::SharedPtr<Aspose::Words::Run> run = runs->idx_get(1);
runs->Remove(run);

ASSERT_EQ(u"Run 1. Run 3.", doc->GetText().Trim());
ASSERT_FALSE(System::TestTools::IsNull(run));
ASSERT_FALSE(runs->Contains(run));
```

## Ayrıca Bakınız

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
