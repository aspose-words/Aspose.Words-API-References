---
title: "Aspose::Words::Fields::FieldHyperlink::get_OpenInNewWindow yöntemi."
linktitle: "get_OpenInNewWindow"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldHyperlink::get_OpenInNewWindow yöntemi. Hedef siteyi C++'ta yeni bir web tarayıcı penceresinde açıp açmayacağını alır veya ayarlar."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.fields/fieldhyperlink/get_openinnewwindow/
---
## FieldHyperlink::get_OpenInNewWindow method


Hedef siteyi yeni bir web tarayıcı penceresinde açıp açmayacağını alır veya ayarlar.

```cpp
bool Aspose::Words::Fields::FieldHyperlink::get_OpenInNewWindow()
```


## Örnekler



Yerel dosya sistemindeki belgelere bağlamak için HYPERLINK alanlarının nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldHyperlink, true));

// Microsoft Word'de bu HYPERLINK alanına tıkladığımızda,
// bağlantılı belge açılacak ve ardından imleç belirtilen yer işaretine yerleştirilecektir.
field->set_Address(get_MyDir() + u"Bookmarks.docx");
field->set_SubAddress(u"MyBookmark3");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address() + u" on bookmark " + field->get_SubAddress() + u" in a new window");

builder->Writeln();

// Microsoft Word'de bu HYPERLINK alanına tıkladığımızda,
// bağlantılı belge açılacak ve otomatik olarak belirtilen iframe'e kaydırılacaktır.
field = System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldHyperlink, true));
field->set_Address(get_MyDir() + u"Iframes.html");
field->set_ScreenTip(System::String(u"Open ") + field->get_Address());
field->set_Target(u"iframe_3");
field->set_OpenInNewWindow(true);
field->set_IsImageMap(false);

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.HYPERLINK.docx");
```

## Ayrıca Bakınız

* Class [FieldHyperlink](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
