---
title: "Aspose::Words::Fields::FieldHyperlink::get_IsImageMap yöntemi"
linktitle: "get_IsImageMap"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldHyperlink::get_IsImageMap yöntemi. C++'de sunucu tarafı bir görüntü haritası için köprüye koordinat eklenip eklenmeyeceğini alır veya ayarlar."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.fields/fieldhyperlink/get_isimagemap/
---
## FieldHyperlink::get_IsImageMap method


Sunucu tarafı görüntü haritası için hiperlinke koordinat eklenip eklenmeyeceğini alır veya ayarlar.

```cpp
bool Aspose::Words::Fields::FieldHyperlink::get_IsImageMap()
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
