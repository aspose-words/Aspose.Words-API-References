---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins yöntemi"
linktitle: "get_ExportPageMargins"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins yöntemi. Sayfa kenar boşluklarının HTML, MHTML veya EPUB'a aktarılıp aktarılmayacağını belirtir. Varsayılan değer C++'ta false'tur."
type: docs
weight: 23000
url: /tr/cpp/aspose.words.saving/htmlsaveoptions/get_exportpagemargins/
---
## HtmlSaveOptions::get_ExportPageMargins method


Sayfa kenar boşluklarının HTML, MHTML veya EPUB'a dışa aktarılıp aktarılmayacağını belirtir. Varsayılan değer **false**'tur.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins() const
```


## Örnekler



Çıktı HTML belgelerinde sınırların dışındaki nesnelerin nasıl gösterileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Kaydırma olmayan bir şekil eklemek için bir oluşturucu kullanın.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 200, 200);

shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Negatif şekil konum değerleri, şekli sayfa sınırlarının dışına yerleştirebilir.
// Bunu HTML'ye dışa aktarırsak, şekil kesilmiş görünecektir.
shape->set_Left(-150);

// Belgeyi HTML olarak kaydederken bir SaveOptions nesnesi geçebiliriz
// sınırların dışındaki nesnelerin tam olarak görüntülenmesi için sayfanın ayarlanıp ayarlanmayacağını belirlemek.
// Eğer "ExportPageMargins" bayrağını "true" olarak ayarlarsak, şekil çıktı HTML'sinde tamamen görünür olacaktır.
// Eğer "ExportPageMargins" bayrağını "false" olarak ayarlarsak,
// belgemiz şekli Microsoft Word'de gördüğümüz gibi kesilmiş olarak gösterecektir.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportPageMargins(exportPageMargins);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageMargins.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageMargins.html");

if (exportPageMargins)
{
    ASSERT_TRUE(outDocContents.Contains(u"<style type=\"text/css\">div.Section_1 { margin:70.85pt }</style>"));
    ASSERT_TRUE(outDocContents.Contains(u"<div class=\"Section_1\"><p style=\"margin-top:0pt; margin-left:150pt; margin-bottom:0pt\">"));
}
else
{
    ASSERT_FALSE(outDocContents.Contains(u"style type=\"text/css\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<div><p style=\"margin-top:0pt; margin-left:220.85pt; margin-bottom:0pt\">"));
}
```

## Ayrıca Bakınız

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
