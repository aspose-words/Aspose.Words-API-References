---
title: Font.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: .NET için Aspose.Words
description: Font Bidi özelliğini keşfedin, web tasarımlarınızda gelişmiş okunabilirlik ve kullanıcı deneyimi için sağdan sola metin özelliklerini kontrol edin.
type: docs
weight: 30
url: /tr/net/aspose.words/font/bidi/
---
## Font.Bidi property

Bu çalışmanın içeriğinin sağdan sola özelliklere sahip olup olmayacağını belirtir.

```csharp
public bool Bidi { get; set; }
```

## Notlar

Bu özellik, açık olduğunda, güçlü soldan sağa metinle kullanılmamalıdır. Bu koşul altındaki herhangi bir davranış belirtilmemiştir. Bu özellik, kapalı olduğunda, güçlü sağdan sola metinle kullanılmamalıdır. Bu koşul altındaki herhangi bir davranış belirtilmemiştir.

Bu çalışmanın içerikleri görüntülendiğinde, tüm karakterler formatting amaçları için karmaşık betik karakterleri olarak ele alınacaktır. Bu,[`BoldBi`](../boldbi/) ,[`ItalicBi`](../italicbi/) ,[`SizeBi`](../sizebi/) ve bu çalışma işlenirken buna karşılık gelen font adı kullanılacaktır.

Ayrıca, bu çalışmanın içerikleri görüntülendiğinde, bu özellik "zayıf tipler" ve "nötr tipler" olarak sınıflandırılan characters için sağdan sola geçersiz kılma işlevi görür.

## Örnekler

Sağdan sola ve sağdan sola metinler için ayrı yazı tipi ayarları kümelerinin nasıl tanımlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Soldan sağa metin için bir dizi yazı tipi ayarı tanımlayın.
builder.Font.Name = "Courier New";
builder.Font.Size = 16;
builder.Font.Italic = false;
builder.Font.Bold = false;
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Sağdan sola metin için başka bir yazı tipi ayarları kümesi tanımlayın.
builder.Font.NameBi = "Andalus";
builder.Font.SizeBi = 24;
builder.Font.ItalicBi = true;
builder.Font.BoldBi = true;
builder.Font.LocaleIdBi = new CultureInfo("ar-AR", false).LCID;

// Eklemek üzere olduğumuz metnin Bidi bayrağını kullanarak gösterilip gösterilmeyeceğini belirtebiliriz.
// belge oluşturucu sağdan soladır. Bu bayrak true olarak ayarlandığında metin eklediğimizde,
// sağdan sola doğru olan yazı tipi ayarları kullanılarak biçimlendirilecektir.
builder.Font.Bidi = true;
builder.Write("مرحبًا");

// Bayrağı false olarak ayarlayın ve ardından soldan sağa metin ekleyin.
// Belge oluşturucu bunları soldan sağa doğru olan yazı tipi ayarlarını kullanarak biçimlendirecektir.
builder.Font.Bidi = false;
builder.Write(" Hello world!");

doc.Save(ArtifactsDir + "Font.Bidi.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
