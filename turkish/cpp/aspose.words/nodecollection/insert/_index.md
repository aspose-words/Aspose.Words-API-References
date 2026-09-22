---
title: "Aspose::Words::NodeCollection::Insert yöntemi"
linktitle: "Insert"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::NodeCollection::Insert yöntemi. C++'da belirtilen indekste bir düğümü koleksiyona ekler."
type: docs
weight: 10000
url: /tr/cpp/aspose.words/nodecollection/insert/
---
## NodeCollection::Insert method


Belirtilen indeksde bir düğümü koleksiyona ekler.

```cpp
void Aspose::Words::NodeCollection::Insert(int32_t index, const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| index | int32_t | Düğümün sıfır tabanlı indeksi. Negatif indekslere izin verilir ve listenin sonundan erişimi gösterir. Örneğin -1 son düğüm, -2 sondan bir önceki ve böyle devam eder. |
| düğüm | const System::SharedPtr\<Aspose::Words::Node\>\& | Eklenecek düğüm. |
## Açıklamalar


Düğüm, koleksiyonun oluşturulduğu düğüm nesnesine alt öğe olarak eklenir.

Eğer indeks [Count](../get_count/) değerine eşit ya da daha büyükse, düğüm koleksiyonun sonuna eklenir.

Eğer indeks negatifse ve mutlak değeri [Count](../get_count/) değerinden büyükse, düğüm koleksiyonun sonuna eklenir.

Eğer eklenen düğüm başka bir belgeden oluşturulmuşsa, düğümü geçerli belgeye aktarmak için [ImportNode()](../) kullanmalısınız. İçe aktarılan düğüm daha sonra geçerli belgeye eklenebilir.

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
