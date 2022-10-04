---
title: ListLevelNumber
second_title: Aspose.Words for .NET API Referansı
description: Paragraf için liste düzeyi numarasını 0 ila 8 alır veya ayarlar.
type: docs
weight: 40
url: /tr/net/aspose.words.lists/listformat/listlevelnumber/
---
## ListFormat.ListLevelNumber property

Paragraf için liste düzeyi numarasını (0 ila 8) alır veya ayarlar.

```csharp
public int ListLevelNumber { get; set; }
```

### Notlar

Word belgelerinde, listeler 0'dan 8'e kadar numaralandırılmış 1 veya 9 seviyeden oluşabilir.

Yalnızca şu durumlarda etkilidir:[`List`](../list/) özellik, geçerli bir listeye başvuracak şekilde ayarlandı.

### Örnekler

Liste seviyeleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Liste, önek sembolleri ve girintilerle paragraf kümelerini düzenlememize ve süslememize olanak tanır.
// Girinti seviyesini artırarak iç içe listeler oluşturabiliriz. 
// Bir belge oluşturucunun "ListFormat" özelliğini kullanarak bir listeyi başlatabilir ve bitirebiliriz. 
// Bir listenin başlangıcı ile bitişi arasına eklediğimiz her paragraf listede bir öğe haline gelecektir.
// Aşağıda, bir belge oluşturucu kullanarak oluşturabileceğimiz iki tür liste bulunmaktadır.
// 1 - Numaralandırılmış bir liste:
// Numaralandırılmış listeler, her bir öğeyi numaralandırarak paragrafları için mantıksal bir sıra oluşturur.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// "ListLevelNumber" özelliğini ayarlayarak liste seviyesini yükseltebiliriz
// geçerli liste öğesinde bağımsız bir alt liste başlatmak için.
// "NumberDefault" adlı Microsoft Word liste şablonu, ilk liste düzeyi için liste düzeyleri oluşturmak için sayıları kullanır.
// Daha derin liste seviyelerinde harfler ve küçük Romen rakamları kullanılır. 
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Madde işaretli bir liste:
// Bu liste, her paragraftan önce bir girinti ve bir madde işareti ("•") uygular.
// Bu listenin daha derin seviyelerinde "■" ve "○" gibi farklı semboller kullanılacaktır.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// "Liste" bayrağının ayarını kaldırarak, sonraki paragrafları liste olarak biçimlendirmemek için liste biçimlendirmesini devre dışı bırakabiliriz.
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

Madde işaretli ve numaralı listelerin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Aspose.Words main advantages are:");

// Liste, önek sembolleri ve girintilerle paragraf kümelerini düzenlememize ve süslememize olanak tanır.
// Girinti seviyesini artırarak iç içe listeler oluşturabiliriz. 
// Bir belge oluşturucunun "ListFormat" özelliğini kullanarak bir listeyi başlatabilir ve bitirebiliriz. 
// Bir listenin başlangıcı ile bitişi arasına eklediğimiz her paragraf listede bir öğe haline gelecektir.
// Aşağıda, bir belge oluşturucu ile oluşturabileceğimiz iki tür liste bulunmaktadır.
// 1 - Madde işaretli bir liste:
// Bu liste, her paragraftan önce bir girinti ve bir madde işareti ("•") uygular.
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

// 2 - Numaralandırılmış bir liste:
// Numaralandırılmış listeler, her bir öğeyi numaralandırarak paragrafları için mantıksal bir sıra oluşturur.
builder.ListFormat.ApplyNumberDefault();

// Bu paragraf ilk öğedir. Numaralandırılmış bir listenin ilk öğesi "1" olacaktır. liste öğesi sembolü olarak.
builder.Writeln("Opening documents from different formats:");

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Mevcut liste seviyesini yükseltmek için "ListIndent" yöntemini çağırın,
// bu, ilk liste seviyesinin geçerli öğesinde daha derin bir girintiye sahip yeni bir bağımsız liste başlatır.
builder.ListFormat.ListIndent();

Assert.AreEqual(1, builder.ListFormat.ListLevelNumber);

// Bunlar, ikinci liste seviyesinin ilk üç liste öğesidir ve bir sayımı sürdürür
// ilk liste seviyesinin sayısından bağımsız. Mevcut liste formatına göre,
// "a.", "b." ve "c." sembollerine sahip olacaklar.
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");

// Bir önceki liste düzeyine dönmek için "ListOutdent" yöntemini çağırın.
builder.ListFormat.ListOutdent();

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Bu iki paragraf ilk liste seviyesinin sayımına devam edecek.
// Bu öğeler "2." ve "3" sembollerine sahip olacaktır.
builder.Writeln("Processing documents");
builder.Writeln("Saving documents in different formats:");

// Liste seviyesini daha önce item eklediğimiz bir seviyeye çıkarırsak,
// iç içe geçmiş liste öncekinden ayrı olacak ve numaralandırması baştan başlayacak. 
// Bu liste öğeleri "a.", "b.", "c.", "d." ve "e" sembollerine sahip olacaktır.
builder.ListFormat.ListIndent();
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");
builder.Writeln("MHTML");
builder.Writeln("Plain text");

// Liste düzeyini tekrar girin.
builder.ListFormat.ListOutdent();
builder.Writeln("Doing many other things!");

// Numaralandırılmış listeyi sonlandır.
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.ApplyDefaultBulletsAndNumbers.docx");
```

### Ayrıca bakınız

* class [ListFormat](../)
* ad alanı [Aspose.Words.Lists](../../listformat/)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
