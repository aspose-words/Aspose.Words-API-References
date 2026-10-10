---
title: "Aspose::Words::SaveFormat enum"
linktitle: "SaveFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::SaveFormat enum. Belgenin C++'da kaydedildiği formatı gösterir."
type: docs
weight: 114000
url: /tr/cpp/aspose.words/saveformat/
---
## SaveFormat enum


Belgenin kaydedildiği formatı gösterir.

```cpp
enum class SaveFormat
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Bilinmiyor | 0 | Varsayılan, dosya formatı için geçersiz değer. |
| Doc | 10 | Belgeyi Microsoft Word 97 - 2007 [Document](../document/) formatında kaydeder. |
| Dot | 11 | Belgeyi Microsoft Word 97 - 2007 Şablon formatında kaydeder. |
| Docx | 20 | Belgeyi Office Open XML WordprocessingML [Document](../document/) (makro içermeyen) olarak kaydeder. |
| Docm | 21 | Belgeyi Office Open XML WordprocessingML Makro Etkinleştirilmiş [Document](../document/) olarak kaydeder. |
| Dotx | 22 | Belgeyi Office Open XML WordprocessingML Şablonu (makro içermeyen) olarak kaydeder. |
| Dotm | 23 | Belgeyi Office Open XML WordprocessingML Makro Etkinleştirilmiş Şablon olarak kaydeder. |
| FlatOpc | 24 | Belgeyi ZIP paketi yerine düz bir XML dosyasında depolanan Office Open XML WordprocessingML olarak kaydeder. |
| FlatOpcMacroEnabled | 25 | Belgeyi ZIP paketi yerine düz bir XML dosyasında depolanan Office Open XML WordprocessingML Makro Etkinleştirilmiş [Document](../document/) olarak kaydeder. |
| FlatOpcTemplate | 26 | Belgeyi ZIP paketi yerine düz bir XML dosyasında depolanan Office Open XML WordprocessingML Şablonu (makro içermeyen) olarak kaydeder. |
| FlatOpcTemplateMacroEnabled | 27 | Belgeyi ZIP paketi yerine düz bir XML dosyasında depolanan Office Open XML WordprocessingML Makro Etkinleştirilmiş Şablon olarak kaydeder. |
| Rtf | 30 | Belgeyi RTF formatında kaydeder. 7 bitten büyük tüm karakterler onaltılık veya Unicode karakterleri olarak kaçış yapılır. |
| WordML | 31 | Belgeyi Microsoft Word 2003 WordprocessingML formatında kaydeder. |
| Pdf | 40 | Belgeyi PDF (Adobe Portable [Document](../document/)) formatında kaydeder. |
| Xps | 41 | Belgeyi XPS (XML Paper Specification) formatında kaydeder. |
| XamlFixed | 42 | Belgeyi Extensible Application [Markup](../../aspose.words.markup/) Language (XAML) formatında sabit belge olarak kaydeder. |
| Svg | 44 | Belgeyi Svg (Scalable Vector Graphics) formatında kaydeder. |
| HtmlFixed | 45 | Belgeyi mutlak konumlandırılmış öğeler kullanarak HTML formatında kaydeder. |
| OpenXps | 46 | Belgeyi OpenXPS (Ecma-388) formatında kaydeder. |
| Ps | 47 | Belgeyi PS (PostScript) formatında kaydeder. |
| Pcl | 48 | Belgeyi PCL (Printer Control Language) formatında kaydeder. |
| Html | 50 | Belgeyi HTML formatında kaydeder. |
| Mhtml | 51 | Belgeyi MHTML (Web archive) formatında kaydeder. |
| Epub | 52 | Belgeyi EPUB formatında kaydeder. |
| Azw3 | 53 | Belgeyi AZW3 formatında kaydeder. |
| Mobi | 54 | Belgeyi MOBI formatında kaydeder. |
| Odt | 60 | Belgeyi ODF Text [Document](../document/) olarak kaydeder. |
| Ott | 61 | Belgeyi ODF Text [Document](../document/) Şablonu olarak kaydeder. |
| Metin | 70 | Belgeyi düz metin formatında kaydeder. |
| XamlFlow | 71 | **Beta.** Belgeyi Extensible Application [Markup](../../aspose.words.markup/) Language (XAML) formatında akış belgesi olarak kaydeder. |
| XamlFlowPack | 72 | **Beta.** Belgeyi Extensible Application [Markup](../../aspose.words.markup/) Language (XAML) paket formatında akış belgesi olarak kaydeder. |
| Markdown | 73 | Belgeyi Markdown formatında kaydeder. |
| Xlsx | 80 | Belgeyi Office Open XML SpreadsheetML [Document](../document/) (makro içermeyen) olarak kaydeder. |
| Docling | 81 | Belgeyi Docling JSON formatında kaydeder. |
| Tiff | 100 | Belgenin bir veya birden fazla sayfasını render eder ve bunları tekli veya çok sayfalı bir TIFF dosyasına kaydeder. |
| Png | 101 | Belgenin bir sayfasını render eder ve PNG dosyası olarak kaydeder. |
| Bmp | 102 | Belgenin bir sayfasını render eder ve BMP dosyası olarak kaydeder. |
| Emf | 103 | Belgenin bir sayfasını render eder ve vektör EMF (Enhanced Meta File) dosyası olarak kaydeder. |
| Jpeg | 104 | Belgenin bir sayfasını render eder ve JPEG dosyası olarak kaydeder. |
| Gif | 105 | Belgenin bir sayfasını render eder ve GIF dosyası olarak kaydeder. |
| Eps | 106 | Belgenin bir sayfasını render eder ve EPS dosyası olarak kaydeder. |


## Örnekler



DOCX'ten HTML formatına nasıl dönüştürüleceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToHtml.html", Aspose::Words::SaveFormat::Html);
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
