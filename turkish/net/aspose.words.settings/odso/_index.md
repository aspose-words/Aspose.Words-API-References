---
title: Odso
second_title: Aspose.Words for .NET API Referansı
description: Adres mektup birleştirme veri kaynağı için Office Veri Kaynağı Nesnesi ODSO ayarlarını belirtir.
type: docs
weight: 5580
url: /tr/net/aspose.words.settings/odso/
---
## Odso class

Adres mektup birleştirme veri kaynağı için Office Veri Kaynağı Nesnesi (ODSO) ayarlarını belirtir.

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
| [ColumnDelimiter](../../aspose.words.settings/odso/columndelimiter/) { get; set; } | Harici veri kaynakları içindeki sütunları ayırmak için kullanılan sütun sınırlayıcı olarak yorumlanacak karakteri belirtir. Varsayılan değer 0'dır, yani tanımlanmış sütun sınırlayıcı yoktur. |
| [DataSource](../../aspose.words.settings/odso/datasource/) { get; set; } | Adres mektup birleştirme gerçekleştirmek için bir belgeye bağlanacak dış veri kaynağının konumunu belirtir. Varsayılan değer boş bir dizedir. |
| [DataSourceType](../../aspose.words.settings/odso/datasourcetype/) { get; set; } | Bu adres mektup birleştirme için ODSO bağlantı bilgilerinin bir parçası olarak bağlanılacak dış veri kaynağının türünü belirtir. Varsayılan değerDefault . |
| [FieldMapDatas](../../aspose.words.settings/odso/fieldmapdatas/) { get; set; } | harici veri kaynağından gelen sütunların belgedeki önceden tanımlanmış birleştirme alanı adlarıyla nasıl eşlendiğini belirten bir nesneler koleksiyonunu alır veya ayarlar. Bu nesne hiçbir zaman boş değildir. |
| [FirstRowContainsColumnNames](../../aspose.words.settings/odso/firstrowcontainscolumnnames/) { get; set; } | Bir barındırma uygulamasının, belirtilen harici data kaynağındaki ilk veri satırını, veri kaynağındaki her sütunun adlarını içeren bir başlık satırı olarak ele alacağını belirtir. Varsayılan değer`yanlış` . |
| [RecipientDatas](../../aspose.words.settings/odso/recipientdatas/) { get; set; } | Adres mektup birleştirmede tek tek kayıtların dahil edilmesini/hariç tutulmasını belirten bir nesneler koleksiyonunu alır veya ayarlar. Bu nesne hiçbir zaman boş değildir. |
| [TableName](../../aspose.words.settings/odso/tablename/) { get; set; } | Bir kaynağın harici bir veri kaynağı içinde bağlanacağı belirli veri kümesini belirtir. Varsayılan değer boş bir dizedir. |
| [UdlConnectString](../../aspose.words.settings/odso/udlconnectstring/) { get; set; } | Harici bir veri kaynağına bağlanmak için kullanılan Evrensel Veri Bağlantısı (UDL) bağlantı dizesini belirtir. Varsayılan değer boş bir dizedir. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clone](../../aspose.words.settings/odso/clone/)() | Bu nesnenin derin bir klonunu döndürür. |

### Notlar

ODSO, yeni Microsoft Word sürümlerinin adres mektup birleştirme belgesi için belirli veri kaynağı türlerini belirtirken kullanmayı tercih ettiği "yeni" yol gibi görünüyor. ODSO muhtemelen ilk olarak Microsoft Word 2000'de ortaya çıktı.

ODSO kullanımı yetersiz belgelenmiştir ve bu nesnesinin özelliklerinin nasıl kullanılacağını öğrenmenin en iyi yolu, istenen veri kaynağına sahip bir belgeyi Microsoft Word'de manuel olarak oluşturmak ve ardından bu belgeyi Aspose.Words kullanarak açmak ve özelliklerini incelemektir. arasında[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) ve [`Odso`](../mailmergesettings/odso/) nesneler. Örneğin, bir veri kaynağını programlı olarak nasıl yapılandıracağınızı öğrenmek istiyorsanız bu iyi bir yaklaşımdır.

ODSO settings aracılığıyla her zaman erişilebilir olduğundan, normalde bu sınıfın nesnelerini doğrudan oluşturmanız gerekmez.[`Odso`](../mailmergesettings/odso/) Emlak.

### Örnekler

Office Veri Kaynağı Nesnesindeki verilerle adres mektup birleştirmenin nasıl yürütüleceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");
builder.Writeln(": ");
builder.InsertField("MERGEFIELD Message", "<Message>");

// "|" ile ASCII dosyası biçiminde bir veri kaynağı oluşturun karakter
// sütunları ayıran sınırlayıcı görevi görür. İlk satır, üç sütunun adını içerir,
// ve sonraki her satır, kendi değerlerine sahip bir satırdır.
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

// Bu belgeyi Microsoft Word'de açmak, içeriği görüntülemeden önce adres mektup birleştirmeyi yürütecektir. 
doc.Save(ArtifactsDir + "MailMerge.MailMergeSettings.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Settings](../../aspose.words.settings/)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
