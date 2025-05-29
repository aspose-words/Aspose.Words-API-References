---
title: SaveFormat Enum
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: .NET için Aspose.Words
description: Sorunsuz iş akışları için dosya yönetiminizi ve uyumluluğunuzu geliştirerek belge kaydetme biçimlerini kolayca seçmek için Aspose.Words.SaveFormat enum'unu keşfedin.
type: docs
weight: 5580
url: /tr/net/aspose.words/saveformat/
---
## SaveFormat enumeration

Belgenin kaydedildiği formatı belirtir.

```csharp
public enum SaveFormat
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Unknown | `0` | Varsayılan, dosya biçimi için geçersiz değer. |
| Doc | `10` | Belgeyi Microsoft Word 97 - 2007 Belge biçiminde kaydeder. |
| Dot | `11` | Belgeyi Microsoft Word 97 - 2007 Şablonu biçiminde kaydeder. |
| Docx | `20` | Belgeyi Office Açık XML WordprocessingML Belgesi (makro içermeyen) olarak kaydeder. |
| Docm | `21` | Belgeyi Office Açık XML WordprocessingML Makro Etkinleştirilmiş Belge olarak kaydeder. |
| Dotx | `22` | Belgeyi Office Açık XML WordprocessingML Şablonu (makro içermeyen) olarak kaydeder. |
| Dotm | `23` | Belgeyi Office Açık XML WordprocessingML Makro Etkin Şablonu olarak kaydeder. |
| FlatOpc | `24` | Belgeyi, ZIP paketi yerine düz bir XML dosyasında saklanan bir Office Open XML WordprocessingML olarak kaydeder. |
| FlatOpcMacroEnabled | `25` | Belgeyi, ZIP paketi yerine düz bir XML dosyasında saklanan Office Açık XML WordprocessingML Makro Etkinleştirilmiş Belge olarak kaydeder. |
| FlatOpcTemplate | `26` | Belgeyi, bir ZIP paketi yerine düz bir XML dosyasında saklanan bir Office Açık XML Kelime İşleme ML Şablonu (makro içermeyen) olarak kaydeder. |
| FlatOpcTemplateMacroEnabled | `27` | Belgeyi, ZIP paketi yerine düz bir XML dosyasında saklanan Office Açık XML WordprocessingML Makro Etkin Şablonu olarak kaydeder. |
| Rtf | `30` | Belgeyi RTF biçiminde kaydeder. 7 bitin üzerindeki tüm karakterler onaltılık veya Unicode karakterleri olarak kaçırılır. |
| WordML | `31` | Belgeyi Microsoft Word 2003 WordprocessingML biçiminde kaydeder. |
| Pdf | `40` | Belgeyi PDF (Adobe Taşınabilir Belge) biçiminde kaydeder. |
| Xps | `41` | Belgeyi XPS (XML Kağıt Spesifikasyonu) biçiminde kaydeder. |
| XamlFixed | `42` | Belgeyi Genişletilebilir Uygulama İşaretleme Dili (XAML) biçiminde sabit bir belge olarak kaydeder. |
| Svg | `44` | Belgeyi Svg (Ölçeklenebilir Vektör Grafikleri) biçiminde kaydeder. |
| HtmlFixed | `45` | Belgeyi mutlak konumlandırılmış öğeleri kullanarak HTML biçiminde kaydeder |
| OpenXps | `46` | Belgeyi OpenXPS (Ecma-388) biçiminde kaydeder. |
| Ps | `47` | Belgeyi PS (PostScript) biçiminde kaydeder. |
| Pcl | `48` | Belgeyi PCL (Yazıcı Kontrol Dili) biçiminde kaydeder. |
| Html | `50` | Belgeyi HTML biçiminde kaydeder. |
| Mhtml | `51` | Belgeyi MHTML (Web arşivi) biçiminde kaydeder. |
| Epub | `52` | Belgeyi EPUB formatında kaydeder. |
| Azw3 | `53` | Belgeyi AZW3 biçiminde kaydeder. |
| Mobi | `54` | Belgeyi MOBI formatında kaydeder. |
| Odt | `60` | Belgeyi ODF Metin Belgesi olarak kaydeder. |
| Ott | `61` | Belgeyi ODF Metin Belgesi Şablonu olarak kaydeder. |
| Text | `70` | Belgeyi düz metin biçiminde kaydeder. |
| XamlFlow | `71` | **Beta.** Belgeyi Genişletilebilir Uygulama İşaretleme Dili (XAML) biçiminde bir akış belgesi olarak kaydeder. |
| XamlFlowPack | `72` | **Beta.** Belgeyi Genişletilebilir Uygulama İşaretleme Dili (XAML) paketi biçiminde bir akış belgesi olarak kaydeder. |
| Markdown | `73` | Belgeyi Markdown biçiminde kaydeder. |
| Xlsx | `80` | Belgeyi Office Open XML SpreadsheetML Belgesi (makro içermeyen) olarak kaydeder. |
| Tiff | `100` | Belgenin bir veya birden fazla sayfasını işler ve bunları tek veya çok sayfalı bir TIFF dosyasına kaydeder. |
| Png | `101` | Belgenin bir sayfasını işler ve onu PNG dosyası olarak kaydeder. |
| Bmp | `102` | Belgenin bir sayfasını işler ve bunu bir BMP dosyası olarak kaydeder. |
| Emf | `103` | Belgenin bir sayfasını işler ve onu bir vektör EMF (Gelişmiş Meta Dosyası) dosyası olarak kaydeder. |
| Jpeg | `104` | Belgenin bir sayfasını işler ve onu JPEG dosyası olarak kaydeder. |
| Gif | `105` | Belgenin bir sayfasını işler ve bunu bir GIF dosyası olarak kaydeder. |
| Eps | `106` | Belgenin bir sayfasını işler ve bunu bir EPS dosyası olarak kaydeder. |
| WebP | `107` | Belgenin bir sayfasını işler ve onu bir WebP dosyası olarak kaydeder. |

## Örnekler

DOCX'ten HTML formatına nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToHtml.html", SaveFormat.Html);
```

### Ayrıca bakınız

* method [Save](../document/save/)
* class [SaveOptions](../../aspose.words.saving/saveoptions/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
