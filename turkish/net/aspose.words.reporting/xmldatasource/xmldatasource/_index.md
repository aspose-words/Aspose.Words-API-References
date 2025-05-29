---
title: XmlDataSource
linktitle: XmlDataSource
articleTitle: XmlDataSource
second_title: .NET için Aspose.Words
description: XmlDataSource oluşturucusu ile zahmetsizce güçlü bir veri kaynağı oluşturun ve sorunsuz entegrasyon için optimize edilmiş varsayılan seçenekleri kullanarak XML verilerini yükleyin.
type: docs
weight: 10
url: /tr/net/aspose.words.reporting/xmldatasource/xmldatasource/
---
## XmlDataSource(*string*) {#constructor_4}

XML veri yüklemesi için varsayılan seçenekleri kullanarak bir XML dosyasındaki verilerle yeni bir veri kaynağı oluşturur.

```csharp
public XmlDataSource(string xmlPath)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| xmlPath | String | Veri kaynağı olarak kullanılacak XML dosyasının yolu. |

## Örnekler

XML'in veri kaynağı (dize) olarak nasıl kullanılacağını gösterin.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

XmlDataSource dataSource = new XmlDataSource(MyDir + "List of people.xml");
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataString.docx");
```

### Ayrıca bakınız

* class [XmlDataSource](../)
* ad alanı [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../../)

---

## XmlDataSource(*Stream*) {#constructor}

XML veri yüklemesi için varsayılan seçenekleri kullanarak XML akışından gelen verilerle yeni bir veri kaynağı oluşturur.

```csharp
public XmlDataSource(Stream xmlStream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| xmlStream | Stream | Veri kaynağı olarak kullanılacak XML veri akışı. |

## Örnekler

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

* class [XmlDataSource](../)
* ad alanı [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../../)

---

## XmlDataSource(*string, string*) {#constructor_6}

XML Şema Tanımı dosyasını kullanarak bir XML dosyasındaki verilerle yeni bir veri kaynağı oluşturur. Varsayılan seçenekler XML veri yüklemesi için kullanılır.

```csharp
public XmlDataSource(string xmlPath, string xmlSchemaPath)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| xmlPath | String | Veri kaynağı olarak kullanılacak XML dosyasının yolu. |
| xmlSchemaPath | String | XML dosyası için şema sağlayan XML Şema Tanımı dosyasının yolu. |

### Ayrıca bakınız

* class [XmlDataSource](../)
* ad alanı [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, Stream*) {#constructor_2}

XML Şema Tanımı akışını kullanarak bir XML akışından gelen verilerle yeni bir veri kaynağı oluşturur. Varsayılan seçenekler XML veri yüklemesi için kullanılır.

```csharp
public XmlDataSource(Stream xmlStream, Stream xmlSchemaStream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| xmlStream | Stream | Veri kaynağı olarak kullanılacak XML veri akışı. |
| xmlSchemaStream | Stream | XML verilerine şema sağlayan XML Şema Tanımı akışı. |

### Ayrıca bakınız

* class [XmlDataSource](../)
* ad alanı [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../../)

---

## XmlDataSource(*string, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_5}

XML veri yüklemesi için belirtilen seçenekleri kullanarak bir XML dosyasındaki verilerle yeni bir veri kaynağı oluşturur.

```csharp
public XmlDataSource(string xmlPath, XmlDataLoadOptions options)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| xmlPath | String | Veri kaynağı olarak kullanılacak XML dosyasının yolu. |
| options | XmlDataLoadOptions | XML veri yükleme seçenekleri. |

### Ayrıca bakınız

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* ad alanı [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_1}

XML veri yüklemesi için belirtilen seçenekleri kullanarak XML akışından gelen verilerle yeni bir veri kaynağı oluşturur.

```csharp
public XmlDataSource(Stream xmlStream, XmlDataLoadOptions options)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| xmlStream | Stream | Veri kaynağı olarak kullanılacak XML veri akışı. |
| options | XmlDataLoadOptions | XML veri yükleme seçenekleri. |

### Ayrıca bakınız

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* ad alanı [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../../)

---

## XmlDataSource(*string, string, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_7}

XML Şema Tanımı dosyasını kullanarak bir XML dosyasından gelen verilerle yeni bir veri kaynağı oluşturur. Belirtilen seçenekleri XML veri yüklemesi için kullanılır.

```csharp
public XmlDataSource(string xmlPath, string xmlSchemaPath, XmlDataLoadOptions options)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| xmlPath | String | Veri kaynağı olarak kullanılacak XML dosyasının yolu. |
| xmlSchemaPath | String | XML dosyası için şema sağlayan XML Şema Tanımı dosyasının yolu. |
| options | XmlDataLoadOptions | XML veri yükleme seçenekleri. |

### Ayrıca bakınız

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* ad alanı [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, Stream, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_3}

XML Şema Tanımı akışını kullanarak bir XML akışından gelen verilerle yeni bir veri kaynağı oluşturur. Belirtilen seçenekleri XML veri yüklemesi için kullanılır.

```csharp
public XmlDataSource(Stream xmlStream, Stream xmlSchemaStream, XmlDataLoadOptions options)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| xmlStream | Stream | Veri kaynağı olarak kullanılacak XML veri akışı. |
| xmlSchemaStream | Stream | XML verilerine şema sağlayan XML Şema Tanımı akışı. |
| options | XmlDataLoadOptions | XML veri yükleme seçenekleri. |

### Ayrıca bakınız

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* ad alanı [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../../)
