---
title: "Aspose::Words::DocumentBuilder::InsertOleObject method"
linktitle: "InsertOleObject"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::InsertOleObject yöntemi. Bir akıştan belgeye gömülü bir OLE nesnesi ekler (C++)."
type: docs
weight: 41000
url: /tr/cpp/aspose.words/documentbuilder/insertoleobject/
---
## DocumentBuilder::InsertOleObject(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


Bir akıştan gömülü bir OLE nesnesi belgeye ekler.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::SharedPtr<System::IO::Stream> &stream, const System::String &progId, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| akış | const System::SharedPtr\<System::IO::Stream\>\& | Uygulama verilerini içeren akış. |
| progId | const System::String\& | OLE nesnesinin programatik tanımlayıcısı. |
| asIcon | bool | Eklenecek OLE nesnesinin İkonik veya Normal modunu belirtir. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | OLE nesnesinin görüntü sunumu. Değer **null** ise Aspose.Words önceden tanımlı görüntülerden birini kullanır. |

### ReturnValue

Ole nesnesini içeren şekil düğümü ve geçerli Builder konumuna eklenir.

## Örnekler



Bir belgeye OLE nesneleri gömmek için document builder'ın nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Yerel dosya sisteminden bir Microsoft Excel çalışma sayfası ekle
// belgenin içine, varsayılan görünümünü koruyarak.
{
    System::SharedPtr<System::IO::Stream> spreadsheetStream = System::IO::File::Open(get_MyDir() + u"Spreadsheet.xlsx", System::IO::FileMode::Open);
    builder->Writeln(u"Spreadsheet Ole object:");
    // 'presentation' atlanır ve 'asIcon' ayarlanırsa, bu aşırı yüklenmiş yöntem seçer
    // simgeyi 'progId'ye göre ve önceden tanımlı simge başlığını kullanır.
    builder->InsertOleObject(spreadsheetStream, u"OleObject.xlsx", false, nullptr);
}

// Bir Microsoft Powerpoint sunumunu OLE nesnesi olarak ekle.
// Bu sefer, simge için web'den indirilen bir görüntüsü olacak.
{
    System::SharedPtr<System::IO::Stream> powerpointStream = System::IO::File::Open(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    System::ArrayPtr<uint8_t> imgBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");

    {
        auto imageStream = System::MakeObject<System::IO::MemoryStream>(imgBytes);
        builder->InsertParagraph();
        builder->Writeln(u"Powerpoint Ole object:");
        builder->InsertOleObject(powerpointStream, u"OleObject.pptx", true, imageStream);
    }
}

// Bu nesnelere Microsoft Word'de çift tıklayarak açın
// bağlantılı dosyaları ilgili uygulamalarıyla açın.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjects.docx");
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


Bir dosyadan gömülü veya bağlı bir OLE nesnesi belgeye ekler. OLE nesne tipini dosya uzantısı kullanarak algılar.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::String &fileName, bool isLinked, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | const System::String\& | Dosyanın tam yolu. |
| isLinked | bool | **true** ise, bağlı OLE nesnesi eklenir, aksi takdirde gömülü OLE nesnesi eklenir. |
| asIcon | bool | Eklenecek OLE nesnesinin İkonik veya Normal modunu belirtir. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | OLE nesnesinin görüntü sunumu. Değer **null** ise Aspose.Words önceden tanımlı görüntülerden birini kullanır. |

### ReturnValue

Ole nesnesini içeren şekil düğümü ve geçerli Builder konumuna eklenir.

## Örnekler



Bir OLE nesnesini belgeye nasıl ekleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// OLE nesneleri, yerel dosya sistemimizdeki dosyalara bağlantılardır ve diğer yüklü uygulamalar tarafından açılabilir.
// Bu şekillere çift tıklamak uygulamayı başlatır ve ardından bağlı nesneyi açmak için kullanır.
// Bu şekilleri eklemek ve görünümünü yapılandırmak için InsertOleObject yöntemini kullanmanın üç yolu vardır.
// 1 -  Yerel dosya sisteminden alınan görüntü:
{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    // 'presentation' atlanır ve 'asIcon' ayarlanırsa, bu aşırı yüklenmiş yöntem seçer
    // simgeyi dosya uzantısına göre ve dosya adını simge başlığı olarak kullanır.
    builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", false, false, imageStream);
}

// 'presentation' atlanır ve 'asIcon' ayarlanırsa, bu aşırı yüklenmiş yöntem seçer
// simgeyi 'progId'ye göre ve dosya adını simge başlığı olarak kullanır.
// 2 -  Nesneyi açacak uygulamaya dayalı simge:
builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", u"Excel.Sheet", false, true, nullptr);

// 'iconFile' ve 'iconCaption' atlanırsa, bu aşırı yüklenmiş yöntem seçer
// simgeyi 'progId'ye göre ve önceden tanımlı simge başlığını kullanır.
// 3 -  Yerel dosya sisteminden 32 x 32 piksel veya daha küçük bir görüntü simgesi, özel bir başlıkla:
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", false, get_ImageDir() + u"Logo icon.ico", u"Double click to view presentation!");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObject.docx");
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(const System::String\&, const System::String\&, bool, bool, const System::SharedPtr\<System::IO::Stream\>\&) method


