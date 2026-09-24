---
title: "ReportBuilderOptions"
linktitle: "ReportBuilderOptions"
second_title: "Aspose.Words Java için"
description: "Java'da LINQ Reporting Engine işlevselliği için seçenekleri temsil eder."
type: docs
weight: 573
url: /tr/java/com.aspose.words/reportbuilderoptions/
---

**Inheritance:**
java.lang.Object
```
public class ReportBuilderOptions
```

LINQ Reporting Engine işlevselliği için seçenekleri temsil eder.

 **Examples:** 

Belgeyi veriyle nasıl dolduracağınızı gösterir.

```

 public void buildReportData() throws Exception {
     // There is a several ways to populate document with data:
     String doc = getMyDir() + "Reporting engine template - If greedy (Java).docx";

     AsposeData obj = new AsposeData();
     {
         obj.setList(new ArrayList<>());
         {
             obj.getList().add("abc");
         }
     }

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.1.docx", obj);
     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.2.docx", obj, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.3.docx", SaveFormat.DOCX, obj);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.4.docx", SaveFormat.DOCX, obj, options);
 }

 public static class AsposeData {
     public ArrayList getList() {
         return mList;
     }

     ;

     public void setList(ArrayList value) {
         mList = value;
     }

     ;

     private ArrayList mList;
 }
 
```
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [ReportBuilderOptions()](#ReportBuilderOptions) | Bu sınıfın yeni bir örneğini başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getKnownTypes()](#getKnownTypes) | Sırasız bir küme alır (örn. |
| [getMissingMemberMessage()](#getMissingMemberMessage) | Eksik bir nesne üyesine basit bir referans temsil eden şablon ifadesi yerine yazdırılan bir dize değeri alır. |
| [getOptions()](#getOptions) | Bir rapor oluşturulurken bu [ReportingEngine](../../com.aspose.words/reportingengine/) örneğinin davranışını kontrol eden bayrakların bir kümesini alır. |
| [setMissingMemberMessage(String value)](#setMissingMemberMessage-java.lang.String) | Eksik bir nesne üyesine basit bir referans temsil eden şablon ifadesi yerine yazdırılan bir dize değeri ayarlar. |
| [setOptions(int value)](#setOptions-int) | Bir rapor oluşturulurken bu [ReportingEngine](../../com.aspose.words/reportingengine/) örneğinin davranışını kontrol eden bayrakların bir kümesini ayarlar. |
### ReportBuilderOptions() {#ReportBuilderOptions}
```
public ReportBuilderOptions()
```


Bu sınıfın yeni bir örneğini başlatır.

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

**Returns:**
java.lang.String - Eksik bir nesne üyesine basit bir referans temsil eden şablon ifadesi yerine yazdırılan bir dize değeri.
### getOptions() {#getOptions}
```
public int getOptions()
```


Bir rapor oluşturulurken bu [ReportingEngine](../../com.aspose.words/reportingengine/) örneğinin davranışını kontrol eden bayrakların bir kümesini alır.

 **Examples:** 

Belgeyi veriyle nasıl dolduracağınızı gösterir.

```

 public void buildReportData() throws Exception {
     // There is a several ways to populate document with data:
     String doc = getMyDir() + "Reporting engine template - If greedy (Java).docx";

     AsposeData obj = new AsposeData();
     {
         obj.setList(new ArrayList<>());
         {
             obj.getList().add("abc");
         }
     }

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.1.docx", obj);
     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.2.docx", obj, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.3.docx", SaveFormat.DOCX, obj);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.4.docx", SaveFormat.DOCX, obj, options);
 }

 public static class AsposeData {
     public ArrayList getList() {
         return mList;
     }

     ;

     public void setList(ArrayList value) {
         mList = value;
     }

     ;

     private ArrayList mList;
 }
 
```

**Returns:**
int - Bir rapor oluşturulurken bu [ReportingEngine](../../com.aspose.words/reportingengine/) örneğinin davranışını kontrol eden bayrakların bir kümesi. Döndürülen değer, [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/) sabitlerinin bit düzeyinde bir kombinasyonudur.
### setMissingMemberMessage(String value) {#setMissingMemberMessage-java.lang.String}
```
public void setMissingMemberMessage(String value)
```


Eksik bir nesne üyesine basit bir referans temsil eden şablon ifadesi yerine yazdırılan bir dize değeri ayarlar. Varsayılan değer boş bir dizedir.

 **Remarks:** 

Bu özellik, [ReportBuildOptions.ALLOW\_MISSING\_MEMBERS](../../com.aspose.words/reportbuildoptions/\#ALLOW-MISSING-MEMBERS) seçeneğiyle birlikte kullanılmalıdır. Aksi takdirde, bir nesnenin eksik bir üyesiyle karşılaşıldığında bir istisna fırlatılır.

Bu özellik yalnızca eksik bir nesne üyesine basit bir referans temsil eden şablon ifadesinin yazdırılmasını etkiler. Örneğin, bir ikili operatörün yazdırılması, operandlarından birinin eksik bir nesne üyesine referans vermesi durumunda etkilenmez.

Bu özelliğin değeri null olarak ayarlanamaz.

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

Belgeyi veriyle nasıl dolduracağınızı gösterir.

```

 public void buildReportData() throws Exception {
     // There is a several ways to populate document with data:
     String doc = getMyDir() + "Reporting engine template - If greedy (Java).docx";

     AsposeData obj = new AsposeData();
     {
         obj.setList(new ArrayList<>());
         {
             obj.getList().add("abc");
         }
     }

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.1.docx", obj);
     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.2.docx", obj, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.3.docx", SaveFormat.DOCX, obj);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.4.docx", SaveFormat.DOCX, obj, options);
 }

 public static class AsposeData {
     public ArrayList getList() {
         return mList;
     }

     ;

     public void setList(ArrayList value) {
         mList = value;
     }

     ;

     private ArrayList mList;
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Bir rapor oluşturulurken bu [ReportingEngine](../../com.aspose.words/reportingengine/) örneğinin davranışını kontrol eden bayrakların bir kümesi. Değer, [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/) sabitlerinin bit düzeyinde bir kombinasyonu olmalıdır. |

