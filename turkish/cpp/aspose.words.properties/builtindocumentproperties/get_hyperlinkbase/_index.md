---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase metodu"
linktitle: "get_HyperlinkBase"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase metodu. C++'da bu belgede göreli köprüleri değerlendirmek için kullanılan temel dizeyi belirtir."
type: docs
weight: 13000
url: /tr/cpp/aspose.words.properties/builtindocumentproperties/get_hyperlinkbase/
---
## BuiltInDocumentProperties::get_HyperlinkBase method


Bu belgede göreceli bağlantıların değerlendirilmesinde kullanılan temel dizeyi belirtir.

```cpp
System::String Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase()
```

## Açıklamalar


Aspose.Words bu özelliği kullanmaz.

## Örnekler



Bir köprünün temel bölümünün belge özelliklerinde nasıl saklanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Yerel dosya sisteminde "Document.docx" adlı bir belgeye göreli bir köprü ekleyin.
// Microsoft Word'de bağlantıya tıklamak, belge mevcutsa belirlenen belgeyi açar.
builder->InsertHyperlink(u"Relative hyperlink", u"Document.docx", false);

// Bu bağlantı görelidir. Aynı klasörde "Document.docx" yoksa
// bu bağlantıyı içeren belgeyle aynı klasörde "Document.docx" yoksa, bağlantı kırık olur.
ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"Document.docx"));
doc->Save(get_ArtifactsDir() + u"DocumentProperties.HyperlinkBase.BrokenLink.docx");

// Bağlantı vermeye çalıştığımız belge, kaydetmeyi planladığımız klasörden farklı bir dizinde bulunuyor.
// Bağlantıları, her birine mutlak bir dosya adı ekleyerek bu şekilde düzeltebiliriz.
// Alternatif olarak, göreli dosya adı içeren her köprünün önüne eklenecek bir temel bağlantı sağlayabiliriz
// bağlantıya tıkladığımızda linkine eklenecektir.
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();
properties->set_HyperlinkBase(get_MyDir());

ASSERT_TRUE(System::IO::File::Exists(properties->get_HyperlinkBase() + (System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(doc->get_Range()->get_Fields()->idx_get(0)))->get_Address()));

doc->Save(get_ArtifactsDir() + u"DocumentProperties.HyperlinkBase.WorkingLink.docx");
```

## Ayrıca Bakınız

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
