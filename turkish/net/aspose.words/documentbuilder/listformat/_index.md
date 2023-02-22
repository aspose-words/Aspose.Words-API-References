---
title: DocumentBuilder.ListFormat
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder mülk. Geçerli liste biçimlendirme özelliklerini temsil eden bir nesne döndürür.
type: docs
weight: 130
url: /tr/net/aspose.words/documentbuilder/listformat/
---
## DocumentBuilder.ListFormat property

Geçerli liste biçimlendirme özelliklerini temsil eden bir nesne döndürür.

```csharp
public ListFormat ListFormat { get; }
```

### Örnekler

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

* class [ListFormat](../../../aspose.words.lists/listformat/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)


