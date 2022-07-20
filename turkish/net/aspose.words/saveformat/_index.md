---
title: SaveFormat
second_title: Aspose.Words for .NET API Referansı
description: Belgenin kaydedildiği biçimi belirtir.
type: docs
weight: 4580
url: /tr/net/aspose.words/saveformat/
---
## SaveFormat enumeration

Belgenin kaydedildiği biçimi belirtir.

```csharp
public enum SaveFormat
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Unknown | `0` | Dosya biçimi için varsayılan, geçersiz değer. |
| Doc | `10` | Belgeyi Microsoft Word 97 - 2007 Belge biçiminde kaydeder. |
| Dot | `11` | Belgeyi Microsoft Word 97 - 2007 Şablon biçiminde kaydeder. |
| Docx | `20` | Belgeyi bir Office Açık XML Kelime İşlemeML Belgesi (makro içermeyen) olarak kaydeder. |
| Docm | `21` | Belgeyi bir Office Açık XML Kelime İşlemeML Makro-Etkin Belgesi olarak kaydeder. |
| Dotx | `22` | Belgeyi bir Office Açık XML Kelime İşlemeML Şablonu (makro içermeyen) olarak kaydeder. |
| Dotm | `23` | Belgeyi bir Office Açık XML Kelime İşlemeML Makro Etkin Şablonu olarak kaydeder. |
| FlatOpc | `24` | Belgeyi, ZIP paketi yerine düz bir XML dosyasında depolanan Office Açık XML Kelime İşlemeML'si olarak kaydeder. |
| FlatOpcMacroEnabled | `25` | Belgeyi, bir ZIP paketi yerine düz bir XML dosyasında saklanan Office Açık XML Kelime İşlemeML Makro-Etkin Belgesi olarak kaydeder. |
| FlatOpcTemplate | `26` | Belgeyi, ZIP paketi yerine düz bir XML dosyasında saklanan Office Açık XML Kelime İşlemeML Şablonu (makro içermeyen) olarak kaydeder. |
| FlatOpcTemplateMacroEnabled | `27` | Belgeyi, ZIP paketi yerine düz bir XML dosyasında saklanan Office Açık XML Kelime İşlemeML Makro Etkin Şablonu olarak kaydeder. |
| Rtf | `30` | Belgeyi RTF biçiminde kaydeder. 7 bitin üzerindeki tüm karakterlerden onaltılık veya Unicode karakterler olarak çıkış yapılır. |
| WordML | `31` | Belgeyi Microsoft Word 2003 WordprocessingML biçiminde kaydeder. |
| Pdf | `40` | Belgeyi PDF (Adobe Portable Document) formatında kaydeder. |
| Xps | `41` | Belgeyi XPS (XML Kağıt Belirtimi) biçiminde kaydeder. |
| XamlFixed | `42` | Belgeyi Genişletilebilir Uygulama İşaretleme Dili (XAML) biçiminde sabit bir belge olarak kaydeder. |
| Svg | `44` | Belgeyi Svg (Ölçeklenebilir Vektör Grafikleri) formatında kaydeder. |
| HtmlFixed | `45` | Belgeyi, kesinlikle konumlandırılmış öğeleri kullanarak HTML biçiminde kaydeder |
| OpenXps | `46` | Belgeyi OpenXPS (Ecma-388) biçiminde kaydeder. |
| Ps | `47` | Belgeyi PS (PostScript) biçiminde kaydeder. |
| Pcl | `48` | Belgeyi PCL (Yazıcı Kontrol Dili) formatında kaydeder. |
| Html | `50` | Belgeyi HTML biçiminde kaydeder. |
| Mhtml | `51` | Belgeyi MHTML (Web arşivi) biçiminde kaydeder. |
| Epub | `52` | Belgeyi EPUB biçiminde kaydeder. |
| Odt | `60` | Belgeyi bir ODF Metin Belgesi olarak kaydeder. |
| Ott | `61` | Belgeyi bir ODF Metin Belgesi Şablonu olarak kaydeder. |
| Text | `70` | Belgeyi düz metin biçiminde kaydeder. |
| XamlFlow | `71` | **Beta.**Belgeyi, Genişletilebilir Uygulama İşaretleme Dili (XAML) biçiminde bir akış belgesi olarak kaydeder. |
| XamlFlowPack | `72` | **Beta.** Belgeyi, Genişletilebilir Uygulama İşaretleme Dili (XAML) paket biçiminde bir akış belgesi olarak kaydeder. |
| Markdown | `73` | Belgeyi Markdown biçiminde kaydeder. |
| Tiff | `100` | Belgenin bir sayfasını veya sayfalarını işler ve bunları tek veya çok sayfalı bir TIFF dosyasına kaydeder. |
| Png | `101` | Belgenin bir sayfasını oluşturur ve onu PNG dosyası olarak kaydeder. |
| Bmp | `102` | Belgenin bir sayfasını oluşturur ve bir BMP dosyası olarak kaydeder. |
| Emf | `103` | Belgenin bir sayfasını işler ve onu bir vektör EMF (Gelişmiş Meta Dosyası) dosyası olarak kaydeder. |
| Jpeg | `104` | Belgenin bir sayfasını işler ve onu bir JPEG dosyası olarak kaydeder. |
| Gif | `105` | Belgenin bir sayfasını oluşturur ve bir GIF dosyası olarak kaydeder. |

### Örnekler

DOCX'ten HTML formatına nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToHtml.html", SaveFormat.Html);
```

### Ayrıca bakınız

* method [Save](../document/save)
* class [SaveOptions](../../aspose.words.saving/saveoptions)
* ad alanı [Aspose.Words](../../aspose.words)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->