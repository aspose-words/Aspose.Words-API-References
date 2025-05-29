---
title: ListFormat.ListLevelNumber
linktitle: ListLevelNumber
articleTitle: ListLevelNumber
second_title: .NET için Aspose.Words
description: ListFormat ListLevelNumber özelliğini keşfedin, gelişmiş belge organizasyonu ve netlik için paragraf listesi düzeylerini 0'dan 8'e kadar kolayca yönetin.
type: docs
weight: 40
url: /tr/net/aspose.words.lists/listformat/listlevelnumber/
---
## ListFormat.ListLevelNumber property

Paragraf için liste düzeyi numarasını (0 ila 8) alır veya ayarlar.

```csharp
public int ListLevelNumber { get; set; }
```

## Notlar

Word belgelerinde listeler 0'dan 8'e kadar numaralandırılmış 1 veya 9 seviyeden oluşabilir.

Yalnızca şu durumlarda etkilidir:[`List`](../list/) özellik geçerli bir listeye referans verecek şekilde ayarlandı.

## Örnekler

Liste düzeyleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Bir liste, paragraf kümelerini önek sembolleri ve girintilerle düzenlememize ve süslememize olanak tanır.
 // Girinti seviyesini artırarak iç içe listeler oluşturabiliriz.
 // Bir listeyi, bir belge oluşturucunun "ListFormat" özelliğini kullanarak başlatabilir ve sonlandırabiliriz.
// Bir listenin başlangıcı ile sonu arasına eklediğimiz her paragraf listede bir öğe haline gelecektir.
// Aşağıda bir belge oluşturucu kullanarak oluşturabileceğimiz iki tür liste bulunmaktadır.
// 1 - Numaralandırılmış liste:
// Numaralandırılmış listeler, her bir öğeyi numaralandırarak paragrafları için mantıksal bir sıra oluşturur.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// "ListLevelNumber" özelliğini ayarlayarak liste düzeyini artırabiliriz
// geçerli liste öğesinde kendi kendine yeten bir alt liste başlatmak için.
// "NumberDefault" adlı Microsoft Word liste şablonu, ilk liste düzeyi için liste düzeyleri oluşturmak amacıyla sayıları kullanır.
 // Daha derin liste seviyelerinde harfler ve küçük harfli Roma rakamları kullanılır.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Madde işaretli liste:
// Bu liste her paragraftan önce bir girinti ve madde işareti ("•") uygulayacaktır.
// Bu listenin daha derin seviyelerinde "■" ve "○" gibi farklı semboller kullanılacaktır.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// "Liste" bayrağını kaldırarak, sonraki paragrafların liste olarak biçimlendirilmesini önlemek için liste biçimlendirmesini devre dışı bırakabiliriz.
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

Madde işaretli ve numaralı listelerin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Aspose.Words main advantages are:");

// Bir liste, paragraf kümelerini önek sembolleri ve girintilerle düzenlememize ve süslememize olanak tanır.
 // Girinti seviyesini artırarak iç içe listeler oluşturabiliriz.
 // Bir listeyi, bir belge oluşturucunun "ListFormat" özelliğini kullanarak başlatabilir ve sonlandırabiliriz.
// Bir listenin başlangıcı ile sonu arasına eklediğimiz her paragraf listede bir öğe haline gelecektir.
// Aşağıda bir belge oluşturucu ile oluşturabileceğimiz iki tür liste bulunmaktadır.
// 1 - Madde işaretli liste:
// Bu liste her paragraftan önce bir girinti ve madde işareti ("•") uygulayacaktır.
builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Great performance");
builder.Writeln("High reliability");
builder.Writeln("Quality code and working");
builder.Writeln("Wide variety of features");
builder.Writeln("Easy to understand API");

// Madde işaretli listeyi sonlandır.
builder.ListFormat.RemoveNumbers();

builder.InsertBreak(BreakType.ParagraphBreak);
builder.Writeln("Aspose.Words allows:");

// 2 - Numaralandırılmış liste:
// Numaralandırılmış listeler, her bir öğeyi numaralandırarak paragrafları için mantıksal bir sıra oluşturur.
builder.ListFormat.ApplyNumberDefault();

// Bu paragraf ilk maddedir. Numaralandırılmış bir listenin ilk maddesi, liste maddesi sembolü olarak "1." olacaktır.
builder.Writeln("Opening documents from different formats:");

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Mevcut liste düzeyini artırmak için "ListIndent" yöntemini çağırın,
// ilk liste seviyesinin geçerli öğesinde, daha derin bir girintiye sahip yeni bir kendi kendine yeten liste başlatacaktır.
builder.ListFormat.ListIndent();

Assert.AreEqual(1, builder.ListFormat.ListLevelNumber);

// Bunlar, bir sayım tutacak olan ikinci liste düzeyinin ilk üç liste öğesidir
// ilk liste seviyesinin sayısından bağımsız. Mevcut liste biçimine göre,
// "a.", "b." ve "c." sembolleri olacak.
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");

// Önceki liste düzeyine dönmek için "ListOutdent" metodunu çağırın.
builder.ListFormat.ListOutdent();

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Bu iki paragraf ilk liste seviyesinin sayımını sürdürecektir.
// Bu öğelerin sembolleri "2." ve "3." olacaktır.
builder.Writeln("Processing documents");
builder.Writeln("Saving documents in different formats:");

// Eğer liste seviyesini daha önce öğe eklediğimiz seviyeye çıkarırsak,
 // iç içe geçmiş liste bir öncekinden ayrı olacak ve numaralandırması baştan başlayacak.
// Bu liste öğeleri "a.", "b.", "c.", "d." ve "e" sembollerini içerecektir.
builder.ListFormat.ListIndent();
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");
builder.Writeln("MHTML");
builder.Writeln("Plain text");

// Liste düzeyini tekrar dışarı doğru girintileyin.
builder.ListFormat.ListOutdent();
builder.Writeln("Doing many other things!");

// Numaralandırılmış listeyi sonlandır.
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.ApplyDefaultBulletsAndNumbers.docx");
```

### Ayrıca bakınız

* class [ListFormat](../)
* ad alanı [Aspose.Words.Lists](../../../aspose.words.lists/)
* toplantı [Aspose.Words](../../../)