Bir dosyadan gömülü veya bağlı bir OLE nesnesi belgeye ekler. OLE nesne tipini verilen progID parametresi kullanarak algılar.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(const System::String &fileName, const System::String &progId, bool isLinked, bool asIcon, const System::SharedPtr<System::IO::Stream> &presentation)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | const System::String\& | Dosyanın tam yolu. |
| progId | const System::String\& | OLE nesnesinin ProgId'si. |
| isLinked | bool | **true** ise, bağlı OLE nesnesi eklenir, aksi takdirde gömülü OLE nesnesi eklenir. |
| asIcon | bool | Eklenecek OLE nesnesinin İkonik veya Normal modunu belirtir. |
| presentation | const System::SharedPtr\<System::IO::Stream\>\& | OLE nesnesinin görüntü sunumu. Değer **null** ise Aspose.Words önceden tanımlı görüntülerden birini kullanır. |

### ReturnValue

Ole nesnesini içeren şekil düğümü ve geçerli Builder konumuna eklenir.

## Örnekler



Bir OLE nesnesini belgeye nasıl ekleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// OLE nesneleri, yerel dosya sistemimizdeki dosyalara bağlantılardır ve diğer yüklü uygulamalar tarafından açılabilir.
// Bu şekillere çift tıklamak uygulamayı başlatır ve ardından bağlı nesneyi açmak için kullanır.
// Bu şekilleri eklemek ve görünümünü yapılandırmak için InsertOleObject yöntemini kullanmanın üç yolu vardır.
// 1 -  Yerel dosya sisteminden alınan görüntü:
{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open);
    // 'presentation' atlanır ve 'asIcon' ayarlanırsa, bu aşırı yüklenmiş yöntem seçer
    // simgeyi dosya uzantısına göre ve dosya adını simge başlığı olarak kullanır.
    builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", false, false, imageStream);
}

// 'presentation' atlanır ve 'asIcon' ayarlanırsa, bu aşırı yüklenmiş yöntem seçer
// simgeyi 'progId'ye göre ve dosya adını simge başlığı olarak kullanır.
// 2 -  Nesneyi açacak uygulamaya dayalı simge:
builder->InsertOleObject(get_MyDir() + u"Spreadsheet.xlsx", u"Excel.Sheet", false, true, nullptr);

// 'iconFile' ve 'iconCaption' atlanırsa, bu aşırı yüklenmiş yöntem seçer
// simgeyi 'progId'ye göre ve önceden tanımlı simge başlığını kullanır.
// 3 -  Yerel dosya sisteminden 32 x 32 piksel veya daha küçük bir görüntü simgesi, özel bir başlıkla:
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", false, get_ImageDir() + u"Logo icon.ico", u"Double click to view presentation!");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObject.docx");
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(std::basic_istream\<CharType, Traits\>\&, System::String, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(std::basic_istream<CharType, Traits> &stream, System::String progId, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(System::String fileName, bool isLinked, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObject(System::String, System::String, bool, bool, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObject(System::String fileName, System::String progId, bool isLinked, bool asIcon, std::basic_istream<CharType, Traits> &presentation)
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
