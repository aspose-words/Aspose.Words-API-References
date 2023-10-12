---
title: Class TextColumnCollection
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.TextColumnCollection sınıf. Bir koleksiyonTextColumn bir belgenin bir bölümündeki metnin tüm sütunlarını temsil eden nesneler.
type: docs
weight: 6400
url: /tr/net/aspose.words/textcolumncollection/
---
## TextColumnCollection class

Bir koleksiyon[`TextColumn`](../textcolumn/) bir belgenin bir bölümündeki metnin tüm sütunlarını temsil eden nesneler.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Bölümlerle Çalışmak](https://docs.aspose.com/words/net/working-with-sections/) dokümantasyon makalesi.

```csharp
public class TextColumnCollection
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/textcolumncollection/count/) { get; } | Belgenin bölümündeki sütunların sayısını alır. |
| [EvenlySpaced](../../aspose.words/textcolumncollection/evenlyspaced/) { get; set; } | Metin sütunları eşit genişlikte ve eşit aralıklıysa doğrudur. |
| [Item](../../aspose.words/textcolumncollection/item/) { get; } | Belirtilen dizindeki bir metin sütununu döndürür. |
| [LineBetween](../../aspose.words/textcolumncollection/linebetween/) { get; set; } | Ne zaman`doğru` sütunların arasına dikey bir çizgi ekler. |
| [Spacing](../../aspose.words/textcolumncollection/spacing/) { get; set; } | Sütunlar eşit aralıklarla yerleştirildiğinde, her sütun arasındaki boşluk miktarını nokta cinsinden alır veya ayarlar. |
| [Width](../../aspose.words/textcolumncollection/width/) { get; } | Sütunlar eşit aralıklarla yerleştirildiğinde sütunların genişliğini alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [SetCount](../../aspose.words/textcolumncollection/setcount/)(int) | Metni belirtilen sayıda metin sütunu halinde düzenler. |

### Notlar

Kullanmak[`SetCount`](./setcount/) Metin sütunlarının sayısını ayarlamak için.

Tüm sütunların eşit genişliğe ve eşit aralıklara sahip olmasını sağlamak için[`EvenlySpaced`](./evenlyspaced/) ile`doğru` ve sütunlar arasındaki boşluk miktarını belirtin[`Spacing`](./spacing/). MS Word will sütun genişliklerini otomatik olarak hesaplar.

eğer varsa[`EvenlySpaced`](./evenlyspaced/) ayarlanır`YANLIŞ` , her sütunu için genişliği ve aralığı ayrı ayrı belirtmeniz gerekir. Bireye erişmek için dizin oluşturucuyu kullanın[`TextColumn`](../textcolumn/) nesneler.

Özel sütun genişlikleri kullanırken, tüm sütun genişliklerinin ve aralarındaki aralıkların (x000d_) toplamının, sayfa genişliği eksi sol ve sağ sayfa kenar boşluklarına eşit olduğundan emin olun.

### Örnekler

Bir bölümde birden çok eşit aralıklı sütunun nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.Spacing = 100;
columns.SetCount(2);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

doc.Save(ArtifactsDir + "PageSetup.ColumnsSameWidth.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


