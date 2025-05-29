---
title: DocumentBuilder.InsertHyperlink
linktitle: InsertHyperlink
articleTitle: InsertHyperlink
second_title: .NET için Aspose.Words
description: Belgelerinizi DocumentBuilder'ın InsertHyperlink yöntemiyle geliştirin, gelişmiş gezinme ve kullanıcı etkileşimi için tıklanabilir bağlantıları zahmetsizce ekleyin.
type: docs
weight: 390
url: /tr/net/aspose.words/documentbuilder/inserthyperlink/
---
## DocumentBuilder.InsertHyperlink method

Belgeye bir köprü metni ekler.

```csharp
public Field InsertHyperlink(string displayText, string urlOrBookmark, bool isBookmark)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| displayText | String | Belgede görüntülenecek bağlantının metni. |
| urlOrBookmark | String | Bağlantı hedefi. Bir URL veya belgenin içindeki bir yer iminin adı olabilir. Bu yöntem her zaman URL'nin başına ve sonuna kesme işareti ekler. |
| isBookmark | Boolean | `doğru` eğer önceki parametre belgenin içindeki bir yer iminin adıysa; `YANLIŞ` önceki parametre bir URL'dir. |

### Geri dönüş değeri

A[`Field`](../../../aspose.words.fields/field/) eklenen alanı temsil eden nesne.

## Notlar

Köprü metni görüntüleme metni için yazı tipi biçimlendirmesini açıkça belirtmeniz gerektiğini unutmayın [`Font`](../font/) mülk.

Bu yöntemler dahili olarak çağrılır[`InsertField`](../insertfield/)Belgeye bir MS Word HYPERLINK alanı eklemek için.

## Örnekler

Bir köprü metni alanının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Bir köprü metni ekleyin ve özel biçimlendirmeyle vurgulayın.
// Köprü metni, URL'de belirtilen yere bizi götürecek tıklanabilir bir metin parçası olacaktır.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", yanlış);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Microsoft Word'de metindeki bağlantıya Ctrl + sol tıklama bizi yeni bir web tarayıcısı penceresi aracılığıyla URL'ye götürecektir.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

Yerel bir yer imine referans veren bir köprü metninin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("Bookmark1");
builder.Write("Bookmarked text. ");
builder.EndBookmark("Bookmark1");
builder.Writeln("Text outside of the bookmark.");

// Yer imine bağlanan bir HYPERLINK alanı ekleyin. Alan anahtarlarını geçebiliriz
// başvurulan yer iminin adını içeren argümanın bir parçası olarak "InsertHyperlink" yöntemine.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
FieldHyperlink hyperlink = (FieldHyperlink)builder.InsertHyperlink("Link to Bookmark1", "Bookmark1", true);
hyperlink.ScreenTip = "Hyperlink Tip";

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

Bir belge oluşturucunun biçimlendirme yığınının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Yazı tipi biçimlendirmesini ayarlayın, ardından köprü metninden önce gelecek metni yazın.
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

// Yığındaki mevcut biçimlendirme yapılandırmamızı koruyalım.
builder.PushFont();

// Yeni bir stil uygulayarak oluşturucunun geçerli biçimlendirmesini değiştirin.
builder.Font.StyleIdentifier = StyleIdentifier.Hyperlink;
builder.InsertHyperlink("here", "http://www.google.com", yanlış);

Assert.AreEqual(Color.Blue.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.Single, builder.Font.Underline);

// Daha önce kaydettiğimiz yazı tipi biçimlendirmesini geri yükleyin ve öğeyi yığından kaldırın.
builder.PopFont();

Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.None, builder.Font.Underline);

builder.Write(". We hope you enjoyed the example.");

doc.Save(ArtifactsDir + "DocumentBuilder.PushPopFont.docx");
```

### Ayrıca bakınız

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
