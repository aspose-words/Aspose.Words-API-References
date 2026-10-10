---
title: "Aspose::Words::Lists::ListLevelAlignment enum"
linktitle: "ListLevelAlignment"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Lists::ListLevelAlignment enum. C++'de liste numarası veya madde işareti için hizalamayı belirtir."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.lists/listlevelalignment/
---
## ListLevelAlignment enum


Liste numarası veya madde işareti için hizalamayı belirtir.

```cpp
enum class ListLevelAlignment
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Sol | 0 | Liste etiketi, sayı konumunun soluna hizalanmıştır. |
| Orta | 1 | Liste etiketi, sayı konumunda ortalanmıştır. |
| Sağ | 2 | Bu liste etiketi, sayı konumunun sağına hizalanmıştır. |

## Açıklamalar


[Alignment](../listlevel/get_alignment/) özelliği için bir değer olarak kullanılır.

## Örnekler



[DocumentBuilder](../../aspose.words/documentbuilder/) kullanırken paragraflara özel liste biçimlendirmesinin nasıl uygulanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Bir liste, paragraf gruplarını ön ek sembolleri ve girintilerle düzenlememizi ve süslememizi sağlar.
// Girintiyi artırarak iç içe listeler oluşturabiliriz.
// Bir belge oluşturucunun "ListFormat" özelliğini kullanarak bir listeyi başlatabilir ve sonlandırabiliriz.
// Bir listenin başlangıcı ile sonu arasına eklediğimiz her paragraf, listenin bir öğesi haline gelir.
// Microsoft Word şablonundan bir liste oluşturun ve liste seviyelerinin ilk ikisini özelleştirin.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = list->get_ListLevels()->idx_get(0);
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Red());
listLevel->get_Font()->set_Size(24);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::OrdinalText);
listLevel->set_StartAt(21);
listLevel->set_NumberFormat(u"\x0000");

listLevel->set_NumberPosition(-36);
listLevel->set_TextPosition(144);
listLevel->set_TabPosition(144);

listLevel = list->get_ListLevels()->idx_get(1);
listLevel->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::Bullet);
listLevel->get_Font()->set_Name(u"Wingdings");
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Blue());
listLevel->get_Font()->set_Size(24);

// Bu NumberFormat değeri yıldız şeklinde madde işareti listesi sembolleri oluşturur.
listLevel->set_NumberFormat(u"\xf0af");
listLevel->set_TrailingCharacter(Aspose::Words::Lists::ListTrailingCharacter::Space);
listLevel->set_NumberPosition(144);

// Paragraflar oluşturun ve özel liste biçimlendirmemizin iki liste seviyesini onlara uygulayın.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->set_List(list);
builder->Writeln(u"The quick brown fox...");
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->ListIndent();
builder->Writeln(u"jumped over the lazy dog.");
builder->Writeln(u"jumped over the lazy dog.");

builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateCustomList.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
