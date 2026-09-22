---
title: "Aspose::Words::Fields::FieldListNum::get_StartingNumber yöntemi"
linktitle: "get_StartingNumber"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldListNum::get_StartingNumber yöntemi. Bu alan için başlangıç değerini C++'ta alır veya ayarlar."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.fields/fieldlistnum/get_startingnumber/
---
## FieldListNum::get_StartingNumber method


Bu alan için başlangıç değerini alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldListNum::get_StartingNumber()
```


## Örnekler



LISTNUM alanlarıyla paragrafları numaralandırmanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// LISTNUM alanları, her LISTNUM alanında artan bir sayı gösterir.
// Bu alanların ayrıca numaralı listeleri taklit etmemizi sağlayan çeşitli seçenekleri vardır.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));

// Listeler varsayılan olarak 1'den saymaya başlar, ancak bu sayıyı 0 gibi farklı bir değere ayarlayabiliriz.
// Bu alan "0)" görüntüler.
field->set_StartingNumber(u"0");
builder->Writeln(u"Paragraph 1");

ASSERT_EQ(u" LISTNUM  \\s 0", field->GetFieldCode());

// LISTNUM alanları her liste seviyesi için ayrı sayımlar tutar.
// Başka bir LISTNUM alanı ile aynı paragrafta bir LISTNUM alanı eklemek
// sayım yerine liste seviyesini artırır.
// Sonraki alan, yukarıda başlattığımız sayımı devam ettirecek ve liste seviyesi 1'de "1" değerini gösterecektir.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);

// Bu alan, liste seviyesi 2'de bir sayım başlatacak. "1" değerini gösterecektir.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);

// Bu alan, liste seviyesi 3'de bir sayım başlatacak. "1" değerini gösterecektir.
// Farklı liste seviyelerinin farklı biçimlendirmeleri vardır,
// bu yüzden bu alanlar birleştirildiğinde "1)a)i)" değerini gösterir.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);
builder->Writeln(u"Paragraph 2");

// Eklediğimiz bir sonraki LISTNUM alanı, liste seviyesinde sayımı devam ettirecek
// önceki LISTNUM alanının bulunduğu seviyede.
// "ListLevel" özelliğini kullanarak farklı bir liste seviyesine atlayabiliriz.
// Bu LISTNUM alanı liste seviyesi 3'te kalırsa, "ii)" gösterirdi,
// ancak, onu liste seviyesi 2'ye taşıdığımız için, o seviyede sayımı sürdürür ve "b)" gösterir.
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_ListLevel(u"2");
builder->Writeln(u"Paragraph 3");

ASSERT_EQ(u" LISTNUM  \\l 2", field->GetFieldCode());

// Alanı farklı bir AUTONUM alan türünü taklit ettirmek için ListName özelliğini ayarlayabiliriz.
// "NumberDefault" AUTONUM'u, "OutlineDefault" AUTONUMOUT'u taklit eder,
// ve "LegalDefault" AUTONUMLGL alanlarını taklit eder.
// "OutlineDefault" liste adı, başlangıç numarası 1 olduğunda "I." görüntülenir.
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_StartingNumber(u"1");
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 4");

ASSERT_TRUE(field->get_HasListName());
ASSERT_EQ(u" LISTNUM  OutlineDefault \\s 1", field->GetFieldCode());

// ListName önceki alandan devralınmaz, bu yüzden her yeni alan için ayarlamamız gerekir.
// Bu alan, farklı liste adıyla sayımı devam ettirir ve "II." görüntüler.
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 5");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.LISTNUM.docx");
```

## Ayrıca Bakınız

* Class [FieldListNum](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
