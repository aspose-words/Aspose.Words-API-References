---
title: "Aspose::Words::Body::EnsureMinimum yöntemi"
linktitle: "EnsureMinimum"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Body::EnsureMinimum yöntemi. Son çocuk bir paragraf değilse, C++'ta bir boş paragraf oluşturur ve ekler."
type: docs
weight: 4000
url: /tr/cpp/aspose.words/body/ensureminimum/
---
## Body::EnsureMinimum method


Son çocuk bir paragraf değilse, boş bir paragraf oluşturur ve ekler.

```cpp
void Aspose::Words::Body::EnsureMinimum()
```


## Örnekler



Belgedeki tüm bölümlerden ana metni temizler, bölümleri olduğu gibi bırakır.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Boş bir belge bir bölüm, bir gövde ve bir paragraf içerir.
// "RemoveAllChildren" yöntemini çağırarak bu düğümlerin tümünü kaldırın,
// ve hiçbir çocuğu olmayan bir belge düğümü elde edin.
doc->RemoveAllChildren();

// Bu belge artık içerik ekleyebileceğimiz birleşik alt düğümlere sahip değil.
// Eğer düzenlemek istersek, düğüm koleksiyonunu yeniden doldurmamız gerekecek.
// İlk olarak yeni bir bölüm oluşturun ve ardından kök belge düğümüne çocuk olarak ekleyin.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Bir bölüm bir gövdeye ihtiyaç duyar, bu gövde tüm içeriğini barındırır ve gösterir
// sayfada bölümün başlığı ile altbilgisi arasındaki alanda.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Bu gövde henüz çocuğu yok, bu yüzden ona run ekleyemiyoruz.
ASSERT_EQ(0, doc->get_FirstSection()->get_Body()->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Bu gövdenin en az bir boş paragraf içerdiğinden emin olmak için "EnsureMinimum" metodunu çağırın.
body->EnsureMinimum();

// Şimdi, gövdeye run ekleyebilir ve belgenin bunları göstermesini sağlayabiliriz.
body->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [Body](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
