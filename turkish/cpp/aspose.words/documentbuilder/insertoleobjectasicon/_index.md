---
title: "Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon metodu"
linktitle: "InsertOleObjectAsIcon"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon metodu. Bir akıştan belgeye bir gömülü OLE nesnesini simge olarak ekler. Simge dosyası ve başlığı belirtmeye izin verir. C++'ta verilen progID parametresi kullanılarak OLE nesne türünü algılar."
type: docs
weight: 42000
url: /tr/cpp/aspose.words/documentbuilder/insertoleobjectasicon/
---
## DocumentBuilder::InsertOleObjectAsIcon(const System::SharedPtr\<System::IO::Stream\>\&, const System::String\&, const System::String\&, const System::String\&) method


Bir akıştan gömülü bir OLE nesnesini simge olarak belgeye ekler. Simge dosyasını ve başlığı belirtmeye izin verir. OLE nesne tipini verilen progID parametresi kullanarak algılar.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::SharedPtr<System::IO::Stream> &stream, const System::String &progId, const System::String &iconFile, const System::String &iconCaption)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| akış | const System::SharedPtr\<System::IO::Stream\>\& | Uygulama verilerini içeren akış. |
| progId | const System::String\& | OLE nesnesinin ProgId'si. |
| iconFile | const System::String\& | ICO dosyasının tam yolu. Değer **null** ise, Aspose.Words önceden tanımlı bir görüntüyü kullanacaktır. |
| iconCaption | const System::String\& | Simge başlığı. Değer **null** ise, Aspose.Words önceden tanımlı bir simge başlığı kullanacaktır. |

### ReturnValue

Ole nesnesini içeren şekil düğümü ve geçerli Builder konumuna eklenir.

## Örnekler



Bir gömülü veya bağlı OLE nesnesini belgeye simge olarak nasıl ekleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 'iconFile' ve 'iconCaption' atlanırsa, bu aşırı yüklenmiş yöntem seçer
// simgeyi 'progId'ye göre ve dosya adını simge başlığı olarak kullanır.
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", u"Package", false, get_ImageDir() + u"Logo icon.ico", u"My embedded file");

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    // 'iconFile' ve 'iconCaption' atlanırsa, bu aşırı yüklenmiş yöntem seçer
    // simgeyi dosya uzantısına göre ve dosya adını simge başlığı olarak kullanır.
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObjectAsIcon(stream, u"PowerPoint.Application", get_ImageDir() + u"Logo icon.ico", u"My embedded file stream");

    System::SharedPtr<Aspose::Words::Drawing::OlePackage> setOlePackage = shape->get_OleFormat()->get_OlePackage();
    setOlePackage->set_FileName(u"Presentation.pptx");
    setOlePackage->set_DisplayName(u"Presentation.pptx");
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjectAsIcon.docx");
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObjectAsIcon(const System::String\&, bool, const System::String\&, const System::String\&) method


Gömülü veya bağlı bir OLE nesnesini simge olarak belgeye ekler. Simge dosyasını ve başlığı belirtmeye izin verir. OLE nesne tipini dosya uzantısı kullanarak algılar.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::String &fileName, bool isLinked, const System::String &iconFile, const System::String &iconCaption)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | const System::String\& | Dosyanın tam yolu. |
| isLinked | bool | **true** ise, bağlı OLE nesnesi eklenir, aksi takdirde gömülü OLE nesnesi eklenir. |
| iconFile | const System::String\& | ICO dosyasının tam yolu. Değer **null** ise, Aspose.Words önceden tanımlı bir görüntüyü kullanacaktır. |
| iconCaption | const System::String\& | Simge başlığı. Değer **null** ise, Aspose.Words dosya adını kullanacaktır. |

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
## DocumentBuilder::InsertOleObjectAsIcon(const System::String\&, const System::String\&, bool, const System::String\&, const System::String\&) method


Gömülü veya bağlı bir OLE nesnesini simge olarak belgeye ekler. Simge dosyasını ve başlığı belirtmeye izin verir. OLE nesne tipini verilen progID parametresi kullanarak algılar.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(const System::String &fileName, const System::String &progId, bool isLinked, const System::String &iconFile, const System::String &iconCaption)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | const System::String\& | Dosyanın tam yolu. |
| progId | const System::String\& | OLE nesnesinin ProgId'si. |
| isLinked | bool | **true** ise, bağlı OLE nesnesi eklenir, aksi takdirde gömülü OLE nesnesi eklenir. |
| iconFile | const System::String\& | ICO dosyasının tam yolu. Değer **null** ise, Aspose.Words önceden tanımlı bir görüntüyü kullanacaktır. |
| iconCaption | const System::String\& | Simge başlığı. Değer **null** ise, Aspose.Words dosya adını kullanacaktır. |

### ReturnValue

Ole nesnesini içeren şekil düğümü ve geçerli Builder konumuna eklenir.

## Örnekler



Bir gömülü veya bağlı OLE nesnesini belgeye simge olarak nasıl ekleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 'iconFile' ve 'iconCaption' atlanırsa, bu aşırı yüklenmiş yöntem seçer
// simgeyi 'progId'ye göre ve dosya adını simge başlığı olarak kullanır.
builder->InsertOleObjectAsIcon(get_MyDir() + u"Presentation.pptx", u"Package", false, get_ImageDir() + u"Logo icon.ico", u"My embedded file");

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Presentation.pptx", System::IO::FileMode::Open);
    // 'iconFile' ve 'iconCaption' atlanırsa, bu aşırı yüklenmiş yöntem seçer
    // simgeyi dosya uzantısına göre ve dosya adını simge başlığı olarak kullanır.
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObjectAsIcon(stream, u"PowerPoint.Application", get_ImageDir() + u"Logo icon.ico", u"My embedded file stream");

    System::SharedPtr<Aspose::Words::Drawing::OlePackage> setOlePackage = shape->get_OleFormat()->get_OlePackage();
    setOlePackage->set_FileName(u"Presentation.pptx");
    setOlePackage->set_DisplayName(u"Presentation.pptx");
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOleObjectAsIcon.docx");
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOleObjectAsIcon(std::basic_istream\<CharType, Traits\>\&, System::String, System::String, System::String) method




```cpp
template<typename CharType,typename Traits> System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOleObjectAsIcon(std::basic_istream<CharType, Traits> &stream, System::String progId, System::String iconFile, System::String iconCaption)
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
