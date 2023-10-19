---
title: Odso Class
linktitle: Odso
articleTitle: Odso
second_title: Aspose.Words for .NET
description: Aspose.Words.Settings.Odso sınıf. Adresmektup birleştirme veri kaynağı için Office Veri Kaynağı Nesnesi ODSO ayarlarını belirtir C#'da.
type: docs
weight: 5880
url: /tr/net/aspose.words.settings/odso/
---
## Odso class

Adres-mektup birleştirme veri kaynağı için Office Veri Kaynağı Nesnesi (ODSO) ayarlarını belirtir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Adres Mektup Birleştirme ve Raporlama](https://docs.aspose.com/words/net/mail-merge-and-reporting/) dokümantasyon makalesi.

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
| [ColumnDelimiter](../../aspose.words.settings/odso/columndelimiter/) { get; set; } | Harici veri kaynaklarındaki sütunları ayırmak için kullanılan sütun sınırlayıcı olarak yorumlanacak karakteri belirtir. Varsayılan değer 0'dır; bu, tanımlanmış bir sütun sınırlayıcı olmadığı anlamına gelir. |
| [DataSource](../../aspose.words.settings/odso/datasource/) { get; set; } | Adres-mektup birleştirmeyi gerçekleştirmek için bir belgeye bağlanacak harici veri kaynağının konumunu belirtir. Varsayılan değer boş bir dizedir. |
| [DataSourceType](../../aspose.words.settings/odso/datasourcetype/) { get; set; } | Bu adres-mektup birleştirme için ODSO bağlantı bilgilerinin bir parçası olarak bağlanılacak dış veri kaynağının türünü belirtir. Varsayılan değer:Default . |
| [FieldMapDatas](../../aspose.words.settings/odso/fieldmapdatas/) { get; set; } | Dış veri kaynağı 'deki sütunların belgedeki önceden tanımlanmış birleştirme alanı adlarıyla nasıl eşlendiğini belirten bir nesne koleksiyonunu alır veya ayarlar. Bu nesne hiçbir zaman`hükümsüz` . |
| [FirstRowContainsColumnNames](../../aspose.words.settings/odso/firstrowcontainscolumnnames/) { get; set; } | Bir barındırma uygulamasının, belirtilen harici data kaynağındaki ilk veri satırını, veri kaynağındaki her sütunun adlarını içeren bir başlık satırı olarak ele alacağını belirtir. Varsayılan değer:`YANLIŞ` . |
| [RecipientDatas](../../aspose.words.settings/odso/recipientdatas/) { get; set; } | Bireysel kayıtların adres-mektup birleştirmeye dahil edilmesini/hariç tutulmasını belirten bir nesne koleksiyonunu alır veya ayarlar. Bu nesne hiçbir zaman`hükümsüz` . |
| [TableName](../../aspose.words.settings/odso/tablename/) { get; set; } | Bir kaynağın harici bir veri kaynağı dahilinde bağlanacağı belirli veri kümesini belirtir. Varsayılan değer boş bir dizedir. |
| [UdlConnectString](../../aspose.words.settings/odso/udlconnectstring/) { get; set; } | Harici bir veri kaynağına bağlanmak için kullanılan Evrensel Veri Bağlantısı (UDL) bağlantı dizesini belirtir. Varsayılan değer boş bir dizedir. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clone](../../aspose.words.settings/odso/clone/)() | Bu nesnenin derin bir kopyasını döndürür. |

## Notlar

ODSO, daha yeni Microsoft Word sürümlerinin adres-mektup birleştirme belgesi için belirli veri kaynağı türlerini belirtirken kullanmayı tercih ettiği "yeni" yöntem gibi görünüyor. ODSO muhtemelen ilk olarak Microsoft Word 2000'de ortaya çıktı.

ODSO'nun kullanımı yeterince belgelenmemiştir ve bu nesnesinin özelliklerinin nasıl kullanılacağını öğrenmenin en iyi yolu Microsoft Word'de istenen veri kaynağına sahip bir belgeyi manuel olarak oluşturmak ve ardından bu belgeyi Aspose.Words kullanarak açmak ve özelliklerini incelemektir. arasında[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) ve [`Odso`](../mailmergesettings/odso/)nesneler. Örneğin, bir veri kaynağını programlı olarak nasıl yapılandıracağınızı öğrenmek istiyorsanız bu iyi bir yaklaşımdır.

ODSO settings dosyasına her zaman erişilebildiğinden normalde bu sınıfın nesnelerini doğrudan oluşturmanıza gerek yoktur.[`Odso`](../mailmergesettings/odso/) mülk.

## Örnekler

Bir Office Veri Kaynağı Nesnesinden alınan verilerle adres-mektup birleştirmenin nasıl yürütüleceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");
builder.Writeln(": ");
builder.InsertField("MERGEFIELD Message", "<Message>");

// ASCII dosyası biçiminde "|" işaretli bir veri kaynağı oluşturun karakter
// sütunları ayıran sınırlayıcı görevi görüyor. İlk satır üç sütunun adını içerir,
// ve sonraki her satır, ilgili değerlerin bulunduğu bir satırdır.
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

 // Bu belgeyi Microsoft Word'de açmak, içerikleri görüntülemeden önce adres-mektup birleştirme işlemini gerçekleştirecektir.
doc.Save(ArtifactsDir + "MailMerge.MailMergeSettings.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Settings](../../aspose.words.settings/)
* toplantı [Aspose.Words](../../)
