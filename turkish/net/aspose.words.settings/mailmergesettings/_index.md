---
title: MailMergeSettings
second_title: Aspose.Words for .NET API Referansı
description: Bir belge için tüm adres mektup birleştirme bilgilerini belirtir.
type: docs
weight: 5550
url: /tr/net/aspose.words.settings/mailmergesettings/
---
## MailMergeSettings class

Bir belge için tüm adres mektup birleştirme bilgilerini belirtir.

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
| [ActiveRecord](../../aspose.words.settings/mailmergesettings/activerecord/) { get; set; } | Microsoft Word'de görüntülenecek olan veri kaynağından kaydın tek tabanlı dizinini belirtir. Varsayılan değer 1. 'dir |
| [AddressFieldName](../../aspose.words.settings/mailmergesettings/addressfieldname/) { get; set; } | Veri kaynağındaki e-posta adreslerini içeren sütunu belirtir. Varsayılan değer boş bir dizedir. |
| [CheckErrors](../../aspose.words.settings/mailmergesettings/checkerrors/) { get; set; } | Adres mektup birleştirme gerçekleştirirken Microsoft Word tarafından yürütülecek hata raporlama türünü belirtir. Varsayılan değerDefault . |
| [ConnectString](../../aspose.words.settings/mailmergesettings/connectstring/) { get; set; } | Bir dış veri kaynağına bağlanmak için kullanılan bağlantı dizesini belirtir. Varsayılan değer boş bir dizedir. |
| [DataSource](../../aspose.words.settings/mailmergesettings/datasource/) { get; set; } | Adres mektup birleştirme veri kaynağının yolunu belirtir. Varsayılan değer boş bir dizedir. |
| [DataType](../../aspose.words.settings/mailmergesettings/datatype/) { get; set; } | Adres mektup birleştirme veri kaynağının türünü ve veri erişim yöntemini belirtir. Varsayılan değerDefault . |
| [Destination](../../aspose.words.settings/mailmergesettings/destination/) { get; set; } | Microsoft Word'ün adres mektup birleştirme sonuçlarının nasıl çıktısını alacağını belirtir. Varsayılan değerDefault . |
| [DoNotSupressBlankLines](../../aspose.words.settings/mailmergesettings/donotsupressblanklines/) { get; set; } | Adres mektup birleştirme gerçekleştiren bir uygulamanın, birleştirilmiş belgelerde adres mektup birleştirmeden kaynaklanan boş satırları nasıl işleyeceğini belirtir. Varsayılan değer`yanlış` . |
| [HeaderSource](../../aspose.words.settings/mailmergesettings/headersource/) { get; set; } | Adres mektup birleştirme üstbilgi kaynağının yolunu belirtir. Varsayılan değer boş bir dizedir. |
| [LinkToQuery](../../aspose.words.settings/mailmergesettings/linktoquery/) { get; set; } | Bundan emin değilim. Microsoft Word Otomasyon Referansı, bunun sorgunun belgesi Microsoft Word'de her açıldığında yürütüldüğünü belirttiğini belirtir. Ancak OOXML belirtimi, bunun, sorgunun gerçek sorguyu içeren harici bir sorgu dosyasına referans içerdiğini belirttiğini belirtir. Varsayılan değer`yanlış` . |
| [MailAsAttachment](../../aspose.words.settings/mailmergesettings/mailasattachment/) { get; set; } | Adres mektup birleştirme işlemi sırasında üretilen belgelerin, asıl e-postanın gövdesi yerine eki olarak e-postayla gönderilmesi gerektiğini belirtir. Varsayılan değer`yanlış` . |
| [MailSubject](../../aspose.words.settings/mailmergesettings/mailsubject/) { get; set; } | Adres mektup birleştirme sırasında üretilen e-postaların veya faksların konu satırında görünecek metni belirtir. Varsayılan değer boş bir dizedir. |
| [MainDocumentType](../../aspose.words.settings/mailmergesettings/maindocumenttype/) { get; set; } | Adres mektup birleştirme ana belge türünü belirtir. Varsayılan değerDefault . |
| [Odso](../../aspose.words.settings/mailmergesettings/odso/) { get; set; } | Office Veri Kaynağı Nesnesi (ODSO) ayarlarını belirten nesneyi alır veya ayarlar. |
| [Query](../../aspose.words.settings/mailmergesettings/query/) { get; set; } | Adres mektup birleştirme işlemi gerçekleştirildiğinde belgeye aktarılacak kayıt kümesini döndürmek için belirtilen harici veri kaynağına karşı çalıştırılacak Yapılandırılmış Sorgu Dili dizesini içerir. Varsayılan değer boş bir dizedir. |
| [ViewMergedData](../../aspose.words.settings/mailmergesettings/viewmergeddata/) { get; set; } | Microsoft Word'ün, birleştirme alanlarının eklendiği belirtilen harici veri kaynağından gelen verileri görüntüleyeceğini belirtir (örneğin, birleştirilmiş verileri önizleme). Varsayılan değer`yanlış` . |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Clear](../../aspose.words.settings/mailmergesettings/clear/)() | Adres mektup birleştirme ayarlarını, belge kaydedildiğinde hiçbir adres mektup birleştirme ayarı kaydedilmeyecek ve normal bir belge haline gelecek şekilde temizler. |
| [Clone](../../aspose.words.settings/mailmergesettings/clone/)() | Bu nesnenin derin bir klonunu döndürür. |

### Notlar

Bir belge için adres mektup birleştirme veri kaynağı belirtmek için bu nesneyi kullanabilirsiniz ve bu bilgi (kullanılabilir veri alanlarıyla birlikte) kullanıcı bu belgeyi açtığında Microsoft Word'de görünecektir. Veya bu nesneyi adres mektup birleştirme ayarlarını sorgulamak için kullanabilirsiniz. kullanıcının bu belge için Microsoft Word içinde belirttiği.

Bir belgenin Adres mektup birleştirme ayarları her zaman[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) Emlak.

Bu belgenin adres mektup birleştirme ana belgesi olup olmadığını saptamak için değerini kontrol edin.[`MainDocumentType`](./maindocumenttype/) Emlak.

Adres mektup birleştirme ayarlarını ve veri kaynağı bilgilerini bir belgeden kaldırmak için [`Clear`](./clear/) yöntem. Aspose.Words adres mektup birleştirme ayarlarını bir belgeye [`MainDocumentType`](./maindocumenttype/) özellik olarak ayarlandıNotAMergeDocument veya[`DataType`](./datatype/) özellik olarak ayarlandıNone.

Bu nesnenin özelliklerinin nasıl kullanılacağını öğrenmenin en iyi yolu, istenen veri kaynağına sahip bir belgeyi Microsoft Word'de manuel olarak oluşturmak ve ardından bu belgeyi Aspose.Words kullanarak açmak ve o belgenin özelliklerini incelemektir.[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/) ve[`Odso`](./odso/) nesneler. Örneğin, bir veri kaynağını programlı olarak nasıl yapılandıracağınızı öğrenmek istiyorsanız, bu iyi bir yaklaşımdır.

Aspose.Words, belgeler 'yi farklı biçimler arasında yüklerken, kaydederken ve dönüştürürken adres mektup birleştirme bilgilerini korur, ancak[`MailMerge`](../../aspose.words.mailmerging/mailmerge/) nesne.

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
