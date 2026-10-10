---
title: "Aspose::Words::Drawing::OleFormat::Save yöntemi"
linktitle: "Save"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::OleFormat::Save yöntemi. Gömülü nesnenin verilerini C++'ta belirtilen akışa kaydeder."
type: docs
weight: 19000
url: /tr/cpp/aspose.words.drawing/oleformat/save/
---
## OleFormat::Save(const System::SharedPtr\<System::IO::Stream\>\&) method


Gömülü nesnenin verilerini belirtilen akışa kaydeder.

```cpp
void Aspose::Words::Drawing::OleFormat::Save(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| akış | const System::SharedPtr\<System::IO::Stream\>\& | Nesne verileri nerede kaydedilir. |
## Açıklamalar


Akışı serbest bırakmak çağıranın sorumluluğundadır.

## Örnekler



Gömülü OLE nesnelerinin dosyalara nasıl çıkarılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE spreadsheet.docm");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

// İlk şekildeki OLE nesnesi bir Microsoft Excel elektronik tablosudur.
System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shape->get_OleFormat();

ASSERT_EQ(u"Excel.Sheet.12", oleFormat->get_ProgId());

// Nesnemiz ne otomatik güncelleniyor ne de güncellemelerden kilitli.
ASSERT_FALSE(oleFormat->get_AutoUpdate());
ASPOSE_ASSERT_EQ(false, oleFormat->get_IsLocked());

// OLE nesnesini yerel dosya sisteminde bir dosyaya kaydetmeyi planlıyorsak,
// dosyaya uygulanacak dosya uzantısını belirlemek için "SuggestedExtension" özelliğini kullanabiliriz.
ASSERT_EQ(u".xlsx", oleFormat->get_SuggestedExtension());

// Aşağıda, OLE nesnesini yerel dosya sisteminde bir dosyaya kaydetmenin iki yolu verilmiştir.
// 1 -  Akış üzerinden kaydedin:
{
    auto fs = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"OLE spreadsheet extracted via stream" + oleFormat->get_SuggestedExtension(), System::IO::FileMode::Create);
    oleFormat->Save(fs);
}

// 2 -  Doğrudan bir dosya adına kaydedin:
oleFormat->Save(get_ArtifactsDir() + u"OLE spreadsheet saved directly" + oleFormat->get_SuggestedExtension());
```

## Ayrıca Bakınız

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## OleFormat::Save(const System::String\&) method


Gömülü nesnenin verilerini belirtilen adla bir dosyaya kaydeder.

```cpp
void Aspose::Words::Drawing::OleFormat::Save(const System::String &fileName)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | const System::String\& | OLE nesnesi verilerini kaydetmek için dosya adı. |

## Örnekler



Gömülü OLE nesnelerinin dosyalara nasıl çıkarılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE spreadsheet.docm");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

// İlk şekildeki OLE nesnesi bir Microsoft Excel elektronik tablosudur.
System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shape->get_OleFormat();

ASSERT_EQ(u"Excel.Sheet.12", oleFormat->get_ProgId());

// Nesnemiz ne otomatik güncelleniyor ne de güncellemelerden kilitli.
ASSERT_FALSE(oleFormat->get_AutoUpdate());
ASPOSE_ASSERT_EQ(false, oleFormat->get_IsLocked());

// OLE nesnesini yerel dosya sisteminde bir dosyaya kaydetmeyi planlıyorsak,
// dosyaya uygulanacak dosya uzantısını belirlemek için "SuggestedExtension" özelliğini kullanabiliriz.
ASSERT_EQ(u".xlsx", oleFormat->get_SuggestedExtension());

// Aşağıda, OLE nesnesini yerel dosya sisteminde bir dosyaya kaydetmenin iki yolu verilmiştir.
// 1 -  Akış üzerinden kaydedin:
{
    auto fs = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"OLE spreadsheet extracted via stream" + oleFormat->get_SuggestedExtension(), System::IO::FileMode::Create);
    oleFormat->Save(fs);
}

// 2 -  Doğrudan bir dosya adına kaydedin:
oleFormat->Save(get_ArtifactsDir() + u"OLE spreadsheet saved directly" + oleFormat->get_SuggestedExtension());
```

## Ayrıca Bakınız

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## OleFormat::Save(std::basic_ostream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Drawing::OleFormat::Save(std::basic_ostream<CharType, Traits> &stream)
```

## Ayrıca Bakınız

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
