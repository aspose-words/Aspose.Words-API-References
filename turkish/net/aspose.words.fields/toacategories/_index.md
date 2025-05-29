---
title: ToaCategories Class
linktitle: ToaCategories
articleTitle: ToaCategories
second_title: .NET için Aspose.Words
description: Belgelerinizdeki yetki kategorilerinin verimli yönetimi için Aspose.Words.Fields.ToaCategories sınıfını keşfedin. Belge yapılandırmanızı geliştirin!
type: docs
weight: 3190
url: /tr/net/aspose.words.fields/toacategories/
---
## ToaCategories class

Yetki kategorilerinin bir tablosunu temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public class ToaCategories
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [ToaCategories](toacategories/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| static [DefaultCategories](../../aspose.words.fields/toacategories/defaultcategories/) { get; } | Yetkili kategorilerinin varsayılan tablosunu alır. |
| [Item](../../aspose.words.fields/toacategories/item/) { get; set; } | Kategori numarasına göre kategori başlığını alır veya ayarlar. |

## Örnekler

TOA alanları için bir kategori kümesinin nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// TOA alanları, girdilerini bu koleksiyonda tanımlanan kategorilere göre filtreleyebilir.
ToaCategories toaCategories = new ToaCategories();
doc.FieldOptions.ToaCategories = toaCategories;

// Bu kategori koleksiyonu varsayılan değerlerle gelir ve bunları özel değerlerle değiştirebiliriz.
Assert.AreEqual("Cases", toaCategories[1]);
Assert.AreEqual("Statutes", toaCategories[2]);

toaCategories[1] = "My Category 1";
toaCategories[2] = "My Category 2";

// Bu koleksiyon aracılığıyla her zaman varsayılan değerlere erişebiliriz.
Assert.AreEqual("Cases", ToaCategories.DefaultCategories[1]);
Assert.AreEqual("Statutes", ToaCategories.DefaultCategories[2]);

// 2 TOA alanı ekle. TOA alanları, belgedeki her TA alanı için bir giriş oluşturur.
// Koleksiyonumuzdan bir kategorinin dizinini seçmek için "\c" anahtarını kullanın.
// Bu anahtarla, bir TOA alanı yalnızca TA alanlarından girişleri alacaktır.
// ayrıca eşleşen bir kategori indeksi olan bir "\c" anahtarına da sahip olun. Her TOA alanı ayrıca görüntülenecektir
// "\c" anahtarının işaret ettiği kategorinin adı.
builder.InsertField("TOA \\c 1 \\h", null);
builder.InsertField("TOA \\c 2 \\h", null);
builder.InsertBreak(BreakType.PageBreak);

// 2 kategoriye TOA girişleri ekleyin. İlk TOA alanımız bir giriş alacaktır,
// "\c" anahtarı da ilk kategoriye işaret eden ikinci TA alanından.
// İkinci TOA alanı diğer iki TA alanından iki girişe sahip olacak.
builder.InsertField("TA \\c 2 \\l \"entry 1\"");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertField("TA \\c 1 \\l \"entry 2\"");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertField("TA \\c 2 \\l \"entry 3\"");

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.TOA.Categories.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
