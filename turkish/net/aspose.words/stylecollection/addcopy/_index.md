---
title: StyleCollection.AddCopy
linktitle: AddCopy
articleTitle: AddCopy
second_title: .NET için Aspose.Words
description: StyleCollection AddCopy yöntemi ile stilleri zahmetsizce kopyalayın. Tasarım iş akışınızı geliştirin ve stil yönetiminizi bugün kolaylaştırın!
type: docs
weight: 70
url: /tr/net/aspose.words/stylecollection/addcopy/
---
## StyleCollection.AddCopy method

Bu koleksiyona bir stil kopyalar.

```csharp
public Style AddCopy(Style style)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| style | Style | Kopyalanacak bir stil. |

### Geri dönüş değeri

Kopyalanmış stil kullanıma hazır.

## Notlar

Kopyalanacak stil aynı belgeye ait olabileceği gibi farklı bir belgeye de ait olabilir.

Bağlantılı stil kopyalandı.

Bu yöntem temel stilleri kopyalamaz.

Eğer koleksiyonda aynı isimde bir stil varsa, o zaman yeni isim is 0'dan başlayarak "_number" eki eklenerek otomatik olarak üretilir, örneğin "Normal_0", "Başlık 1_1" vb. [`Name`](../../style/name/) içe aktarılan stilin adını değiştirmek için ayarlayıcı.

## Örnekler

Bir belgedeki stilin başka bir belgeye nasıl aktarılacağını gösterir.

```csharp
Document srcDoc = new Document();

// Kaynak belge için özel bir stil oluşturun.
Style srcStyle = srcDoc.Styles.Add(StyleType.Paragraph, "MyStyle");
srcStyle.Font.Color = Color.Red;

// Kaynak belgenin özel stilini hedef belgeye aktar.
Document dstDoc = new Document();
Style newStyle = dstDoc.Styles.AddCopy(srcStyle);

// İçeri aktarılan stilin görünümü kaynak stiliyle aynıdır.
Assert.AreEqual("MyStyle", newStyle.Name);
Assert.AreEqual(Color.Red.ToArgb(), newStyle.Font.Color.ToArgb());
```

Bir belgenin stilinin nasıl kopyalanacağını gösterir.

```csharp
Document doc = new Document();

// AddCopy yöntemi belirtilen stilin bir kopyasını oluşturur ve
// stil için otomatik olarak "Başlık 1_0" gibi yeni bir ad üretir.
Style newStyle = doc.Styles.AddCopy(doc.Styles["Heading 1"]);

// Stilin tanımlayıcı adını değiştirmek için stilin "Ad" özelliğini kullanın.
newStyle.Name = "My Heading 1";

// Belgemiz artık farklı isimlere sahip, aynı görünümlü iki stile sahip.
// Stillerden birinin ayarlarını değiştirmek diğerini etkilemez.
newStyle.Font.Color = Color.Red;

Assert.AreEqual("My Heading 1", newStyle.Name);
Assert.AreEqual("Heading 1", doc.Styles["Heading 1"].Name);

Assert.AreEqual(doc.Styles["Heading 1"].Type, newStyle.Type);
Assert.AreEqual(doc.Styles["Heading 1"].Font.Name, newStyle.Font.Name);
Assert.AreEqual(doc.Styles["Heading 1"].Font.Size, newStyle.Font.Size);
Assert.AreNotEqual(doc.Styles["Heading 1"].Font.Color, newStyle.Font.Color);
```

### Ayrıca bakınız

* class [Style](../../style/)
* class [StyleCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
