---
title: ListFormat.List
linktitle: List
articleTitle: List
second_title: .NET için Aspose.Words
description: ListFormat ile belgenizin yapısını yönetin. Herhangi bir paragraf için listeyi kolayca alın veya ayarlayın, organizasyonu ve okunabilirliği artırın.
type: docs
weight: 20
url: /tr/net/aspose.words.lists/listformat/list/
---
## ListFormat.List property

Bu paragrafın üyesi olduğu listeyi alır veya ayarlar.

```csharp
public List List { get; set; }
```

## Notlar

Bu özelliğe atanacak listenin geçerli belgeye ait olması gerekir.

Bu özelliğe atanan liste bir liste stili tanımı olmamalıdır.

Bu özelliği şu şekilde ayarlayın:`hükümsüz` paragraph 'den madde işaretlerini ve numaralandırmayı kaldırır ve liste düzeyi numarasını sıfıra ayarlar. Bu özelliği şu şekilde ayarlar:`hükümsüz` çağrıya eşdeğerdir [`RemoveNumbers`](../removenumbers/).

## Örnekler

Bir listenin başka bir listenin içine nasıl yerleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir liste, paragraf kümelerini önek sembolleri ve girintilerle düzenlememize ve süslememize olanak tanır.
 // Girinti seviyesini artırarak iç içe listeler oluşturabiliriz.
 // Bir listeyi, bir belge oluşturucunun "ListFormat" özelliğini kullanarak başlatabilir ve sonlandırabiliriz.
// Bir listenin başlangıcı ile sonu arasına eklediğimiz her paragraf listede bir öğe haline gelecektir.
// Başlıklar için bir ana hat listesi oluşturun.
List outlineList = doc.Lists.Add(ListTemplate.OutlineNumbers);
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 1");

// Numaralandırılmış bir liste oluştur.
List numberedList = doc.Lists.Add(ListTemplate.NumberDefault);
builder.ListFormat.List = numberedList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Writeln("Numbered list item 1.");

// Liste oluşturan her paragraf bu bayrağa sahip olacaktır.
Assert.True(builder.CurrentParagraph.IsListItem);
Assert.True(builder.ParagraphFormat.IsListItem);

// Madde işaretli bir liste oluşturun.
List bulletedList = doc.Lists.Add(ListTemplate.BulletDefault);
builder.ListFormat.List = bulletedList;
builder.ParagraphFormat.LeftIndent = 72;
builder.Writeln("Bulleted list item 1.");
builder.Writeln("Bulleted list item 2.");
builder.ParagraphFormat.ClearFormatting();

// Numaralandırılmış listeye geri dön.
builder.ListFormat.List = numberedList;
builder.Writeln("Numbered list item 2.");
builder.Writeln("Numbered list item 3.");

// Anahat listesine geri dön.
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 2");

builder.ParagraphFormat.ClearFormatting();

builder.Document.Save(ArtifactsDir + "Lists.NestedLists.docx");
```

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

### Ayrıca bakınız

* class [List](../../list/)
* class [ListFormat](../)
* ad alanı [Aspose.Words.Lists](../../../aspose.words.lists/)
* toplantı [Aspose.Words](../../../)
