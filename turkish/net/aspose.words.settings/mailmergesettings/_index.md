---
title: MailMergeSettings Class
linktitle: MailMergeSettings
articleTitle: MailMergeSettings
second_title: Aspose.Words for .NET
description: Aspose.Words.Settings.MailMergeSettings sınıf. Bir belgeye ilişkin tüm adresmektup birleştirme bilgilerini belirtir C#'da.
type: docs
weight: 5850
url: /tr/net/aspose.words.settings/mailmergesettings/
---
## MailMergeSettings class

Bir belgeye ilişkin tüm adres-mektup birleştirme bilgilerini belirtir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Adres Mektup Birleştirme ve Raporlama](https://docs.aspose.com/words/net/mail-merge-and-reporting/) dokümantasyon makalesi.

```csharp
public class MailMergeSettings
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [MailMergeSettings](mailmergesettings/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [ActiveRecord](../../aspose.words.settings/mailmergesettings/activerecord/) { get; set; } | Microsoft Word'de görüntülenecek veri kaynağındaki kaydın tek tabanlı dizinini belirtir. Varsayılan değer 1. 'dir |
| [AddressFieldName](../../aspose.words.settings/mailmergesettings/addressfieldname/) { get; set; } | Veri kaynağı içindeki e-posta adreslerini içeren sütunu belirtir. Varsayılan değer boş bir dizedir. |
| [CheckErrors](../../aspose.words.settings/mailmergesettings/checkerrors/) { get; set; } | Adres-mektup birleştirme gerçekleştirilirken Microsoft Word tarafından gerçekleştirilecek hata raporlama türünü belirtir. Varsayılan değer:Default . |
| [ConnectString](../../aspose.words.settings/mailmergesettings/connectstring/) { get; set; } | Harici bir veri kaynağına bağlanmak için kullanılan bağlantı dizesini belirtir. Varsayılan değer boş bir dizedir. |
| [DataSource](../../aspose.words.settings/mailmergesettings/datasource/) { get; set; } | Adres-mektup birleştirme veri kaynağının yolunu belirtir. Varsayılan değer boş bir dizedir. |
| [DataType](../../aspose.words.settings/mailmergesettings/datatype/) { get; set; } | Adres-mektup birleştirme veri kaynağının türünü ve veri erişim yöntemini belirtir. Varsayılan değer:Default . |
| [Destination](../../aspose.words.settings/mailmergesettings/destination/) { get; set; } | Microsoft Word'ün adres-mektup birleştirmenin sonuçlarını nasıl çıkaracağını belirtir. Varsayılan değer:Default . |
| [DoNotSupressBlankLines](../../aspose.words.settings/mailmergesettings/donotsupressblanklines/) { get; set; } | Adres-mektup birleştirmeyi gerçekleştiren bir uygulamanın, birleştirilmiş belgelerde adres-mektup birleştirmeden kaynaklanan boş satırları nasıl işleyeceğini belirtir. Varsayılan değer:`YANLIŞ` . |
| [HeaderSource](../../aspose.words.settings/mailmergesettings/headersource/) { get; set; } | Adres-mektup birleştirme üstbilgi kaynağının yolunu belirtir. Varsayılan değer boş bir dizedir. |
| [LinkToQuery](../../aspose.words.settings/mailmergesettings/linktoquery/) { get; set; } | Bundan emin değilim. Microsoft Word Otomasyon Referansı, bunun, belgesi Microsoft Word'de her açıldığında sorgunun yürütüldüğünü belirttiğini öne sürüyor. Ancak OOXML spesifikasyonu, bunun, sorgunun gerçek sorguyu içeren harici bir sorgu dosyasına referans içerdiğini belirttiğini öne sürer. Varsayılan değer:`YANLIŞ` . |
| [MailAsAttachment](../../aspose.words.settings/mailmergesettings/mailasattachment/) { get; set; } | Adres-mektup birleştirme işlemi sırasında oluşturulan belgelerin gerçek e-postanın gövdesi yerine eki olarak e-postayla gönderilmesi gerektiğini belirtir. Varsayılan değer:`YANLIŞ` . |
| [MailSubject](../../aspose.words.settings/mailmergesettings/mailsubject/) { get; set; } | Adres-mektup birleştirme sırasında üretilen e-posta veya faksların konu satırında görünecek metni belirtir. Varsayılan değer boş bir dizedir. |
| [MainDocumentType](../../aspose.words.settings/mailmergesettings/maindocumenttype/) { get; set; } | Adres-mektup birleştirme ana belge türünü belirtir. Varsayılan değer:Default . |
| [Odso](../../aspose.words.settings/mailmergesettings/odso/) { get; set; } | Office Veri Kaynağı Nesnesi (ODSO) ayarlarını belirten nesneyi alır veya ayarlar. |
| [Query](../../aspose.words.settings/mailmergesettings/query/) { get; set; } | Adres mektup birleştirme işlemi gerçekleştirildiğinde belgeye aktarılacak kayıt kümesini döndürmek için belirtilen harici veri kaynağına karşı çalıştırılacak Yapılandırılmış Sorgu Dili dizesini içerir. Varsayılan değer boş bir dizedir. |
| [ViewMergedData](../../aspose.words.settings/mailmergesettings/viewmergeddata/) { get; set; } | Microsoft Word'ün, birleştirme alanlarının eklendiği belirtilen harici veri kaynağındaki verileri görüntüleyeceğini belirtir (örn. birleştirilmiş verilerin önizlemesi). Varsayılan değer:`YANLIŞ` . |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clear](../../aspose.words.settings/mailmergesettings/clear/)() | Adres-mektup birleştirme ayarlarını, belge kaydedildiğinde hiçbir adres-mektup birleştirme ayarı kaydedilmeyecek ve normal bir belge haline gelecek şekilde temizler. |
| [Clone](../../aspose.words.settings/mailmergesettings/clone/)() | Bu nesnenin derin bir kopyasını döndürür. |

## Notlar

Bu nesneyi bir belge için adres-mektup birleştirme veri kaynağı belirtmek için kullanabilirsiniz ve kullanıcı bu belgeyi açtığında bu information (mevcut veri alanlarıyla birlikte) Microsoft Word'de görünecektir. Veya bu nesneyi adres-mektup birleştirme ayarlarını sorgulamak için kullanabilirsiniz kullanıcının bu belge için Microsoft Word 'de belirttiği.

Normalde bu sınıfın nesnelerini doğrudan oluşturmanız gerekmez çünkü bir belgenin adres mektup birleştirme ayarları her zaman şu adresten kullanılabilir:[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) mülk.

Bu belgenin adres-mektup birleştirme ana belgesi olup olmadığını algılamak için değerini kontrol edin[`MainDocumentType`](./maindocumenttype/) mülk.

Adres-mektup birleştirme ayarlarını ve veri kaynağı bilgilerini bir belgeden kaldırmak için komutunu kullanabilirsiniz.[`Clear`](./clear/) yöntem. Aspose.Words, durumunda adres-mektup birleştirme ayarlarını bir belgeye yazmaz.[`MainDocumentType`](./maindocumenttype/) özellik şu şekilde ayarlandı:NotAMergeDocument veya[`DataType`](./datatype/) özellik şu şekilde ayarlandı:None.

Bu nesnenin özelliklerinin nasıl kullanılacağını öğrenmenin en iyi yolu, istenen veri kaynağına sahip bir belgeyi Microsoft Word'de manuel olarak oluşturmak ve ardından bu belgeyi Aspose.Words kullanarak açmak ve özelliklerini incelemektir.[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) Ve[`Odso`](./odso/) nesneler. Örneğin, bir veri kaynağını programlı olarak nasıl yapılandıracağınızı öğrenmek istiyorsanız bu, iyi bir yaklaşımdır.

Aspose.Words, belge 'yi yüklerken, kaydederken ve farklı formatlar arasında dönüştürürken adres-mektup birleştirme bilgilerini korur, ancak belgelerini farklı formatlar arasında dönüştürürken bu bilgiyi kullanmaz.[`MailMerge`](../../aspose.words.mailmerging/mailmerge/) nesne.

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
