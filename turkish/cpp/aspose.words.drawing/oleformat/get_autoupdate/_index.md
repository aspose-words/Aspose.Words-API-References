---
title: "Aspose::Words::Drawing::OleFormat::get_AutoUpdate yöntemi"
linktitle: "get_AutoUpdate"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::OleFormat::get_AutoUpdate yöntemi. Microsoft Word içinde C++ ile OLE nesnesine olan bağlantının otomatik olarak güncellenip güncellenmeyeceğini belirtir."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.drawing/oleformat/get_autoupdate/
---
## OleFormat::get_AutoUpdate method


Microsoft Word'de OLE nesnesine olan bağlantının otomatik olarak güncellenip güncellenmeyeceğini belirtir.

```cpp
bool Aspose::Words::Drawing::OleFormat::get_AutoUpdate()
```

## Açıklamalar


Varsayılan değer **false**'tur.

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
