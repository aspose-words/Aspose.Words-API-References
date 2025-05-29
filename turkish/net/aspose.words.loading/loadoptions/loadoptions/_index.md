---
title: LoadOptions
linktitle: LoadOptions
articleTitle: LoadOptions
second_title: .NET için Aspose.Words
description: En iyi performans ve verimlilik için varsayılan değerlerle yeni bir örneği zahmetsizce başlatmak üzere tasarlanmış LoadOptions oluşturucusunu keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.loading/loadoptions/loadoptions/
---
## LoadOptions() {#constructor}

Bu sınıfın yeni bir örneğini varsayılan değerlerle başlatır.

```csharp
public LoadOptions()
```

## Örnekler

Bir akıştan gelen görselleri içeren bir HTML belgesinin temel URI kullanılarak nasıl açılacağını gösterir.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Yükleme sırasında temel klasörün URI'sini geçirin
    // böylece HTML belgesinde bağıl URI'leri olan tüm resimler bulunabilir.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // Belgenin ilk şeklinin geçerli bir resim içerdiğini doğrulayın.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

### Ayrıca bakınız

* class [LoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)

---

## LoadOptions(*string*) {#constructor_2}

Şifrelenmiş bir belgeyi yüklemek için belirtilen parolayla bu sınıfın yeni bir örneğini başlatmak için bir kısayol.

```csharp
public LoadOptions(string password)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| password | String | Şifrelenmiş bir belgeyi açmak için şifre. Olabilir`hükümsüz` veya boş dize. |

## Örnekler

Şifrelenmiş bir Microsoft Word belgesinin nasıl yükleneceğini gösterir.

```csharp
Document doc;

// Şifreli bir belgeyi şifresi olmadan açmaya çalıştığımızda Aspose.Words bir istisna fırlatır.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// Böyle bir belge yüklenirken parola, LoadOptions nesnesi kullanılarak belgenin oluşturucusuna geçirilir.
LoadOptions options = new LoadOptions("docPassword");

// Şifrelenmiş bir belgeyi LoadOptions nesnesiyle yüklemenin iki yolu vardır.
// 1 - Belgeyi yerel dosya sisteminden dosya adına göre yükle:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Belgeyi bir akıştan yükleyin:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

### Ayrıca bakınız

* class [LoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)

---

## LoadOptions(*[LoadFormat](../../../aspose.words/loadformat/), string, string*) {#constructor_1}

Bu sınıfın özelliklerini belirtilen değerlere ayarlayarak yeni bir örneğini başlatmak için bir kısayol.

```csharp
public LoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| loadFormat | LoadFormat | Yüklenecek belgenin biçimi. |
| password | String | Şifrelenmiş bir belgeyi açmak için şifre. Olabilir`hükümsüz` veya boş dize. |
| baseUri | String | Göreceli URI'leri mutlak değere dönüştürmek için kullanılacak dize.`hükümsüz` veya boş dize. |

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

### Ayrıca bakınız

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [LoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
