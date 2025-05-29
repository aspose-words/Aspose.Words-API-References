---
title: DocumentBase.Lists
linktitle: Lists
articleTitle: Lists
second_title: .NET için Aspose.Words
description: Verimli mülk yönetimi için DocumentBase Listelerini keşfedin. Belgenizin sunumunu ve netliğini geliştirmek için özelleştirilebilir liste biçimlendirmesine erişin.
type: docs
weight: 50
url: /tr/net/aspose.words/documentbase/lists/
---
## DocumentBase.Lists property

Belgede kullanılan liste biçimlendirmesine erişim sağlar.

```csharp
public ListCollection Lists { get; }
```

## Notlar

Daha fazla bilgi için açıklamayı inceleyin[`ListCollection`](../../../aspose.words.lists/listcollection/) sınıf.

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

### Ayrıca bakınız

* class [ListCollection](../../../aspose.words.lists/listcollection/)
* class [DocumentBase](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
