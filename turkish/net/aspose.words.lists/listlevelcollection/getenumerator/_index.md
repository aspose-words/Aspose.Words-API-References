---
title: ListLevelCollection.GetEnumerator
second_title: Aspose.Words for .NET API Referansı
description: ListLevelCollection yöntem. Bu listedeki düzeyleri numaralandıracak numaralandırıcı nesnesini alır.
type: docs
weight: 30
url: /tr/net/aspose.words.lists/listlevelcollection/getenumerator/
---
## ListLevelCollection.GetEnumerator method

Bu listedeki düzeyleri numaralandıracak numaralandırıcı nesnesini alır.

```csharp
public IEnumerator<ListLevel> GetEnumerator()
```

### Örnekler

Liste etiketlerini özelleştirmenin gelişmiş yollarını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Liste, paragraf kümelerini önek sembolleri ve girintilerle düzenlememize ve süslememize olanak tanır.
 // Girinti seviyesini artırarak iç içe listeler oluşturabiliriz.
 // Bir listeyi belge oluşturucunun "ListFormat" özelliğini kullanarak başlatabilir ve sonlandırabiliriz.
// Bir listenin başı ile sonu arasına eklediğimiz her paragraf, listede bir öğe haline gelecektir.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

// Düzey 1 etiketleri "Başlık 1" paragraf stiline göre biçimlendirilecek ve bir önek içerecektir.
// Bunlar "Ek A", "Ek B" gibi görünecek...
list.ListLevels[0].NumberFormat = "Appendix \x0000";
list.ListLevels[0].NumberStyle = NumberStyle.UppercaseLetter;
list.ListLevels[0].LinkedStyle = doc.Styles["Heading 1"];

// Seviye 2 etiketleri, birinci ve ikinci liste seviyelerinin mevcut numaralarını gösterecek ve başında sıfırlar bulunduracaktır.
// İlk liste seviyesi 1 ise, bunlardan gelen liste etiketleri "Bölüm (1.01)", "Bölüm (1.02)" gibi görünecektir...
list.ListLevels[1].NumberFormat = "Section (\x0000.\x0001)";
list.ListLevels[1].NumberStyle = NumberStyle.LeadingZero;

// Yüksek seviyenin Büyük Harf numaralandırmasını kullandığını unutmayın.
// "IsLegal" özelliğini daha yüksek liste seviyeleri için Arap rakamlarını kullanacak şekilde ayarlayabiliriz.
list.ListLevels[1].IsLegal = true;
list.ListLevels[1].RestartAfterLevel = 0;

// Düzey 3 etiketleri, bir önek ve bir sonek ile birlikte büyük harf Romen rakamları olacak ve her Liste düzeyi 1 öğesinde yeniden başlayacaktır.
// Bu liste etiketleri "-I-", "-II-" gibi görünecek...
list.ListLevels[2].NumberFormat = "-\x0002-";
list.ListLevels[2].NumberStyle = NumberStyle.UppercaseRoman;
list.ListLevels[2].RestartAfterLevel = 1;

// Tüm liste seviyelerinin etiketlerini kalın yapın.
foreach (ListLevel level in list.ListLevels)
    level.Font.Bold = true;

// Liste formatını geçerli paragrafa uygula.
builder.ListFormat.List = list;

// Liste seviyelerimizin üçünü de görüntüleyecek liste öğeleri oluşturun.
for (int n = 0; n < 2; n++)
{
    for (int i = 0; i < 3; i++)
    {
        builder.ListFormat.ListLevelNumber = i;
        builder.Writeln("Level " + i);
    }
}

builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.CreateListRestartAfterHigher.docx");
```

### Ayrıca bakınız

* class [ListLevel](../../listlevel/)
* class [ListLevelCollection](../)
* ad alanı [Aspose.Words.Lists](../../listlevelcollection/)
* toplantı [Aspose.Words](../../../)


