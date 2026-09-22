---
title: "Aspose::Words::Drawing::OleFormat::get_SourceItem metodu"
linktitle: "get_SourceItem"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::OleFormat::get_SourceItem metodu. Bağlantı verilen kaynak dosyanın hangi bölümünü tanımlamak için kullanılan bir dizeyi alır veya ayarlar."
type: docs
weight: 12000
url: /tr/cpp/aspose.words.drawing/oleformat/get_sourceitem/
---
## OleFormat::get_SourceItem method


Bağlantı yapılan kaynak dosyanın bölümünü tanımlamak için kullanılan dizeyi alır veya ayarlar.

```cpp
System::String Aspose::Words::Drawing::OleFormat::get_SourceItem()
```

## Açıklamalar


Varsayılan değer boş bir dizedir.

Örneğin, kaynak dosya bir Microsoft Excel çalışma kitabı ise, [SourceItem](./) özelliği, OLE nesnesi çalışma sayfasından yalnızca birkaç hücre içeriyorsa "Workbook1!R3C1:R4C2" döndürebilir.

## Örnekler



Bağlantılı ve bağlantısız OLE nesnelerinin nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Microsoft Visio çizimini belgeye OLE nesnesi olarak göm.
builder->InsertOleObject(get_ImageDir() + u"Microsoft Visio drawing.vsd", u"Package", false, false, nullptr);

// Yerel dosya sistemindeki dosyaya bir bağlantı ekle ve bunu simge olarak göster.
builder->InsertOleObject(get_ImageDir() + u"Microsoft Visio drawing.vsd", u"Package", true, true, nullptr);

// OLE nesnelerinin eklenmesi, bu nesneleri depolayan şekiller oluşturur.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());
ASSERT_EQ(2, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_ShapeType() == Aspose::Words::Drawing::ShapeType::OleObject;
}))));

// Bir şekil bir OLE nesnesi içeriyorsa, geçerli bir "OleFormat" özelliğine sahip olacaktır,
// bu özelliği şeklin bazı yönlerini doğrulamak için kullanabiliriz.
System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shapes[0]->get_OleFormat();

ASPOSE_ASSERT_EQ(false, oleFormat->get_IsLink());
ASPOSE_ASSERT_EQ(false, oleFormat->get_OleIcon());

oleFormat = shapes[1]->get_OleFormat();

ASPOSE_ASSERT_EQ(true, oleFormat->get_IsLink());
ASPOSE_ASSERT_EQ(true, oleFormat->get_OleIcon());

ASSERT_TRUE(oleFormat->get_SourceFullName().EndsWith(System::String(u"Images") + System::IO::Path::DirectorySeparatorChar + u"Microsoft Visio drawing.vsd"));
ASSERT_EQ(u"", oleFormat->get_SourceItem());

ASSERT_EQ(u"Microsoft Visio drawing.vsd", oleFormat->get_IconCaption());

doc->Save(get_ArtifactsDir() + u"Shape.OleLinks.docx");

// Nesne OLE verisi içeriyorsa, ona bir akış kullanarak erişebiliriz.
{
    System::SharedPtr<System::IO::MemoryStream> stream = oleFormat->GetOleEntry(u"\x0001" u"CompObj");
    System::ArrayPtr<uint8_t> oleEntryBytes = stream->ToArray();
    ASSERT_EQ(76, oleEntryBytes->get_Length());
}
```

## Ayrıca Bakınız

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
