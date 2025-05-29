---
title: TextColumnCollection Class
linktitle: TextColumnCollection
articleTitle: TextColumnCollection
second_title: .NET için Aspose.Words
description: Belgelerinizdeki metin sütunlarını zahmetsizce yönetmek için Aspose.Words.TextColumnCollection'ı keşfedin. Belge biçimlendirmenizi kolaylıkla geliştirin!
type: docs
weight: 7250
url: /tr/net/aspose.words/textcolumncollection/
---
## TextColumnCollection class

Bir koleksiyon[`TextColumn`](../textcolumn/) bir belgenin bir bölümündeki tüm metin sütunlarını temsil eden nesneler.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Bölümlerle Çalışma](https://docs.aspose.com/words/net/working-with-sections/) belgeleme makalesi.

```csharp
public class TextColumnCollection
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/textcolumncollection/count/) { get; } | Bir belgenin bölümündeki sütun sayısını alır. |
| [EvenlySpaced](../../aspose.words/textcolumncollection/evenlyspaced/) { get; set; } | Metin sütunları eşit genişlikte ve eşit aralıklıysa doğrudur. |
| [Item](../../aspose.words/textcolumncollection/item/) { get; } | Belirtilen dizinde bir metin sütunu döndürür. |
| [LineBetween](../../aspose.words/textcolumncollection/linebetween/) { get; set; } | Ne zaman`doğru` , sütunlar arasına dikey bir çizgi ekler. |
| [Spacing](../../aspose.words/textcolumncollection/spacing/) { get; set; } | Sütunlar eşit aralıklı olduğunda, her sütun arasındaki boşluk miktarını noktalar halinde alır veya ayarlar. |
| [Width](../../aspose.words/textcolumncollection/width/) { get; } | Sütunlar eşit aralıklı olduğunda sütunların genişliğini alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [SetCount](../../aspose.words/textcolumncollection/setcount/)(*int*) | Metni belirtilen sayıda metin sütununa düzenler. |

## Notlar

Kullanmak[`SetCount`](./setcount/) metin sütunlarının sayısını ayarlamak için.

Tüm sütunların eşit genişlikte ve eşit aralıklı olmasını sağlamak için şunu ayarlayın:[`EvenlySpaced`](./evenlyspaced/) ile`doğru` ve sütunlar arasındaki boşluk miktarını belirtin[`Spacing`](./spacing/). MS Word sütun genişliklerini otomatik olarak hesaplayacaktır.

Eğer varsa[`EvenlySpaced`](./evenlyspaced/) ayarlandı`YANLIŞ` , her sütunu için genişliği ve aralığı ayrı ayrı belirtmeniz gerekir. Ayrı ayrı erişmek için dizinleyiciyi kullanın[`TextColumn`](../textcolumn/) nesneler.

Özel sütun genişlikleri kullanırken, tüm sütun genişlikleri ve aralarındaki boşlukların toplamının sayfa genişliğinden sol ve sağ sayfa kenar boşluklarının çıkarılmasıyla elde edilen değere eşit olduğundan emin olun.

## Örnekler

Bir bölümde birden fazla eşit aralıklı sütunun nasıl oluşturulacağını gösterir.

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
