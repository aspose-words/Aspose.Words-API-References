---
title: ListCollection.Add
linktitle: Add
articleTitle: Add
second_title: .NET için Aspose.Words
description: ListCollection Add yönteminin şablonlardan özel listeler oluşturarak belgenizin organizasyonunu ve verimliliğini nasıl artırdığını keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.lists/listcollection/add/
---
## Add(*[ListTemplate](../../listtemplate/)*) {#add}

Önceden tanımlanmış bir şablona dayalı yeni bir liste oluşturur ve bunu belgedeki liste koleksiyonuna ekler.

```csharp
public List Add(ListTemplate listTemplate)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| listTemplate | ListTemplate | Listenin şablonu. |

### Geri dönüş değeri

Yeni oluşturulan liste.

## Notlar

Aspose.Words liste şablonları, Microsoft Word 2003'teki Madde İşaretleri ve Numaralandırma iletişim kutusunda bulunan 21 liste şablonuna karşılık gelir.

Bu yöntemle oluşturulan tüm listeler 9 liste seviyesine sahiptir.

## Örnekler

Bir paragraf koleksiyonuna yeni bir liste biçimi uygulayarak bir listenin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1");
builder.Writeln("Paragraph 2");
builder.Write("Paragraph 3");

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

Assert.AreEqual(0, paras.Count(n => ((Paragraph)n).ListFormat.IsListItem));

List docList = doc.Lists.Add(ListTemplate.NumberUppercaseLetterDot);

foreach (Paragraph paragraph in paras.OfType<Paragraph>())
{
    paragraph.ListFormat.List = docList;
    paragraph.ListFormat.ListLevelNumber = 1;
}

Assert.AreEqual(3, paras.Count(n => ((Paragraph)n).ListFormat.IsListItem));
```

Bir listeyi kopyalayarak listede numaralandırmanın nasıl yeniden başlatılacağını gösterir.

```csharp
Document doc = new Document();

// Bir liste, paragraf kümelerini önek sembolleri ve girintilerle düzenlememize ve süslememize olanak tanır.
 // Girinti seviyesini artırarak iç içe listeler oluşturabiliriz.
 // Bir listeyi, bir belge oluşturucunun "ListFormat" özelliğini kullanarak başlatabilir ve sonlandırabiliriz.
// Bir listenin başlangıcı ile sonu arasına eklediğimiz her paragraf listede bir öğe haline gelecektir.
// Microsoft Word şablonundan bir liste oluşturun ve ilk liste düzeyini özelleştirin.
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// Listemizi bazı paragraflara uygulayalım.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("List 1 starts below:");
builder.ListFormat.List = list1;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// Mevcut bir listenin bir kopyasını belgenin liste koleksiyonuna ekleyebiliriz
// orijinalinde değişiklik yapmadan benzer bir liste oluşturmak.
List list2 = doc.Lists.AddCopy(list1);
list2.ListLevels[0].Font.Color = Color.Blue;
list2.ListLevels[0].StartAt = 10;

// İkinci listeyi yeni paragraflara uygula.
builder.Writeln("List 2 starts below:");
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.RestartNumberingUsingListCopy.docx");
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
* enum [ListTemplate](../../listtemplate/)
* class [ListCollection](../)
* ad alanı [Aspose.Words.Lists](../../../aspose.words.lists/)
* toplantı [Aspose.Words](../../../)

---

## Add(*[Style](../../../aspose.words/style/)*) {#add_1}

Bir liste stiline başvuran yeni bir liste oluşturur ve bunu belgedeki liste koleksiyonuna ekler.

```csharp
public List Add(Style listStyle)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| listStyle | Style | Liste stili. |

### Geri dönüş değeri

Yeni oluşturulan liste.

## Notlar

Yeni oluşturulan liste liste stiline başvurur. list stilinin özelliklerini değiştirirseniz, bu listenin özelliklerine yansır. Tam tersi, listenin properties stilini değiştirirseniz, bu liste stilinin özelliklerine yansır.

## Örnekler

Bir liste stilinin nasıl oluşturulacağını ve bir belgede nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();

// Bir liste, paragraf kümelerini önek sembolleri ve girintilerle düzenlememize ve süslememize olanak tanır.
 // Girinti seviyesini artırarak iç içe listeler oluşturabiliriz.
 // Bir listeyi, bir belge oluşturucunun "ListFormat" özelliğini kullanarak başlatabilir ve sonlandırabiliriz.
// Bir listenin başlangıcı ile sonu arasına eklediğimiz her paragraf listede bir öğe haline gelecektir.
// Bir stilin içerisinde bütün bir Liste nesnesini barındırabiliriz.
Style listStyle = doc.Styles.Add(StyleType.List, "MyListStyle");

List list1 = listStyle.List;

Assert.True(list1.IsListStyleDefinition);
Assert.False(list1.IsListStyleReference);
Assert.True(list1.IsMultiLevel);
Assert.AreEqual(listStyle, list1.Style);

// Listemizdeki tüm liste seviyelerinin görünümünü değiştirelim.
foreach (ListLevel level in list1.ListLevels)
{
    level.Font.Name = "Verdana";
    level.Font.Color = Color.Blue;
    level.Font.Bold = true;
}

DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Using list style first time:");

// Bir stil içindeki listeden başka bir liste oluştur.
List list2 = doc.Lists.Add(listStyle);

Assert.False(list2.IsListStyleDefinition);
Assert.True(list2.IsListStyleReference);
Assert.AreEqual(listStyle, list2.Style);

// Listemizin biçimlendireceği bazı liste öğelerini ekleyin.
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Writeln("Using list style second time:");

// Liste stiline göre başka bir liste oluştur ve uygula.
List list3 = doc.Lists.Add(listStyle);
builder.ListFormat.List = list3;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateAndUseListStyle.docx");
```

### Ayrıca bakınız

* class [List](../../list/)
* class [Style](../../../aspose.words/style/)
* class [ListCollection](../)
* ad alanı [Aspose.Words.Lists](../../../aspose.words.lists/)
* toplantı [Aspose.Words](../../../)
