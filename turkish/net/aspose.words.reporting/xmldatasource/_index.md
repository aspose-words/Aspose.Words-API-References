---
title: XmlDataSource Class
linktitle: XmlDataSource
articleTitle: XmlDataSource
second_title: .NET için Aspose.Words
description: Aspose.Words.XmlDataSource ile güçlü raporlamanın kilidini açın. Raporlarınıza sorunsuz entegrasyon için XML verilerine kolayca erişin ve veri görselleştirmesini geliştirin.
type: docs
weight: 5490
url: /tr/net/aspose.words.reporting/xmldatasource/
---
## XmlDataSource class

Bir rapor içerisinde kullanılacak bir XML dosyasının veya akışının verilerine erişim sağlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[LINQ Raporlama Motoru](https://docs.aspose.com/words/net/linq-reporting-engine/) belgeleme makalesi.

```csharp
public class XmlDataSource
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [XmlDataSource](xmldatasource/#constructor)(*Stream*) | XML veri yüklemesi için varsayılan seçenekleri kullanarak XML akışından gelen verilerle yeni bir veri kaynağı oluşturur. |
| [XmlDataSource](xmldatasource/#constructor_4)(*string*) | XML veri yüklemesi için varsayılan seçenekleri kullanarak bir XML dosyasındaki verilerle yeni bir veri kaynağı oluşturur. |
| [XmlDataSource](xmldatasource/#constructor_2)(*Stream, Stream*) | XML Şema Tanımı akışını kullanarak bir XML akışından gelen verilerle yeni bir veri kaynağı oluşturur. Varsayılan seçenekler XML veri yüklemesi için kullanılır. |
| [XmlDataSource](xmldatasource/#constructor_1)(*Stream, [XmlDataLoadOptions](../xmldataloadoptions/)*) | XML veri yüklemesi için belirtilen seçenekleri kullanarak XML akışından gelen verilerle yeni bir veri kaynağı oluşturur. |
| [XmlDataSource](xmldatasource/#constructor_6)(*string, string*) | XML Şema Tanımı dosyasını kullanarak bir XML dosyasındaki verilerle yeni bir veri kaynağı oluşturur. Varsayılan seçenekler XML veri yüklemesi için kullanılır. |
| [XmlDataSource](xmldatasource/#constructor_5)(*string, [XmlDataLoadOptions](../xmldataloadoptions/)*) | XML veri yüklemesi için belirtilen seçenekleri kullanarak bir XML dosyasındaki verilerle yeni bir veri kaynağı oluşturur. |
| [XmlDataSource](xmldatasource/#constructor_3)(*Stream, Stream, [XmlDataLoadOptions](../xmldataloadoptions/)*) | XML Şema Tanımı akışını kullanarak bir XML akışından gelen verilerle yeni bir veri kaynağı oluşturur. Belirtilen seçenekleri XML veri yüklemesi için kullanılır. |
| [XmlDataSource](xmldatasource/#constructor_7)(*string, string, [XmlDataLoadOptions](../xmldataloadoptions/)*) | XML Şema Tanımı dosyasını kullanarak bir XML dosyasından gelen verilerle yeni bir veri kaynağı oluşturur. Belirtilen seçenekleri XML veri yüklemesi için kullanılır. |

## Notlar

Bir rapor oluştururken ilgili dosyanın veya akışın verilerine erişmek için, bu sınıfın bir örneğini bir veri kaynağı olarak aşağıdakilere geçirin:[`ReportingEngine`](../reportingengine/) .BuildReport aşırı yüklemeleri.

Şablon belgelerinde, en üst düzey XML öğesi yalnızca aynı türdeki öğelerin bir listesini içeriyorsa, `XmlDataSource` örnek, bir örnekmiş gibi ele alınmalıdırDataTable örneği. Aksi takdirde, bir`XmlDataSource` örnek, bir örnekmiş gibi ele alınmalıdırDataRow örneği. Daha fazla bilgi için şablon sözdizimi başvurusu 'ye bakın (https://docs.aspose.com/display/wordsnet/Template+Syntax).

XML Şema Tanımı bu sınıfın bir kurucusuna geçirildiğinde, basit XML öğelerinin değerlerinin veri türleri ve öznitelikler şemaya göre belirlenir. Bu nedenle şablon belgelerinde, sadece dizeler yerine yazılmış değerlerle çalışabilirsiniz.

XML Şema Tanımı bu sınıfın bir oluşturucusuna geçirilmediğinde, basit XML öğelerinin ve özniteliklerinin değerlerinin veri türleri, dize gösterimlerine göre otomatik olarak belirlenir. Bu nedenle şablon belgelerinde, bu durumda da yazılmış değerlerle çalışabilirsiniz. Motor, aşağıdaki türlerin değerlerini otomatik olarak tanıyabilir:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Veri türlerinin otomatik olarak tanınması için, basit XML öğelerinin ve özniteliklerinin değerlerinin dize gösterimlerinin değişmez kültür ayarları kullanılarak oluşturulması gerektiğini unutmayın.

XML veri yüklemesinin varsayılan davranışını geçersiz kılmak için bir[`XmlDataLoadOptions`](../xmldataloadoptions/) örneği bu sınıfın bir kurucusuna.

## Örnekler

XML'in veri kaynağı (dize) olarak nasıl kullanılacağını gösterin.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

XmlDataSource dataSource = new XmlDataSource(MyDir + "List of people.xml");
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataString.docx");
```

XML'in veri kaynağı (akış) olarak nasıl kullanılacağını gösterin.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

using (FileStream stream = File.OpenRead(MyDir + "List of people.xml"))
{
    XmlDataSource dataSource = new XmlDataSource(stream);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataStream.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Reporting](../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../)
