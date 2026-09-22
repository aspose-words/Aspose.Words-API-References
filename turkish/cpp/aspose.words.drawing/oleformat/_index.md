---
title: "Aspose::Words::Drawing::OleFormat sınıfı"
linktitle: "OleFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::OleFormat sınıfı. Bir OLE nesnesi veya ActiveX denetiminin verilerine erişim sağlar. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.drawing/oleformat/
---
## OleFormat class


Bir OLE nesnesi veya ActiveX denetiminin verilerine erişim sağlar. Daha fazla bilgi edinmek için [Working with Ole Objects](https://docs.aspose.com/words/cpp/working-with-ole-objects/) dokümantasyon makalesini ziyaret edin.

```cpp
class OleFormat : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_AutoUpdate](./get_autoupdate/)() | Microsoft Word'de OLE nesnesine olan bağlantının otomatik olarak güncellenip güncellenmeyeceğini belirtir. |
| [get_Clsid](./get_clsid/)() | OLE nesnesinin CLSID'sini alır. |
| [get_IconCaption](./get_iconcaption/)() | OLE nesnesinin simge başlığını alır. OLE nesnesinin bir simgesi yoksa veya başlık alınamıyorsa, boş bir dize döndürür. |
| [get_IsLink](./get_islink/)() | OLE nesnesi bağlıysa (**true**) döndürür ( [SourceFullName](./get_sourcefullname/) belirtildiğinde). |
| [get_IsLocked](./get_islocked/)() | OLE nesnesine olan bağlantının güncellemelerden kilitli olup olmadığını belirtir. |
| [get_OleControl](./get_olecontrol/)() | Bu OLE nesnesi bir ActiveX denetimi ise [OleControl](./get_olecontrol/) nesnelerini alır. Aksi takdirde bu özellik null'dur. |
| [get_OleIcon](./get_oleicon/)() | OLE nesnesinin çizim görünümünü alır. **true** olduğunda, OLE nesnesi bir simge olarak gösterilir. **false** olduğunda, OLE nesnesi içerik olarak gösterilir. |
| [get_OlePackage](./get_olepackage/)() | OLE nesnesi bir OLE Paketi ise [OlePackage](../olepackage/) erişimi sağlar. Aksi takdirde **null** döndürür. |
| [get_ProgId](./get_progid/)() | OLE nesnesinin ProgID'sini alır veya ayarlar. |
| [get_SourceFullName](./get_sourcefullname/)() | Bağlı OLE nesnesi için kaynak dosyanın yolunu ve adını alır veya ayarlar. |
| [get_SourceItem](./get_sourceitem/)() | Bağlantı yapılan kaynak dosyanın bölümünü tanımlamak için kullanılan dizeyi alır veya ayarlar. |
| [get_SuggestedExtension](./get_suggestedextension/)() | Mevcut gömülü nesne için bir dosyaya kaydetmek isterseniz önerilen dosya uzantısını alır. |
| [get_SuggestedFileName](./get_suggestedfilename/)() | Mevcut gömülü nesne için bir dosyaya kaydetmek isterseniz önerilen dosya adını alır. |
| [GetOleEntry](./getoleentry/)(const System::String\&) | OLE nesnesi veri girişini alır. |
| [GetRawData](./getrawdata/)() | OLE nesnesi ham verisini alır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | Gömülü nesnenin verilerini belirtilen akışa kaydeder. |
| [Save](./save/)(const System::String\&) | Gömülü nesnenin verilerini belirtilen adla bir dosyaya kaydeder. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_AutoUpdate](./set_autoupdate/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::OleFormat::get_AutoUpdate](./get_autoupdate/). |
| [set_IsLocked](./set_islocked/)(bool) | Ayarlayıcı [Aspose::Words::Drawing::OleFormat::get_IsLocked](./get_islocked/). |
| [set_ProgId](./set_progid/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Drawing::OleFormat::get_ProgId](./get_progid/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Drawing::OleFormat::get_SourceFullName](./get_sourcefullname/). |
| [set_SourceItem](./set_sourceitem/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Drawing::OleFormat::get_SourceItem](./get_sourceitem/). |
| static [Type](./type/)() |  |
## Açıklamalar


OLE nesnesinin verilerine erişmek için [OleFormat](../shape/get_oleformat/) özelliğini kullanın. [OleFormat](./) sınıfının örneklerini doğrudan oluşturmazsınız.

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
