---
title: Enum SaveFormat
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.SaveFormat Sıralama. Belgenin kaydedildiği biçimi belirtir.
type: docs
weight: 4840
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
| Doc | `10` | Belgeyi Microsoft Word 97 - 2007 Belgesi formatında kaydeder. |
| Dot | `11` | Belgeyi Microsoft Word 97 - 2007 Şablon formatında kaydeder. |
| Docx | `20` | Belgeyi Office Açık XML Kelime İşleme ML Belgesi (makro içermeyen) olarak kaydeder. |
| Docm | `21` | Belgeyi Office Açık XML Kelime İşleme ML Makro Etkin Belgesi olarak kaydeder. |
| Dotx | `22` | Belgeyi Office Açık XML Kelime İşleme ML Şablonu (makro içermeyen) olarak kaydeder. |
| Dotm | `23` | Belgeyi Office Açık XML Kelime İşleme ML Makro Etkin Şablonu olarak kaydeder. |
| FlatOpc | `24` | Belgeyi, ZIP paketi yerine düz bir XML dosyasında depolanan Office Açık XML Kelime İşlemeML'si olarak kaydeder. |
| FlatOpcMacroEnabled | `25` | Belgeyi, ZIP paketi yerine düz bir XML dosyasında saklanan Office Açık XML Kelime İşlemeML Makro Etkin Belgesi olarak kaydeder. |
| FlatOpcTemplate | `26` | Belgeyi, ZIP paketi yerine düz bir XML dosyasında saklanan Office Açık XML Kelime İşleme ML Şablonu (makro içermeyen) olarak kaydeder. |
| FlatOpcTemplateMacroEnabled | `27` | Belgeyi, ZIP paketi yerine düz bir XML dosyasında saklanan Office Açık XML Kelime İşlemeML Makro Etkin Şablonu olarak kaydeder. |
| Rtf | `30` | Belgeyi RTF formatında kaydeder. 7 bitin üzerindeki tüm karakterlerden onaltılık veya Unicode karakterler olarak çıkış yapılır. |
| WordML | `31` | Belgeyi Microsoft Word 2003 WordprocessingML formatında kaydeder. |
| Pdf | `40` | Belgeyi PDF (Adobe Taşınabilir Belge) formatında kaydeder. |
| Xps | `41` | Belgeyi XPS (XML Kağıt Belirtimi) formatında kaydeder. |
| XamlFixed | `42` | Belgeyi Genişletilebilir Uygulama İşaretleme Dili (XAML) biçiminde sabit bir belge olarak kaydeder. |
| Svg | `44` | Belgeyi Svg (Ölçeklenebilir Vektör Grafikleri) formatında kaydeder. |
| HtmlFixed | `45` | Belgeyi kesinlikle konumlandırılmış elemanları kullanarak HTML formatında kaydeder |
| OpenXps | `46` | Belgeyi OpenXPS (Ecma-388) formatında kaydeder. |
| Ps | `47` | Belgeyi PS (PostScript) formatında kaydeder. |
| Pcl | `48` | Belgeyi PCL (Yazıcı Kontrol Dili) formatında kaydeder. |
| Html | `50` | Belgeyi HTML formatında kaydeder. |
| Mhtml | `51` | Belgeyi MHTML (Web arşivi) formatında kaydeder. |
| Epub | `52` | Belgeyi EPUB formatında kaydeder. |
| Azw3 | `53` | Belgeyi AZW3 formatında kaydeder. |
| Mobi | `54` | Belgeyi MOBI formatında kaydeder. |
| Odt | `60` | Belgeyi ODF Metin Belgesi olarak kaydeder. |
| Ott | `61` | Belgeyi ODF Metin Belgesi Şablonu olarak kaydeder. |
| Text | `70` | Belgeyi düz metin biçiminde kaydeder. |
| XamlFlow | `71` | **Beta.** Belgeyi Genişletilebilir Uygulama İşaretleme Dili (XAML) biçiminde bir akış belgesi olarak kaydeder. |
| XamlFlowPack | `72` | **Beta.** Belgeyi Genişletilebilir Uygulama İşaretleme Dili (XAML) paket biçiminde bir akış belgesi olarak kaydeder. |
| Markdown | `73` | Belgeyi Markdown formatında kaydeder. |
| Xlsx | `80` | Belgeyi Office Açık XML Elektronik TabloML Belgesi (makro içermeyen) olarak kaydeder. |
| Tiff | `100` | Belgenin bir sayfasını veya sayfalarını oluşturur ve bunları tek veya çok sayfalı bir TIFF dosyasına kaydeder. |
| Png | `101` | Belgenin bir sayfasını oluşturur ve bunu PNG dosyası olarak kaydeder. |
| Bmp | `102` | Belgenin bir sayfasını oluşturur ve BMP dosyası olarak kaydeder. |
| Emf | `103` | Belgenin bir sayfasını oluşturur ve onu bir vektör EMF (Gelişmiş Meta Dosyası) dosyası olarak kaydeder. |
| Jpeg | `104` | Belgenin bir sayfasını oluşturur ve onu JPEG dosyası olarak kaydeder. |
| Gif | `105` | Belgenin bir sayfasını oluşturur ve GIF dosyası olarak kaydeder. |
| Eps | `106` | Belgenin bir sayfasını oluşturur ve bunu bir EPS dosyası olarak kaydeder. |

### Örnekler

DOCX'ten HTML biçimine nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToHtml.html", SaveFormat.Html);
```

### Ayrıca bakınız

* method [Save](../document/save/)
* class [SaveOptions](../../aspose.words.saving/saveoptions/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


