---
title: ListFormat.ApplyBulletDefault
linktitle: ApplyBulletDefault
articleTitle: ApplyBulletDefault
second_title: Aspose.Words for .NET
description: ListFormat ApplyBulletDefault yöntem. Yeni bir varsayılan madde işaretli liste başlatır ve bunu paragrafa uygular C#'da.
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

// Liste, paragraf kümelerini önek sembolleri ve girintilerle düzenlememize ve süslememize olanak tanır.
 // Girinti seviyesini artırarak iç içe listeler oluşturabiliriz.
 // Bir listeyi belge oluşturucunun "ListFormat" özelliğini kullanarak başlatabilir ve sonlandırabiliriz.
// Bir listenin başı ile sonu arasına eklediğimiz her paragraf, listede bir öğe haline gelecektir.
// Aşağıda belge oluşturucuyla oluşturabileceğimiz iki tür liste bulunmaktadır.
// 1 - Madde işaretli liste:
// Bu liste, her paragraftan önce bir girinti ve madde işareti simgesi ("•") uygulayacaktır.
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
// Numaralandırılmış listeler, her öğeyi numaralandırarak paragrafları için mantıksal bir düzen oluşturur.
builder.ListFormat.ApplyNumberDefault();

// Bu paragraf ilk öğedir. Numaralandırılmış bir listenin ilk öğesi "1" olacaktır. liste öğesi sembolü olarak.
builder.Writeln("Opening documents from different formats:");

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Geçerli liste düzeyini artırmak için "ListIndent" yöntemini çağırın,
// bu, ilk liste seviyesinin geçerli öğesinde daha derin bir girintiye sahip yeni bir bağımsız liste başlatacaktır.
builder.ListFormat.ListIndent();

Assert.AreEqual(1, builder.ListFormat.ListLevelNumber);

// Bunlar ikinci liste düzeyinin ilk üç liste öğesidir ve sayımı sürdürür
// ilk liste düzeyinin sayısından bağımsız. Mevcut liste formatına göre,
// "a.", "b." ve "c." simgelerine sahip olacaklar.
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");

// Önceki liste düzeyine dönmek için "ListOutdent" yöntemini çağırın.
builder.ListFormat.ListOutdent();

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Bu iki paragraf ilk liste düzeyinin sayımına devam edecek.
// Bu öğeler "2." ve "3" sembollerine sahip olacaktır.
builder.Writeln("Processing documents");
builder.Writeln("Saving documents in different formats:");

// Liste seviyesini daha önce öğe eklediğimiz seviyeye yükseltirsek,
 // iç içe geçmiş liste öncekinden ayrı olacak ve numaralandırması baştan başlayacak.
// Bu liste öğelerinde "a.", "b.", "c.", "d." ve "e" simgeleri bulunur.
builder.ListFormat.ListIndent();
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");
builder.Writeln("MHTML");
builder.Writeln("Plain text");

// Liste düzeyinin girintisini yeniden artırın.
builder.ListFormat.ListOutdent();
builder.Writeln("Doing many other things!");

//Numaralandırılmış listeyi sonlandırıyoruz.
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.ApplyDefaultBulletsAndNumbers.docx");
```

### Ayrıca bakınız

* class [ListFormat](../)
* ad alanı [Aspose.Words.Lists](../../../aspose.words.lists/)
* toplantı [Aspose.Words](../../../)
