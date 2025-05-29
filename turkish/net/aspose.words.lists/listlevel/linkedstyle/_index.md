---
title: ListLevel.LinkedStyle
linktitle: LinkedStyle
articleTitle: LinkedStyle
second_title: .NET için Aspose.Words
description: Listeleriniz için paragraf stillerini kolayca yönetmek ve özelleştirmek, belgenizin biçimlendirmesini ve okunabilirliğini geliştirmek için ListLevel LinkedStyle özelliğini keşfedin.
type: docs
weight: 60
url: /tr/net/aspose.words.lists/listlevel/linkedstyle/
---
## ListLevel.LinkedStyle property

Bu liste düzeyine bağlı olan paragraf stilini alır veya ayarlar.

```csharp
public Style LinkedStyle { get; set; }
```

## Notlar

Bu mülk`hükümsüz` liste düzeyi bir paragraf stiline bağlı olmadığında. Bu özellik şu şekilde ayarlanabilir:`hükümsüz`.

## Örnekler

Liste etiketlerini özelleştirmenin gelişmiş yollarını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir liste, paragraf kümelerini önek sembolleri ve girintilerle düzenlememize ve süslememize olanak tanır.
 // Girinti seviyesini artırarak iç içe listeler oluşturabiliriz.
 // Bir listeyi, bir belge oluşturucunun "ListFormat" özelliğini kullanarak başlatabilir ve sonlandırabiliriz.
// Bir listenin başlangıcı ile sonu arasına eklediğimiz her paragraf listede bir öğe haline gelecektir.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

// Seviye 1 etiketleri "Başlık 1" paragraf stiline göre biçimlendirilecek ve bir öneki olacak.
// Bunlar "Ek A", "Ek B" gibi gözükecektir...
list.ListLevels[0].NumberFormat = "Appendix \x0000";
list.ListLevels[0].NumberStyle = NumberStyle.UppercaseLetter;
list.ListLevels[0].LinkedStyle = doc.Styles["Heading 1"];

// Seviye 2 etiketleri, birinci ve ikinci liste seviyelerinin geçerli numaralarını görüntüler ve başlarında sıfırlar bulunur.
// Eğer ilk liste seviyesi 1 ise, bu listelerin liste etiketleri "Bölüm (1.01)", "Bölüm (1.02)" gibi görünecektir...
list.ListLevels[1].NumberFormat = "Section (\x0000.\x0001)";
list.ListLevels[1].NumberStyle = NumberStyle.LeadingZero;

// Daha üst düzeyin Büyük Harf numaralandırmasını kullandığını unutmayın.
// Daha üst liste seviyeleri için "IsLegal" özelliğini Arap rakamlarını kullanacak şekilde ayarlayabiliriz.
list.ListLevels[1].IsLegal = true;
list.ListLevels[1].RestartAfterLevel = 0;

// Seviye 3 etiketleri, önek ve sonek içeren büyük harfli Roma rakamları olacak ve her Liste seviyesi 1 öğesinde yeniden başlayacaktır.
// Bu liste etiketleri "-I-", "-II-"... şeklinde görünecektir.
list.ListLevels[2].NumberFormat = "-\x0002-";
list.ListLevels[2].NumberStyle = NumberStyle.UppercaseRoman;
list.ListLevels[2].RestartAfterLevel = 1;

// Tüm liste düzeylerinin etiketlerini kalın yap.
foreach (ListLevel level in list.ListLevels)
    level.Font.Bold = true;

// Liste biçimlendirmesini geçerli paragrafa uygula.
builder.ListFormat.List = list;

// Listemizin üç seviyesini de görüntüleyecek liste öğeleri oluşturun.
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

* class [Style](../../../aspose.words/style/)
* class [ListLevel](../)
* ad alanı [Aspose.Words.Lists](../../../aspose.words.lists/)
* toplantı [Aspose.Words](../../../)
