---
title: "Aspose::Words::Fields::FieldShape::get_Text metodu"
linktitle: "get_Text"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldShape::get_Text metodu. C++'de alınacak metni alır veya ayarlar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/fieldshape/get_text/
---
## FieldShape::get_Text method


Alınacak metni alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldShape::get_Text()
```


## Örnekler



BIDIOUTLINE alanlarıyla sağdan sola dillerle uyumlu listelerin nasıl oluşturulacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// BIDIOUTLINE alanı, AUTONUM/LISTNUM alanları gibi paragraflara numara verir,
// ancak sadece sağdan sola düzenleme dili etkin olduğunda, örneğin İbranice veya Arapça, görünür.
// Aşağıdaki alan ".1" görüntüleyecek, bu "1." liste numarasının sağdan sola eşdeğeridir.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldBidiOutline>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true));
builder->Writeln(u"שלום");

ASSERT_EQ(u" BIDIOUTLINE ", field->GetFieldCode());

// İki tane daha BIDIOUTLINE alanı ekleyin, bunlar ".2" ve ".3" görüntüleyecek.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldBidiOutline, true);
builder->Writeln(u"שלום");

// Belgedeki her paragraf için yatay metin hizalamasını sağdan sola (RTL) olarak ayarlayın.
for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)))
{
    para->get_ParagraphFormat()->set_Bidi(true);
}

// Microsoft Word'de sağdan sola bir düzenleme dili etkinleştirirsek, alanlarımız sayıları gösterecek.
// Aksi takdirde "###" görüntüleyecekler.
doc->Save(get_ArtifactsDir() + u"Field.BIDIOUTLINE.docx");
```


SHAPE ve EMBED gibi bazı eski Microsoft Word alanlarının yükleme sırasında nasıl işlendiğini gösterir.
```cpp
// Microsoft Word 2003'te oluşturulmuş bir belgeyi açın.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Legacy fields.doc");

// Word belgesini açıp Alt+F9 tuşlarına basarsak, bir SHAPE ve bir EMBED alanı göreceğiz.
// Bir SHAPE alanı, "In line with text" sarma stilinin etkin olduğu bir AutoShape nesnesi için çapa/tuval görevi görür.
// Bir EMBED alanı aynı işlevi görür, ancak gömülü bir nesne için,
// örneğin harici bir Excel belgesinden bir elektronik tablo.
// Ancak, bu alanlar belgenin Fields koleksiyonunda görünmez.
ASSERT_EQ(0, doc->get_Range()->get_Fields()->get_Count());

// Bu alanlar yalnızca eski Microsoft Word sürümlerinde desteklenir.
// Belge yükleme süreci bu alanları Shape nesnelerine dönüştürecek,
// ki bunlara belgenin düğüm koleksiyonunda erişebiliriz.
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);
ASSERT_EQ(3, shapes->get_Count());

// İlk Shape düğümü, giriş belgesindeki SHAPE alanına karşılık gelir,
// bu da AutoShape için satır içi tuvaldir.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(0));
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Image, shape->get_ShapeType());

// İkinci Shape düğümü, AutoShape'in kendisidir.
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(1));
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Can, shape->get_ShapeType());

// Üçüncü Shape, harici elektronik tabloyu içeren EMBED alanıydı.
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(shapes->idx_get(2));
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::OleObject, shape->get_ShapeType());
```

## Ayrıca Bakınız

* Class [FieldShape](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
