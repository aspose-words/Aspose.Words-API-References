---
title: "Aspose::Words::LoadFormat enum"
linktitle: "LoadFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::LoadFormat enum. Yüklenecek belgenin formatını C++'da gösterir."
type: docs
weight: 97000
url: /tr/cpp/aspose.words/loadformat/
---
## LoadFormat enum


Yüklenecek belgenin biçimini gösterir.

```cpp
enum class LoadFormat
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Otomatik | 0 | Aspose.Words'ün formatı otomatik olarak tanımasını sağlar. |
| MsWorks | 8 | Microsoft Works 8 [Belge](../document/). |
| Doc | 10 | Microsoft Word 95 veya Word 97 - 2003 [Belge](../document/). |
| Dot | 11 | Microsoft Word 95 veya Word 97 - 2003 Şablonu. |
| DocPreWord60 | 12 | Belge pre-Word 95 formatında. Aspose.Words şu anda bu tür belgeleri yüklemeyi desteklememektedir. |
| Docx | 20 | Office Open XML WordprocessingML [Belge](../document/) (makro içermeyen). |
| Docm | 21 | Office Open XML WordprocessingML Makro Etkin [Belge](../document/). |
| Dotx | 22 | Office Open XML WordprocessingML Şablonu (makro içermeyen). |
| Dotm | 23 | Office Open XML WordprocessingML Makro Etkin Şablon. |
| FlatOpc | 24 | Office Open XML WordprocessingML, ZIP paketi yerine düz bir XML dosyasında depolanır. |
| FlatOpcMacroEnabled | 25 | Office Open XML WordprocessingML Makro Etkin [Belge](../document/) ZIP paketi yerine düz bir XML dosyasında depolanır. |
| FlatOpcTemplate | 26 | Office Open XML WordprocessingML Şablonu (makro içermeyen) ZIP paketi yerine düz bir XML dosyasında depolanır. |
| FlatOpcTemplateMacroEnabled | 27 | Office Open XML WordprocessingML Makro Etkin Şablon, ZIP paketi yerine düz bir XML dosyasında depolanır. |
| Rtf | 30 | RTF formatı. |
| WordML | 31 | Microsoft Word 2003 WordprocessingML formatı. |
| Html | 50 | HTML formatı. |
| Mhtml | 51 | MHTML (Web arşivi) formatı. |
| Mobi | 52 | MOBI formatı. MobiPocket okuyucu ve Amazon Kindle okuyucular tarafından kullanılır. |
| Chm | 53 | CHM (Derlenmiş HTML Yardım) formatı. |
| Azw3 | 54 | AZW3 formatı. Amazon Kindle okuyucular tarafından kullanılır. |
| Epub | 55 | EPUB formatı. |
| Odt | 60 | ODF Metni [Belge](../document/). |
| Ott | 61 | ODF Metni [Belge](../document/) Şablonu. |
| Metin | 62 | Düz Metin. |
| Markdown | 63 | Markdown metin belgesi. |
| Xml | 65 | XML belgesi. |
| Unknown | 255 | Tanımsız format, [Aspose.Words](../) tarafından yüklenemiyor. |


## Örnekler



Bir belgenin formatını tespit etmek için [FileFormatUtil](../fileformatutil/) yöntemlerinin nasıl kullanılacağını gösterir.
```cpp
// Dosya uzantısı eksik bir dosyadan belge yükleyin ve ardından dosya formatını tespit edin.
{
    System::SharedPtr<System::IO::FileStream> docStream = System::IO::File::OpenRead(get_MyDir() + u"Word document with missing file extension");
    System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(docStream);
    Aspose::Words::LoadFormat loadFormat = info->get_LoadFormat();

    ASSERT_EQ(Aspose::Words::LoadFormat::Doc, loadFormat);

    // Aşağıda bir LoadFormat'u ilgili SaveFormat'a dönüştürmenin iki yöntemi verilmiştir.
    // 1 -  LoadFormat için dosya uzantısı dizesini alın, ardından bu dizeden ilgili SaveFormat'ı elde edin:
    System::String fileExtension = Aspose::Words::FileFormatUtil::LoadFormatToExtension(loadFormat);
    Aspose::Words::SaveFormat saveFormat = Aspose::Words::FileFormatUtil::ExtensionToSaveFormat(fileExtension);

    // 2 -  LoadFormat'u doğrudan SaveFormat'ına dönüştürün:
    saveFormat = Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat(loadFormat);

    // Akıştan bir belge yükleyin ve ardından otomatik tespit edilen dosya uzantısına kaydedin.
    auto doc = System::MakeObject<Aspose::Words::Document>(docStream);

    ASSERT_EQ(u".doc", Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));

    doc->Save(get_ArtifactsDir() + u"File.SaveToDetectedFileFormat" + Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));
}
```


Bir html belgesi açılırken temel URI'nin nasıl belirtileceğini gösterir.
```cpp
// .html belgesi içinde göreli bir URI ile bağlanmış bir resmi yüklemek istediğimizi varsayalım
// Resim farklı bir konumda iken. Bu durumda, göreli URI'yi mutlak bir URI'ye dönüştürmemiz gerekir.
// Bir HtmlLoadOptions nesnesi kullanarak temel URI sağlayabiliriz.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(Aspose::Words::LoadFormat::Html, u"", get_ImageDir());

ASSERT_EQ(Aspose::Words::LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing image.html", loadOptions);

// Giriş .html dosyasındaki resim bozuk olsa da, özel temel URI'muz bağlantıyı onarmamıza yardımcı oldu.
auto imageShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// Bu çıktı belgesi eksik olan resmi gösterecek.
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BaseUri.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
