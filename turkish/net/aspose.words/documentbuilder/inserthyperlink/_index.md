---
title: DocumentBuilder.InsertHyperlink
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder yöntem. Belgeye bir köprü ekler.
type: docs
weight: 370
url: /tr/net/aspose.words/documentbuilder/inserthyperlink/
---
## DocumentBuilder.InsertHyperlink method

Belgeye bir köprü ekler.

```csharp
public Field InsertHyperlink(string displayText, string urlOrBookmark, bool isBookmark)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| displayText | String | Belgede görüntülenecek bağlantının metni. |
| urlOrBookmark | String | Bağlantı hedefi. Bir URL veya belge içindeki bir yer işaretinin adı olabilir. Bu yöntem her zaman URL'nin başına ve sonuna kesme işareti ekler. |
| isBookmark | Boolean | `doğru` önceki parametre belge içindeki bir yer iminin adı ise; `YANLIŞ` önceki parametre bir URL'dir. |

### Geri dönüş değeri

A[`Field`](../../../aspose.words.fields/field/) eklenen alanı temsil eden nesne.

### Notlar

Köprü görüntüleme metni için yazı tipi formatını açıkça kullanarak belirtmeniz gerektiğini unutmayın.[`Font`](../font/) mülk.

Bu yöntemler dahili olarak çağırır[`InsertField`](../insertfield/) belgeye bir MS Word HYPERLINK field eklemek için.

### Örnekler

Yerel bir yer imine başvuran bir köprünün nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("Bookmark1");
builder.Write("Bookmarked text. ");
builder.EndBookmark("Bookmark1");
builder.Writeln("Text outside of the bookmark.");

// Yer imine bağlanan bir KÖPRÜ alanı ekleyin. Alan anahtarlarını geçebiliriz
// başvurulan yer iminin adını içeren bağımsız değişkenin bir parçası olarak "InsertHyperlink" yöntemine.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Link to Bookmark1", @"Bookmark1"" \o ""Hyperlink Tip", true);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

Köprü alanının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Bir köprü ekleyin ve bunu özel biçimlendirmeyle vurgulayın.
// Köprü, bizi URL'de belirtilen konuma götürecek tıklanabilir bir metin parçası olacaktır.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", false);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Microsoft Word'deki metindeki bağlantıya Ctrl + sol tıklamak bizi yeni bir web tarayıcı penceresi aracılığıyla URL'ye götürecektir.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

Belge oluşturucunun biçimlendirme yığınının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Yazı tipi formatını ayarlayın, ardından köprüden önce gelen metni yazın.
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

// Yığındaki mevcut biçimlendirme yapılandırmamızı koruyun.
builder.PushFont();

// Yeni bir stil uygulayarak oluşturucunun mevcut formatını değiştirin.
builder.Font.StyleIdentifier = StyleIdentifier.Hyperlink;
builder.InsertHyperlink("here", "http://www.google.com", false);

Assert.AreEqual(Color.Blue.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.Single, builder.Font.Underline);

// Daha önce kaydettiğimiz yazı tipi formatını geri yükleyin ve öğeyi yığından kaldırın.
builder.PopFont();

Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.None, builder.Font.Underline);

builder.Write(". We hope you enjoyed the example.");

doc.Save(ArtifactsDir + "DocumentBuilder.PushPopFont.docx");
```

### Ayrıca bakınız

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)


