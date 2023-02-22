---
title: ListFormat.List
second_title: Aspose.Words for .NET API Referansı
description: ListFormat mülk. Bu paragrafın üyesi olduğu listeyi alır veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words.lists/listformat/list/
---
## ListFormat.List property

Bu paragrafın üyesi olduğu listeyi alır veya ayarlar.

```csharp
public List List { get; set; }
```

### Notlar

Bu özelliğe atanan liste, geçerli belgeye ait olmalıdır.

Bu özelliğe atanan liste, bir liste stili tanımı olmamalıdır.

Bu özelliğin null olarak ayarlanması, paragraf öğesinden madde işaretlerini ve numaralandırmayı kaldırır ve liste düzeyi numarasını sıfıra ayarlar. Bu özelliğin null olarak ayarlanması, çağrıya eşdeğer 'dir[`RemoveNumbers`](../removenumbers/).

### Örnekler

Bir listenin başka bir listenin içine nasıl yerleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Liste, önek sembolleri ve girintilerle paragraf kümelerini düzenlememize ve süslememize olanak tanır.
// Girinti seviyesini artırarak iç içe listeler oluşturabiliriz. 
// Bir belge oluşturucunun "ListFormat" özelliğini kullanarak bir listeyi başlatabilir ve bitirebiliriz. 
// Bir listenin başlangıcı ile bitişi arasına eklediğimiz her paragraf listede bir öğe haline gelecektir.
// Başlıklar için bir anahat listesi oluşturun.
List outlineList = doc.Lists.Add(ListTemplate.OutlineNumbers);
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 1");

// Numaralandırılmış bir liste oluşturun.
List numberedList = doc.Lists.Add(ListTemplate.NumberDefault);
builder.ListFormat.List = numberedList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Writeln("Numbered list item 1.");

// Liste içeren her paragraf bu bayrağa sahip olacaktır.
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

### Ayrıca bakınız

* class [List](../../list/)
* class [ListFormat](../)
* ad alanı [Aspose.Words.Lists](../../listformat/)
* toplantı [Aspose.Words](../../../)


