---
title: ListLevel.NumberFormat
linktitle: NumberFormat
articleTitle: NumberFormat
second_title: .NET için Aspose.Words
description: Listeleriniz için benzersiz sayı biçimlerini kolayca özelleştirmek ve ayarlamak, belgenizin netliğini ve stilini geliştirmek için ListLevel NumberFormat özelliğini keşfedin.
type: docs
weight: 70
url: /tr/net/aspose.words.lists/listlevel/numberformat/
---
## ListLevel.NumberFormat property

Liste düzeyi için sayı biçimini döndürür veya ayarlar.

```csharp
public string NumberFormat { get; set; }
```

## Notlar

Normal metin karakterleri arasında, dize, ilgili liste düzeylerindeki sayıları temsil eden \x0000 ila \x0008 yer tutucu karakterlerini içerebilir.

Örneğin, "\x0000.\x0001)" dizesi, "1.5)" gibi görünen bir label listesi üretecektir. "1" sayısı, 1. liste seviyesinden geçerli sayıdır, "5" sayısı ise 2. liste seviyesinden geçerli sayıdır.

Null kabul edilmez, ancak hiçbir sayının geçerli olmadığı anlamına gelen boş bir dize kabul edilir.

## Örnekler

DocumentBuilder kullanılırken paragraflara özel liste biçimlendirmesinin nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();

// Bir liste, paragraf kümelerini önek sembolleri ve girintilerle düzenlememize ve süslememize olanak tanır.
 // Girinti seviyesini artırarak iç içe listeler oluşturabiliriz.
 // Bir listeyi, bir belge oluşturucunun "ListFormat" özelliğini kullanarak başlatabilir ve sonlandırabiliriz.
// Bir listenin başlangıcı ile sonu arasına eklediğimiz her paragraf listede bir öğe haline gelecektir.
// Microsoft Word şablonundan bir liste oluşturun ve liste düzeylerinin ilk ikisini özelleştirin.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

ListLevel listLevel = list.ListLevels[0];
listLevel.Font.Color = Color.Red;
listLevel.Font.Size = 24;
listLevel.NumberStyle = NumberStyle.OrdinalText;
listLevel.StartAt = 21;
listLevel.NumberFormat = "\x0000";

listLevel.NumberPosition = -36;
listLevel.TextPosition = 144;
listLevel.TabPosition = 144;

listLevel = list.ListLevels[1];
listLevel.Alignment = ListLevelAlignment.Right;
listLevel.NumberStyle = NumberStyle.Bullet;
listLevel.Font.Name = "Wingdings";
listLevel.Font.Color = Color.Blue;
listLevel.Font.Size = 24;

// Bu NumberFormat değeri yıldız şeklinde madde işaretli liste sembolleri oluşturacaktır.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// Paragraflar oluşturun ve özel liste biçimlendirmemizin her iki liste düzeyini de bunlara uygulayın.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("The quick brown fox...");
builder.Writeln("The quick brown fox...");

builder.ListFormat.ListIndent();
builder.Writeln("jumped over the lazy dog.");
builder.Writeln("jumped over the lazy dog.");

builder.ListFormat.ListOutdent();
builder.Writeln("The quick brown fox...");

builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateCustomList.docx");
```

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

* class [ListLevel](../)
* ad alanı [Aspose.Words.Lists](../../../aspose.words.lists/)
* toplantı [Aspose.Words](../../../)
