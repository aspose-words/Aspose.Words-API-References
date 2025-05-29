---
title: ListFormat.ApplyBulletDefault
linktitle: ApplyBulletDefault
articleTitle: ApplyBulletDefault
second_title: .NET için Aspose.Words
description: Belgelerinizde şık madde işaretli listeler oluşturmak, okunabilirliği ve düzeni artırmak için ApplyBulletDefault yöntemini nasıl kullanacağınızı keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words.lists/listformat/applybulletdefault/
---
## ListFormat.ApplyBulletDefault method

Yeni bir varsayılan madde işaretli liste başlatır ve bunu paragrafa uygular.

```csharp
public void ApplyBulletDefault()
```

## Notlar

Bu, varsayılan bulleted şablonunu kullanarak yeni bir liste oluşturan, bunu paragrafa uygulayan ve 1. liste düzeyini seçen bir kısayol yöntemidir.

## Örnekler

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
