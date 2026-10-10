---
title: "ReportingEngine"
linktitle: "ReportingEngine"
second_title: "Aspose.Words Java için"
description: "Java'da bu rutinleri kontrol etmek için bir dizi ayar ve veri ile şablon belgelerini doldurmak için rutinler sağlar."
type: docs
weight: 574
url: /tr/java/com.aspose.words/reportingengine/
---

**Inheritance:**
java.lang.Object
```
public class ReportingEngine
```

Şablon belgelerini veri ile doldurmak için rutinler ve bu rutinleri kontrol eden bir dizi ayar sağlar.

Daha fazla bilgi için, [ LINQ Reporting Engine ][LINQ Reporting Engine] dokümantasyon makalesini ziyaret edin.


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [ReportingEngine()](#ReportingEngine) | Bu sınıfın yeni bir örneğini başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [buildReport(Document document, Object dataSource)](#buildReport-com.aspose.words.Document-java.lang.Object) | Belirtilen şablon belgesini, belirtilen kaynaktan gelen veriyle doldurarak hazır bir rapor haline getirir. |
| [buildReport(Document document, Object dataSource, String dataSourceName)](#buildReport-com.aspose.words.Document-java.lang.Object-java.lang.String) | Belirtilen şablon belgesini, belirtilen kaynaktan gelen veriyle doldurarak hazır bir rapor haline getirir. |
| [buildReport(Document document, Object[] dataSources, String[] dataSourceNames)](#buildReport-com.aspose.words.Document-java.lang.Object---java.lang.String) | Belirtilen şablon belgesini, belirtilen kaynaklardan gelen veriyle doldurarak hazır bir rapor haline getirir. |
| [equals(Object obj)](#equals-java.lang.Object) |  |
| [getKnownTypes()](#getKnownTypes) | Sırasız bir küme alır (örn. |
| [getMissingMemberMessage()](#getMissingMemberMessage) | Eksik bir nesne üyesine basit bir referans temsil eden şablon ifadesi yerine yazdırılan bir dize değeri alır. |
| [getOptions()](#getOptions) | Bir rapor oluşturulurken bu [ReportingEngine](../../com.aspose.words/reportingengine/) örneğinin davranışını kontrol eden bayrakların bir kümesini alır. |
| [getRestrictedTypes()](#getRestrictedTypes) | Motorun şablon sözdizimi aracılığıyla erişememesi gereken türleri, bu türlerin üyelerini ve türetilmiş türlerin üyelerini döndürür. |
| [getUseReflectionOptimization()](#getUseReflectionOptimization) | Yansıma API'si aracılığıyla gerçekleştirilen özel tür üyelerinin çağrılarının dinamik sınıf oluşturma kullanılarak optimize edilip edilmediğini gösteren bir değeri alır. |
| [hashCode()](#hashCode) |  |
| [setMissingMemberMessage(String value)](#setMissingMemberMessage-java.lang.String) | Eksik bir nesne üyesine basit bir referans temsil eden şablon ifadesi yerine yazdırılan bir dize değeri ayarlar. |
| [setOptions(int value)](#setOptions-int) | Bir rapor oluşturulurken bu [ReportingEngine](../../com.aspose.words/reportingengine/) örneğinin davranışını kontrol eden bayrakların bir kümesini ayarlar. |
| [setRestrictedTypes(Class[] types)](#setRestrictedTypes-java.lang.Class...) | Motorun şablon sözdizimi aracılığıyla erişememesi gereken türleri, bu türlerin üyelerini ve türetilmiş türlerin üyelerini belirtir. |
| [setUseReflectionOptimization(boolean value)](#setUseReflectionOptimization-boolean) | Yansıma API'si aracılığıyla gerçekleştirilen özel tür üyelerinin çağrılarının dinamik sınıf oluşturma kullanılarak optimize edilip edilmediğini gösteren bir değeri ayarlar. |
### ReportingEngine() {#ReportingEngine}
```
public ReportingEngine()
```


Bu sınıfın yeni bir örneğini başlatır.

### buildReport(Document document, Object dataSource) {#buildReport-com.aspose.words.Document-java.lang.Object}
```
public boolean buildReport(Document document, Object dataSource)
```


Belirtilen şablon belgesini, belirtilen kaynaktan gelen veriyle doldurarak hazır bir rapor haline getirir.

 **Remarks:** 

Bu aşırı yüklemeyi kullanarak şablon belgesinde veri kaynağının üyelerine başvurabilirsiniz, ancak veri kaynağı nesnesine doğrudan başvuramazsınız. Bunu başarmak için [buildReport(com.aspose.words.Document, java.lang.Object, java.lang.String)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object--java.lang.String) aşırı yüklemesini kullanmalısınız.

Bir veri kaynağı nesnesi aşağıdaki türlerden biri olabilir:

 *  [XmlDataSource](../../com.aspose.words/xmldatasource/)
 *  [JsonDataSource](../../com.aspose.words/jsondatasource/)
 *  [CsvDataSource](../../com.aspose.words/csvdatasource/)
 *  [DataSet](../../com.aspose.words.net.system.data/dataset/)
 *  [DataTable](../../com.aspose.words.net.system.data/datatable/)
 *  [DataRow](../../com.aspose.words.net.system.data/datarow/)
 *  [IDataReader](../../com.aspose.words.net.system.data/idatareader/)
 *  [IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
 *  [DataView](../../com.aspose.words.net.system.data/dataview/)
 *  [DataRowView](../../com.aspose.words.net.system.data/datarowview/)
 *  Any other arbitrary Java type

Şablon belgelerinde farklı türde veri kaynaklarıyla nasıl çalışılacağına ilişkin bilgi için şablon sözdizimi referansına bakın (https://docs.aspose.com/display/wordsjava/Template+Syntax).

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | Veri ile doldurulacak bir şablon belgesi. |
| dataSource | java.lang.Object | Bir veri kaynağı nesnesi. |

**Returns:**
boolean - Şablon belgesinin ayrıştırılmasının başarılı olup olmadığını gösteren bir bayrak. Döndürülen bayrak yalnızca [getOptions()](../../com.aspose.words/reportingengine/\#getOptions) / [setOptions(int)](../../com.aspose.words/reportingengine/\#setOptions-int) özelliğinin değeri [ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions/\#INLINE-ERROR-MESSAGES) seçeneğini içeriyorsa anlamlıdır.
### buildReport(Document document, Object dataSource, String dataSourceName) {#buildReport-com.aspose.words.Document-java.lang.Object-java.lang.String}
```
public boolean buildReport(Document document, Object dataSource, String dataSourceName)
```


Belirtilen şablon belgesini, belirtilen kaynaktan gelen veriyle doldurarak hazır bir rapor haline getirir.

 **Remarks:** 

Bu aşırı yüklemeyi kullanarak şablonda veri kaynağının üyelerine ve veri kaynağı nesnesine başvurabilirsiniz. Veri kaynağı nesnesine başvurmayacaksanız, dataSourceName'i atlayıp null geçebilir veya [buildReport(com.aspose.words.Document, java.lang.Object)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object) aşırı yüklemesini kullanabilirsiniz.

Bir veri kaynağı nesnesi aşağıdaki türlerden biri olabilir:

 *  [XmlDataSource](../../com.aspose.words/xmldatasource/)
 *  [JsonDataSource](../../com.aspose.words/jsondatasource/)
 *  [CsvDataSource](../../com.aspose.words/csvdatasource/)
 *  [DataSet](../../com.aspose.words.net.system.data/dataset/)
 *  [DataTable](../../com.aspose.words.net.system.data/datatable/)
 *  [DataRow](../../com.aspose.words.net.system.data/datarow/)
 *  [IDataReader](../../com.aspose.words.net.system.data/idatareader/)
 *  [IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
 *  [DataView](../../com.aspose.words.net.system.data/dataview/)
 *  [DataRowView](../../com.aspose.words.net.system.data/datarowview/)
 *  Any other arbitrary Java type

Şablon belgelerinde farklı türde veri kaynaklarıyla nasıl çalışılacağına ilişkin bilgi için şablon sözdizimi referansına bakın (https://docs.aspose.com/display/wordsjava/Template+Syntax).

 **Examples:** 

Eksik üyelerin nasıl izin verileceğini gösterir.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

Değerlerin dolar metni olarak nasıl görüntüleneceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("<<[ds.getValue1()]:dollarText>>\r<<[ds.getValue2()]:dollarText>>");

 NumericTestClass testData = new NumericTestBuilder().withValues(1234, 5621718.589).build();

 ReportingEngine report = new ReportingEngine();
 report.getKnownTypes().add(NumericTestClass.class);
 report.buildReport(doc, testData, "ds");

 doc.save(getArtifactsDir() + "ReportingEngine.DollarTextFormat.docx");
 
```

Paragrafların seçici olarak nasıl kaldırılacağını gösterir.

```

 // Template contains tags with an exclamation mark. For such tags, empty paragraphs will be removed.
 Document doc = new Document(getMyDir() + "Reporting engine template - Selective remove paragraphs.docx");

 ReportingEngine engine = new ReportingEngine();
 engine.buildReport(doc, false, "value");

 doc.save(getArtifactsDir() + "ReportingEngine.SelectiveDeletionOfParagraphs.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | Veri ile doldurulacak bir şablon belgesi. |
| dataSource | java.lang.Object | Bir veri kaynağı nesnesi. |
| dataSourceName | java.lang.String | Şablonda veri kaynağı nesnesine başvurmak için bir ad. |

**Returns:**
boolean - Şablon belgesinin ayrıştırılmasının başarılı olup olmadığını gösteren bir bayrak. Döndürülen bayrak yalnızca [getOptions()](../../com.aspose.words/reportingengine/\#getOptions) / [setOptions(int)](../../com.aspose.words/reportingengine/\#setOptions-int) özelliğinin değeri [ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions/\#INLINE-ERROR-MESSAGES) seçeneğini içeriyorsa anlamlıdır.
### buildReport(Document document, Object[] dataSources, String[] dataSourceNames) {#buildReport-com.aspose.words.Document-java.lang.Object---java.lang.String}
```
public boolean buildReport(Document document, Object[] dataSources, String[] dataSourceNames)
```


Belirtilen şablon belgesini, belirtilen kaynaklardan gelen veriyle doldurarak hazır bir rapor haline getirir.

 **Remarks:** 

Bu aşırı yüklemeyi kullanarak şablonda birden fazla veri kaynağı nesnesine ve bunların üyelerine başvurabilirsiniz. İlk veri kaynağının adı, yalnızca veri kaynağının üyelerine başvurup veri kaynağı nesnesine başvurmayacaksanız (ör. boş bir dize veya null) atlanabilir. Diğer veri kaynaklarının adları belirtilmeli ve benzersiz olmalıdır.

Tek bir veri kaynağı kullanacaksanız, bunun yerine [buildReport(com.aspose.words.Document, java.lang.Object)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object) ve [buildReport(com.aspose.words.Document, java.lang.Object, java.lang.String)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object--java.lang.String) aşırı yüklemelerini kullanmayı düşünün.

Bir veri kaynağı nesnesi aşağıdaki türlerden biri olabilir:

 *  [XmlDataSource](../../com.aspose.words/xmldatasource/)
 *  [JsonDataSource](../../com.aspose.words/jsondatasource/)
 *  [CsvDataSource](../../com.aspose.words/csvdatasource/)
 *  [DataSet](../../com.aspose.words.net.system.data/dataset/)
 *  [DataTable](../../com.aspose.words.net.system.data/datatable/)
 *  [DataRow](../../com.aspose.words.net.system.data/datarow/)
 *  [IDataReader](../../com.aspose.words.net.system.data/idatareader/)
 *  [IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
 *  [DataView](../../com.aspose.words.net.system.data/dataview/)
 *  [DataRowView](../../com.aspose.words.net.system.data/datarowview/)
 *  Any other arbitrary Java type

Şablon belgelerinde farklı türde veri kaynaklarıyla nasıl çalışılacağına ilişkin bilgi için şablon sözdizimi referansına bakın (https://docs.aspose.com/display/wordsjava/Template+Syntax).

 **Examples:** 

Eklenen numaralandırmanın olduğu gibi nasıl korunacağını gösterir.

```

 // By default, numbered lists from a template document are continued when their identifiers match those from a document being inserted.
 // With "-sourceNumbering" numbering should be separated and kept as is.
 Document template = DocumentHelper.createSimpleDocument("<>" + System.lineSeparator() + "<>");

 DocumentTestClass doc = new DocumentTestBuilder()
         .withDocument(new Document(getMyDir() + "List item.docx")).build();

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.REMOVE_EMPTY_PARAGRAPHS); }
 engine.buildReport(template, new Object[] { doc }, new String[] { "src" });

 template.save(getArtifactsDir() + "ReportingEngine.SourseListNumbering.docx");
 
```

Word 2016'dan gelen grafiklerle nasıl çalışılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Word 2016 Charts (Java).docx");

 ReportingEngine engine = new ReportingEngine();
 engine.buildReport(doc, new Object[] { Common.getShares(), Common.getShareQuotes() },
         new String[] { "shares", "quotes" });

 doc.save(getArtifactsDir() + "ReportingEngine.Word2016Charts.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | Veri ile doldurulacak bir şablon belgesi. |
| dataSources | java.lang.Object[] | Veri kaynağı nesnelerinin bir dizisi. |
| dataSourceNames | java.lang.String[] | Şablon içinde veri kaynağı nesnelerine referans vermek için kullanılan adların bir dizisi. |

**Returns:**
boolean - Şablon belgesinin ayrıştırılmasının başarılı olup olmadığını gösteren bir bayrak. Döndürülen bayrak yalnızca [getOptions()](../../com.aspose.words/reportingengine/\#getOptions) / [setOptions(int)](../../com.aspose.words/reportingengine/\#setOptions-int) özelliğinin değeri [ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions/\#INLINE-ERROR-MESSAGES) seçeneğini içeriyorsa anlamlıdır.
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getKnownTypes() {#getKnownTypes}
```
public KnownTypeSet getKnownTypes()
```


Bu motor örneği tarafından işlenen rapor şablonları içinde kullanılabilecek tam veya kısmi nitelikli adlarıyla java.lang.Class nesnelerini içeren (yani benzersiz öğeler koleksiyonu) sırasız bir küme alır; bu sayede ilgili tiplerin statik üyeleri çağrılabilir, tip dönüşümleri yapılabilir vb.

**Returns:**
[KnownTypeSet](../../com.aspose.words/knowntypeset/) - An unordered set (i.e.
### getMissingMemberMessage() {#getMissingMemberMessage}
```
public String getMissingMemberMessage()
```


Eksik bir nesne üyesine basit bir referans temsil eden şablon ifadesi yerine yazdırılan bir dize değeri alır. Varsayılan değer boş bir dizedir.

 **Remarks:** 

Bu özellik, [ReportBuildOptions.ALLOW\_MISSING\_MEMBERS](../../com.aspose.words/reportbuildoptions/\#ALLOW-MISSING-MEMBERS) seçeneğiyle birlikte kullanılmalıdır. Aksi takdirde, bir nesnenin eksik bir üyesiyle karşılaşıldığında bir istisna fırlatılır.

Bu özellik yalnızca eksik bir nesne üyesine basit bir referans temsil eden şablon ifadesinin yazdırılmasını etkiler. Örneğin, bir ikili operatörün yazdırılması, operandlarından birinin eksik bir nesne üyesine referans vermesi durumunda etkilenmez.

Bu özelliğin değeri null olarak ayarlanamaz.

 **Examples:** 

Eksik üyelerin nasıl izin verileceğini gösterir.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

**Returns:**
java.lang.String - Eksik bir nesne üyesine basit bir referans temsil eden şablon ifadesi yerine yazdırılan bir dize değeri.
### getOptions() {#getOptions}
```
public int getOptions()
```


Bir rapor oluşturulurken bu [ReportingEngine](../../com.aspose.words/reportingengine/) örneğinin davranışını kontrol eden bayrakların bir kümesini alır.

 **Examples:** 

Eksik üyelerin nasıl izin verileceğini gösterir.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

Raporlama Motoru için seçeneklerin nasıl ayarlanacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Fields (Java).docx");

 // Note that enabling of the option makes the engine to update fields while building a report,
 // so there is no need to update fields separately after that.
 ReportingEngine engine = new ReportingEngine();
 engine.setOptions(ReportBuildOptions.UPDATE_FIELDS_SYNTAX_AWARE);
 engine.buildReport(doc, new String[] { "First topic", "Second topic", "Third topic" }, "topics");

 doc.save(getArtifactsDir() + "ReportingEngine.UpdateFieldsSyntaxAware.docx");
 
```

**Returns:**
int - Bir rapor oluşturulurken bu [ReportingEngine](../../com.aspose.words/reportingengine/) örneğinin davranışını kontrol eden bayrakların bir kümesi. Döndürülen değer, [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/) sabitlerinin bit düzeyinde bir kombinasyonudur.
### getRestrictedTypes() {#getRestrictedTypes}
```
public static Class[] getRestrictedTypes()
```


Motorun şablon sözdizimi aracılığıyla erişememesi gereken türleri, bu türlerin üyelerini ve türetilmiş türlerin üyelerini döndürür.

 **Remarks:** 

Dönen dizi, daha önce [setRestrictedTypes(java.lang.Class[])](../../com.aspose.words/reportingengine/\#setRestrictedTypes-java.lang.Class) kullanılarak ayarlanan öğeleri içerir.

Dönen dizinin öğelerini değiştirmek, kısıtlı türler üzerinde hiçbir etki yapmaz. Kısıtlı türleri değiştirmek için, bunun yerine [setRestrictedTypes(java.lang.Class[])](../../com.aspose.words/reportingengine/\#setRestrictedTypes-java.lang.Class) kullanın.

**Returns:**
java.lang.Class[] - Motorun şablon sözdizimi aracılığıyla erişememesi gereken üyeler ve türetilmiş türlerin üyeleri.
### getUseReflectionOptimization() {#getUseReflectionOptimization}
```
public static boolean getUseReflectionOptimization()
```


Yansıma API'si aracılığıyla gerçekleştirilen özel tür üyelerinin çağrılarının dinamik sınıf oluşturma ile optimize edilip edilmediğini gösteren bir değer alır. Varsayılan değer  true .

 **Remarks:** 

Bu optimizasyonu devre dışı bırakmanın tercih edildiği bazı senaryolar vardır. Örneğin, sürekli olarak küçük veri öğesi koleksiyonlarıyla çalışıyorsanız, dinamik sınıf oluşturmanın getirdiği ek yük, doğrudan yansıma API çağrılarının getirdiği ek yüke göre daha belirgin olabilir. Bu seçenek iOS'ta çalıştırıldığında ve yansıma optimizasyonu kullanılmadığında etkili değildir.

**Returns:**
boolean - Yansıma API'si aracılığıyla gerçekleştirilen özel tür üyelerinin çağrılarının dinamik sınıf oluşturma ile optimize edilip edilmediğini gösteren bir değer.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### setMissingMemberMessage(String value) {#setMissingMemberMessage-java.lang.String}
```
public void setMissingMemberMessage(String value)
```


Eksik bir nesne üyesine basit bir referans temsil eden şablon ifadesi yerine yazdırılan bir dize değeri ayarlar. Varsayılan değer boş bir dizedir.

 **Remarks:** 

Bu özellik, [ReportBuildOptions.ALLOW\_MISSING\_MEMBERS](../../com.aspose.words/reportbuildoptions/\#ALLOW-MISSING-MEMBERS) seçeneğiyle birlikte kullanılmalıdır. Aksi takdirde, bir nesnenin eksik bir üyesiyle karşılaşıldığında bir istisna fırlatılır.

Bu özellik yalnızca eksik bir nesne üyesine basit bir referans temsil eden şablon ifadesinin yazdırılmasını etkiler. Örneğin, bir ikili operatörün yazdırılması, operandlarından birinin eksik bir nesne üyesine referans vermesi durumunda etkilenmez.

Bu özelliğin değeri null olarak ayarlanamaz.

 **Examples:** 

Eksik üyelerin nasıl izin verileceğini gösterir.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Eksik bir nesne üyesine basit bir referans temsil eden şablon ifadesi yerine yazdırılan bir dize değeri. |

### setOptions(int value) {#setOptions-int}
```
public void setOptions(int value)
```


Bir rapor oluşturulurken bu [ReportingEngine](../../com.aspose.words/reportingengine/) örneğinin davranışını kontrol eden bayrakların bir kümesini ayarlar.

 **Examples:** 

Eksik üyelerin nasıl izin verileceğini gösterir.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

Raporlama Motoru için seçeneklerin nasıl ayarlanacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Fields (Java).docx");

 // Note that enabling of the option makes the engine to update fields while building a report,
 // so there is no need to update fields separately after that.
 ReportingEngine engine = new ReportingEngine();
 engine.setOptions(ReportBuildOptions.UPDATE_FIELDS_SYNTAX_AWARE);
 engine.buildReport(doc, new String[] { "First topic", "Second topic", "Third topic" }, "topics");

 doc.save(getArtifactsDir() + "ReportingEngine.UpdateFieldsSyntaxAware.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Bir rapor oluşturulurken bu [ReportingEngine](../../com.aspose.words/reportingengine/) örneğinin davranışını kontrol eden bayrakların bir kümesi. Değer, [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/) sabitlerinin bit düzeyinde bir kombinasyonu olmalıdır. |

### setRestrictedTypes(Class[] types) {#setRestrictedTypes-java.lang.Class...}
```
public static void setRestrictedTypes(Class[] types)
```


Motorun şablon sözdizimi aracılığıyla erişememesi gereken türleri, bu türlerin üyelerini ve türetilmiş türlerin üyelerini belirtir.

 **Remarks:** 

Kısıtlı türler, bir raporun ilk oluşturulmasından önce ayarlanmalıdır. BuildReportbuildReport çağrıldıktan sonra, kısıtlı türler değiştirilemez ve bunu yapmaya çalıştığınızda bir istisna fırlatılır. Kısıtlı türleri ayarlamak için en iyi yer uygulama başlangıcıdır.

Çok sayıda kısıtlı türün performansı etkileyebileceğini unutmayın, bu nedenle yalnızca üyelerine erişimin gerçekten hassas olduğu türleri kısıtlamak daha iyidir.

Aşağıdaki durumlarda java.lang.IllegalArgumentException fırlatır:

\-  types  is null.

\- types öğelerinden biri null .

\- types öğelerinden biri görünmez bir türü temsil eder, i.e. erişilemeyen bir tür veya dış türü erişilemeyen bir public iç içe tür.

\- types öğelerinden biri dizi türünü temsil eder.

\- types yinelenen girişler içerir.

 **Examples:** 

Güvenli olmayan olarak kabul edilen türlerin üyelerine erişimin nasıl reddedileceğini gösterir.

```

 Document doc =
         DocumentHelper.createSimpleDocument(
                 "<><<[typeVar]>>");

 // Note, that you can't set restricted types during or after building a report.
 ReportingEngine.setRestrictedTypes(Class.class);
 // We set "AllowMissingMembers" option to avoid exceptions during building a report.
 ReportingEngine engine = new ReportingEngine();
 engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
 engine.buildReport(doc, new Object());

 // We get an empty string because we can't access the GetType() method.
 Assert.assertEquals(doc.getText().trim(), "");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| types | java.lang.Class[] | Kısıtlanacak türler. |

### setUseReflectionOptimization(boolean value) {#setUseReflectionOptimization-boolean}
```
public static void setUseReflectionOptimization(boolean value)
```


Özel tür üyelerinin yansıma API'si aracılığıyla yapılan çağrılarının dinik sınıf oluşturma ile optimize edilip edilmediğini gösteren bir değer ayarlar. Varsayılan değer  true .

 **Remarks:** 

Bu optimizasyonu devre dışı bırakmanın tercih edildiği bazı senaryolar vardır. Örneğin, sürekli olarak küçük veri öğesi koleksiyonlarıyla çalışıyorsanız, dinamik sınıf oluşturmanın getirdiği ek yük, doğrudan yansıma API çağrılarının getirdiği ek yüke göre daha belirgin olabilir. Bu seçenek iOS'ta çalıştırıldığında ve yansıma optimizasyonu kullanılmadığında etkili değildir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Yansıma API'si aracılığıyla gerçekleştirilen özel tür üyelerinin çağrılarının dinamik sınıf oluşturma ile optimize edilip edilmediğini gösteren bir değer. |

