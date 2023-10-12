---
title: LoadOptions.LoadOptions
second_title: Aspose.Words for .NET API Referansı
description: LoadOptions inşaatçı. Bu sınıfın yeni bir örneğini varsayılan değerlerle başlatır.
type: docs
weight: 10
url: /tr/net/aspose.words.loading/loadoptions/loadoptions/
---
## LoadOptions() {#constructor}

Bu sınıfın yeni bir örneğini varsayılan değerlerle başlatır.

```csharp
public LoadOptions()
```

### Örnekler

Temel URI kullanarak bir akıştan görüntüler içeren bir HTML belgesinin nasıl açılacağını gösterir.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Temel klasörü yüklerken URI'yi iletin
    // böylece HTML belgesindeki ilgili URI'lere sahip tüm görseller bulunabilir.
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
* ad alanı [Aspose.Words.Loading](../../loadoptions/)
* toplantı [Aspose.Words](../../../)

---

## LoadOptions(string) {#constructor_2}

Şifrelenmiş bir belgeyi yüklemek için bu sınıfın yeni bir örneğini belirtilen parolayla başlatmak için kullanılan bir kısayol.

```csharp
public LoadOptions(string password)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| password | String | Şifrelenmiş bir belgeyi açmak için kullanılan parola. Olabilir`hükümsüz` veya boş dize. |

### Örnekler

Şifrelenmiş bir Microsoft Word belgesinin nasıl yükleneceğini gösterir.

```csharp
Document doc;

// Aspose.Words, şifrelenmiş bir belgeyi şifresi olmadan açmaya çalışırsak bir istisna atar.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// Böyle bir belge yüklenirken parola, LoadOptions nesnesi kullanılarak belgenin yapıcısına iletilir.
LoadOptions options = new LoadOptions("docPassword");

// Şifrelenmiş bir belgeyi LoadOptions nesnesiyle yüklemenin iki yolu vardır.
// 1 - Belgeyi yerel dosya sisteminden dosya adına göre yükleyin:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Belgeyi bir akıştan yükleyin:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

### Ayrıca bakınız

* class [LoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../loadoptions/)
* toplantı [Aspose.Words](../../../)

---

## LoadOptions(LoadFormat, string, string) {#constructor_1}

Özellikleri belirtilen değerlere ayarlanmış olarak bu sınıfın yeni bir örneğini başlatmak için kullanılan bir kısayol.

```csharp
public LoadOptions(LoadFormat loadFormat, string password, string baseUri)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| loadFormat | LoadFormat | Yüklenecek belgenin formatı. |
| password | String | Şifrelenmiş bir belgeyi açmak için kullanılan parola. Olabilir`hükümsüz` veya boş dize. |
| baseUri | String | Göreli URI'leri mutlak olarak çözümlemek için kullanılacak dize. Olabilir`hükümsüz` veya boş dize. |

### Örnekler

Bir web sayfasının .docx dosyası olarak nasıl kaydedildiğini gösterir.

```csharp
const string url = "https://www.aspose.com/";

using (HttpClient client = new HttpClient()) 
{
    var bytes = await client.GetByteArrayAsync(url);
    using (MemoryStream stream = new MemoryStream(bytes))
    {
        // URL, ilgili görüntü yollarının doğru şekilde alındığından emin olmak için tekrar baseUri olarak kullanılır.
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // HTML belgesini akıştan yükleyin ve LoadOptions nesnesini iletin.
        Document doc = new Document(stream, options);

        // Bu aşamada belgenin içeriğini okuyup düzenleyebilir ve ardından yerel dosya sistemine kaydedebiliriz.
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

Bir html belgesini açarken temel URI'nin nasıl belirtileceğini gösterir.

```csharp
// Göreli bir URI ile bağlantılı bir resim içeren bir .html belgesi yüklemek istediğimizi varsayalım
// resim farklı bir konumdayken. Bu durumda, göreceli URI'yi mutlak bir URI'ye dönüştürmemiz gerekecek.
 // HtmlLoadOptions nesnesini kullanarak bir temel URI sağlayabiliriz.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Görüntü .html girişinde bozuk olsa da, özel temel URI'miz bağlantıyı onarmamıza yardımcı oldu.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Bu çıktı belgesi eksik olan resmi gösterecektir.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### Ayrıca bakınız

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [LoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../loadoptions/)
* toplantı [Aspose.Words](../../../)


