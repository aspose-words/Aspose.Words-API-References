---
title: LoadFormat
second_title: Aspose.Words for .NET API Referansı
description: Yüklenecek belgenin biçimini belirtir.
type: docs
weight: 3350
url: /tr/net/aspose.words/loadformat/
---
## LoadFormat enumeration

Yüklenecek belgenin biçimini belirtir.

```csharp
public enum LoadFormat
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Auto | `0` | Aspose.Words'e formatı otomatik olarak tanıması talimatını verir. |
| Doc | `10` | Microsoft Word 95 veya Word 97 - 2003 Belgesi. |
| Dot | `11` | Microsoft Word 95 veya Word 97 - 2003 Şablonu. |
| DocPreWord60 | `12` | Belge Word 95 öncesi biçimindedir. Aspose.Words şu anda bu tür belgelerin yüklenmesini desteklememektedir. |
| Docx | `20` | Office Açık XML Kelime İşlemeML Belgesi (makro içermez). |
| Docm | `21` | Office Açık XML Kelime İşlemeML Makro Etkin Belge. |
| Dotx | `22` | Office Açık XML Kelime İşlemeML Şablonu (makro içermez). |
| Dotm | `23` | Office Açık XML Sözcük İşlemeML Makro Etkin Şablon. |
| FlatOpc | `24` | Office Açık XML Kelime İşlemeML, ZIP paketi yerine düz bir XML dosyasında depolanır. |
| FlatOpcMacroEnabled | `25` | Office Açık XML Kelime İşlemeML Makro-Etkin Belge, ZIP paketi yerine düz bir XML dosyasında depolanır. |
| FlatOpcTemplate | `26` | Office Açık XML Kelime İşlemeML Şablonu (makro içermeyen), ZIP paketi yerine düz bir XML dosyasında depolanır. |
| FlatOpcTemplateMacroEnabled | `27` | Office Açık XML Kelime İşlemeML Makro-Etkin Şablonu, ZIP paketi yerine düz bir XML dosyasında depolanır. |
| Rtf | `30` | RTF biçimi. |
| WordML | `31` | Microsoft Word 2003 Kelime İşlemeML biçimi. |
| Html | `50` | HTML biçimi. |
| Mhtml | `51` | MHTML (Web arşivi) biçimi. |
| Mobi | `52` | MOBI biçimi. MobiPocket okuyucu ve Amazon Kindle okuyucuları tarafından kullanılır. |
| Chm | `53` | CHM (Derlenmiş HTML Yardımı) biçimi. |
| Azw3 | `54` | AZW3 biçimi. Amazon Kindle okuyucuları tarafından kullanılır. |
| Epub | `55` | EPUB biçimi. |
| Odt | `60` | ODF Metin Belgesi. |
| Ott | `61` | ODF Metin Belgesi Şablonu. |
| Text | `62` | Düz Metin. |
| Markdown | `63` | İşaretleme metin belgesi. |
| Pdf | `64` | Pdf belgesi. |
| Xml | `65` | XML belgesi. |
| Unknown | `255` | Tanınmayan format, Aspose.Words tarafından yüklenemez. |

### Örnekler

Bir web sayfasının .docx dosyası olarak nasıl kaydedildiğini gösterir.

```csharp
const string url = "http://www.aspose.com/";

using (WebClient client = new WebClient()) 
{ 
    using (MemoryStream stream = new MemoryStream(client.DownloadData(url)))
    {
        // Göreli görüntü yollarının doğru bir şekilde alınmasını sağlamak için URL tekrar baseUri olarak kullanılır.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // HTML belgesini akıştan yükleyin ve LoadOptions nesnesini iletin.
        Document doc = new Document(stream, options);

        // Bu aşamada belgenin içeriğini okuyup düzenleyebilir ve ardından yerel dosya sistemine kaydedebiliriz.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

Bir html belgesini açarken bir temel URI'nin nasıl belirtileceğini gösterir.

```csharp
// Göreli bir URI ile bağlantılı bir resim içeren bir .html belgesi yüklemek istediğimizi varsayalım.
// görüntü farklı bir konumdayken. Bu durumda, göreli URI'yi mutlak bir URI'ye çözmemiz gerekecek.
 // Bir HtmlLoadOptions nesnesi kullanarak bir temel URI sağlayabiliriz.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// .html girişinde görüntü bozukken, özel temel URI'miz bağlantıyı onarmamıza yardımcı oldu.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Bu çıktı belgesi, eksik olan resmi gösterecektir.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

Bir belgenin biçimini algılamak için FileFormatUtil yöntemlerinin nasıl kullanılacağını gösterir.

```csharp
// Dosya uzantısı olmayan bir dosyadan bir belge yükleyin ve ardından dosya biçimini tespit edin.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // Aşağıda, bir LoadFormat'ı karşılık gelen SaveFormat'a dönüştürmenin iki yöntemi bulunmaktadır.
    // 1 - LoadFormat için dosya uzantısı dizesini alın, ardından bu dizeden karşılık gelen SaveFormat'ı alın:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - LoadFormat'ı doğrudan SaveFormat'ına dönüştürün:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Akıştan bir belge yükleyin ve ardından otomatik olarak algılanan dosya uzantısına kaydedin.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
