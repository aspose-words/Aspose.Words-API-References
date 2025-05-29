---
title: Odso Class
linktitle: Odso
articleTitle: Odso
second_title: .NET için Aspose.Words
description: Sorunsuz posta birleştirme entegrasyonu için Aspose.Words.Settings.Odso sınıfını keşfedin. Verimli veri kaynağı yönetimi için ODSO ayarlarınızı optimize edin.
type: docs
weight: 6710
url: /tr/net/aspose.words.settings/odso/
---
## Odso class

Bir posta birleştirme veri kaynağı için Office Veri Kaynağı Nesnesi (ODSO) ayarlarını belirtir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Posta Birleştirme ve Raporlama](https://docs.aspose.com/words/net/mail-merge-and-reporting/) belgeleme makalesi.

```csharp
public class Odso
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [Odso](odso/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [ColumnDelimiter](../../aspose.words.settings/odso/columndelimiter/) { get; set; } | Harici veri kaynaklarındaki sütunları ayırmak için kullanılacak sütun sınırlayıcısı olarak yorumlanacak karakteri belirtir. Varsayılan değer 0'dır, yani tanımlı bir sütun sınırlayıcısı yoktur. |
| [DataSource](../../aspose.words.settings/odso/datasource/) { get; set; } | Posta birleştirmeyi gerçekleştirmek için bir belgeye bağlanacak harici veri kaynağının konumunu belirtir. Varsayılan değer boş bir dizedir. |
| [DataSourceType](../../aspose.words.settings/odso/datasourcetype/) { get; set; } | Bu posta birleştirme için ODSO bağlantı bilgilerinin bir parçası olarak bağlanılacak harici veri kaynağının türünü belirtir. Varsayılan değer:Default . |
| [FieldMapDatas](../../aspose.words.settings/odso/fieldmapdatas/) { get; set; } | Harici veri kaynağı 'den gelen sütunların belgedeki önceden tanımlanmış birleştirme alanı adlarına nasıl eşleneceğini belirten bir nesne koleksiyonunu alır veya ayarlar. Bu nesne asla`hükümsüz` . |
| [FirstRowContainsColumnNames](../../aspose.words.settings/odso/firstrowcontainscolumnnames/) { get; set; } | Bir barındırma uygulamasının belirtilen harici veri kaynağındaki ilk veri satırını, veri kaynağındaki her sütunun adını içeren bir başlık satırı olarak ele alacağını belirtir. Varsayılan değer şudur:`YANLIŞ` . |
| [RecipientDatas](../../aspose.words.settings/odso/recipientdatas/) { get; set; } | Posta birleştirme işleminde bireysel kayıtların dahil edilmesini/hariç tutulmasını belirten bir nesne koleksiyonunu alır veya ayarlar. Bu nesne hiçbir zaman`hükümsüz` . |
| [TableName](../../aspose.words.settings/odso/tablename/) { get; set; } | Bir kaynağın harici bir veri kaynağı içinde bağlanacağı belirli veri kümesini belirtir. Varsayılan değer boş bir dizedir. |
| [UdlConnectString](../../aspose.words.settings/odso/udlconnectstring/) { get; set; } | Harici bir veri kaynağına bağlanmak için kullanılan Evrensel Veri Bağlantısı (UDL) bağlantı dizesini belirtir. Varsayılan değer boş bir dizedir. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clone](../../aspose.words.settings/odso/clone/)() | Bu nesnenin derin bir klonunu döndürür. |

## Notlar

ODSO, daha yeni Microsoft Word sürümlerinin bir posta birleştirme belgesi için belirli türde veri kaynaklarını belirtirken kullanmayı tercih ettiği "yeni" yol gibi görünüyor. ODSO muhtemelen ilk olarak Microsoft Word 2000'de ortaya çıktı.

ODSO'nun kullanımı yetersiz bir şekilde belgelenmiştir ve bu nesnenin özelliklerinin nasıl kullanılacağını öğrenmenin en iyi yolu, Microsoft Word'de istenen veri kaynağıyla bir belgeyi elle oluşturmak ve ardından bu belgeyi Aspose.Words kullanarak açmak ve nesnenin özelliklerini incelemektir.[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) ve [`Odso`](../mailmergesettings/odso/)nesneler. Örneğin, bir veri kaynağını programlı olarak nasıl yapılandıracağınızı öğrenmek istiyorsanız, bu iyi bir yaklaşımdır.

Normalde bu sınıfın nesnelerini doğrudan oluşturmanız gerekmez çünkü ODSO settings her zaman şu şekilde kullanılabilir:[`Odso`](../mailmergesettings/odso/) mülk.

## Örnekler

Office Veri Kaynağı Nesnesi'ndeki verilerle bir posta birleştirmenin nasıl yürütüleceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");
builder.Writeln(": ");
builder.InsertField("MERGEFIELD Message", "<Message>");

// "|" karakterini kullanarak ASCII dosyası biçiminde bir veri kaynağı oluşturun
// sütunları ayıran ayırıcı olarak işlev görür. İlk satır üç sütunun adlarını içerir,
// ve her bir sonraki satır, kendi değerlerine sahip bir satırdır.
string[] lines = { "FirstName|LastName|Message",
    "John|Doe|Hello! This message was created with Aspose Words mail merge." };
string dataSrcFilename = ArtifactsDir + "MailMerge.MailMergeSettings.DataSource.txt";

File.WriteAllLines(dataSrcFilename, lines);

MailMergeSettings settings = doc.MailMergeSettings;
settings.MainDocumentType = MailMergeMainDocumentType.MailingLabels;
settings.CheckErrors = MailMergeCheckErrors.Simulate;
settings.DataType = MailMergeDataType.Native;
settings.DataSource = dataSrcFilename;
settings.Query = "SELECT * FROM " + doc.MailMergeSettings.DataSource;
settings.LinkToQuery = true;
settings.ViewMergedData = true;

Assert.AreEqual(MailMergeDestination.Default, settings.Destination);
Assert.False(settings.DoNotSupressBlankLines);

Odso odso = settings.Odso;
odso.DataSource = dataSrcFilename;
odso.DataSourceType = OdsoDataSourceType.Text;
odso.ColumnDelimiter = '|';
odso.FirstRowContainsColumnNames = true;

Assert.AreNotSame(odso, odso.Clone());
Assert.AreNotSame(settings, settings.Clone());

 // Bu belgeyi Microsoft Word'de açmak, içerikleri görüntülemeden önce posta birleştirme işlemini gerçekleştirecektir.
doc.Save(ArtifactsDir + "MailMerge.MailMergeSettings.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Settings](../../aspose.words.settings/)
* toplantı [Aspose.Words](../../)
