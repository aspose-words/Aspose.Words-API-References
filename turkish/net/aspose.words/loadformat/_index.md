---
title: LoadFormat Enum
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: .NET için Aspose.Words
description: Uygulamalarınızda sorunsuz yükleme ve gelişmiş uyumluluk için belge biçimlerini tanımlayan Aspose.Words.LoadFormat enum'unu keşfedin.
type: docs
weight: 4000
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
| Auto | `0` | Aspose.Words'e formatı otomatik olarak tanımasını söyler. |
| MsWorks | `8` | Microsoft Works 8 Belgesi. |
| Doc | `10` | Microsoft Word 95 veya Word 97 - 2003 Belgesi. |
| Dot | `11` | Microsoft Word 95 veya Word 97 - 2003 Şablonu. |
| DocPreWord60 | `12` | Belge Word 95 öncesi biçimdedir. Aspose.Words şu anda bu tür belgelerin yüklenmesini desteklemiyor. |
| Docx | `20` | Office Açık XML Kelime İşlemeML Belgesi (makro içermeyen). |
| Docm | `21` | Office Açık XML Kelime İşlemeML Makro Etkinleştirilmiş Belge. |
| Dotx | `22` | Office Açık XML Kelime İşlemeML Şablonu (makro içermeyen). |
| Dotm | `23` | Office Açık XML Kelime İşlemeML Makro Etkin Şablonu. |
| FlatOpc | `24` | Office Open XML WordprocessingML, bir ZIP paketi yerine düz bir XML dosyasında saklanır. |
| FlatOpcMacroEnabled | `25` | Office Open XML WordprocessingML Makro Etkinleştirilmiş Belge, bir ZIP paketi yerine düz bir XML dosyasında saklanır. |
| FlatOpcTemplate | `26` | Office Open XML WordprocessingML Şablonu (makro içermeyen) ZIP paketi yerine düz bir XML dosyasında saklanır. |
| FlatOpcTemplateMacroEnabled | `27` | Office Open XML WordprocessingML Makro Etkin Şablonu, bir ZIP paketi yerine düz bir XML dosyasında saklanır. |
| Rtf | `30` | RTF biçimi. |
| WordML | `31` | Microsoft Word 2003 KelimeişlemeML biçimi. |
| Html | `50` | HTML biçimi. |
| Mhtml | `51` | MHTML (Web arşivi) biçimi. |
| Mobi | `52` | MOBI formatı. MobiPocket okuyucu ve Amazon Kindle okuyucuları tarafından kullanılır. |
| Chm | `53` | CHM (Derlenmiş HTML Yardımı) biçimi. |
| Azw3 | `54` | AZW3 formatı. Amazon Kindle okuyucuları tarafından kullanılır. |
| Epub | `55` | EPUB biçimi. |
| Odt | `60` | ODF Metin Belgesi. |
| Ott | `61` | ODF Metin Belgesi Şablonu. |
| Text | `62` | Düz Metin. |
| Markdown | `63` | Markdown metin belgesi. |
| Pdf | `64` | Pdf belgesi. |
| Xml | `65` | XML belgesi. |
| Unknown | `255` | Tanınmayan biçim, Aspose.Words tarafından yüklenemiyor. |

## Örnekler

Bir web sayfasının .docx dosyası olarak nasıl kaydedileceğini gösterir.

```csharp
const string url = "https://ürünler.aspose.com/kelimeler/";

using (WebClient client = new WebClient())
{
    var bytes = client.DownloadData(url);
    using (MemoryStream stream = new MemoryStream(bytes))
    {
        // Herhangi bir bağıl görüntü yolunun doğru şekilde alındığından emin olmak için URL tekrar bir baseUri olarak kullanılır.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // HTML belgesini akıştan yükleyin ve LoadOptions nesnesini geçirin.
        Document doc = new Document(stream, options);

        // Bu aşamada belgenin içeriğini okuyup düzenleyebilir ve ardından yerel dosya sistemine kaydedebiliriz.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

Bir HTML belgesini açarken temel URI'nin nasıl belirtileceğini gösterir.

```csharp
// Göreceli bir URI ile bağlantılı bir resim içeren bir .html belgesi yüklemek istediğimizi varsayalım
// görüntü farklı bir konumdayken. Bu durumda, bağıl URI'yi mutlak olana dönüştürmemiz gerekecektir.
 // HtmlLoadOptions nesnesini kullanarak bir temel URI sağlayabiliriz.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Giriş .html'deki resim bozulmuş olsa da, özel temel URI'miz bağlantıyı onarmamıza yardımcı oldu.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Bu çıktı belgesi eksik olan resmi gösterecektir.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

Bir belgenin biçimini algılamak için FileFormatUtil yöntemlerinin nasıl kullanılacağını gösterir.

```csharp
// Dosya uzantısı eksik olan bir dosyadan bir belge yükleyin ve ardından dosya biçimini algılayın.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // Aşağıda bir LoadFormat'ı karşılık gelen SaveFormat'a dönüştürmenin iki yöntemi bulunmaktadır.
    // 1 - LoadFormat için dosya uzantısı dizesini al, ardından bu dizeden karşılık gelen SaveFormat'ı al:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - LoadFormat'ı doğrudan SaveFormat'ına dönüştür:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Akıştan bir belge yükleyin ve ardından otomatik olarak algılanan dosya uzantısıyla kaydedin.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
