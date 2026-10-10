---
title: "MailMergerContext"
linktitle: "MailMergerContext"
second_title: "Aspose.Words Java için"
description: "Java'da mail birleştirme bağlamı."
type: docs
weight: 447
url: /tr/java/com.aspose.words/mailmergercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class MailMergerContext extends ProcessorContext
```

Posta birleştirme bağlamı.

 **Examples:** 

Bağlam kullanarak tek bir kayıt için posta birleştirme işleminin nasıl yapılacağını gösterir.

```

 // There is a several ways to do mail merge operation:
 String doc = getMyDir() + "Mail merge.doc";

 String[] fieldNames = new String[]{"FirstName", "Location", "SpecialCharsInName()"};
 String[] fieldValues = new String[]{"James Bond", "London", "Classified"};

 MailMergerContext mailMergerContext = new MailMergerContext();
 mailMergerContext.setSimpleDataSource(fieldNames, fieldValues);
 mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

 MailMerger.create(mailMergerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.MailMergeContext.docx")
         .execute();
 
```

Bağlam kullanarak akıştan tek bir kayıt için posta birleştirme işleminin nasıl yapılacağını gösterir.

```

 // There is a several ways to do mail merge operation using documents from the stream:
 String[] fieldNames = new String[]{"FirstName", "Location", "SpecialCharsInName()"};
 String[] fieldValues = new String[]{"James Bond", "London", "Classified"};

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Mail merge.doc")) {
     MailMergerContext mailMergerContext = new MailMergerContext();
     mailMergerContext.setSimpleDataSource(fieldNames, fieldValues);
     mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MailMergeContextStream.docx")) {
         MailMerger.create(mailMergerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

Bağlam kullanarak bir DataRow'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

```

 // There is a several ways to do mail merge operation from a DataRow:
 String doc = getMyDir() + "Mail merge.doc";

 DataTable dataTable = new DataTable();
 dataTable.getColumns().add("FirstName");
 dataTable.getColumns().add("Location");
 dataTable.getColumns().add("SpecialCharsInName()");

 dataTable.getRows().add(new String[]{"James Bond", "London", "Classified"});
 DataRow dataRow = dataTable.getRows().get(0);

 MailMergerContext mailMergerContext = new MailMergerContext();
 mailMergerContext.setSimpleDataSource(dataRow);
 mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

 MailMerger.create(mailMergerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.MailMergeContextDataRow.docx")
         .execute();
 
```

Bağlam kullanarak akıştan belgelerle bir DataRow'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

```

 // There is a several ways to do mail merge operation from a DataRow using documents from the stream:
 DataTable dataTable = new DataTable();
 dataTable.getColumns().add("FirstName");
 dataTable.getColumns().add("Location");
 dataTable.getColumns().add("SpecialCharsInName()");

 dataTable.getRows().add(new String[]{"James Bond", "London", "Classified"});
 DataRow dataRow = dataTable.getRows().get(0);

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Mail merge.doc")) {
     MailMergerContext mailMergerContext = new MailMergerContext();
     mailMergerContext.setSimpleDataSource(dataRow);
     mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MailMergeContextStreamDataRow.docx")) {
         MailMerger.create(mailMergerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

Bağlamı kullanarak bir DataTable'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

```

 // There is a several ways to do mail merge operation from a DataTable:
 String doc = getMyDir() + "Mail merge.doc";

 DataTable dataTable = new DataTable();
 dataTable.getColumns().add("FirstName");
 dataTable.getColumns().add("Location");
 dataTable.getColumns().add("SpecialCharsInName()");

 dataTable.getRows().add(new String[]{"James Bond", "London", "Classified"});

 MailMergerContext mailMergerContext = new MailMergerContext();
 mailMergerContext.setSimpleDataSource(dataTable);
 mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

 MailMerger.create(mailMergerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.MailMergeContextDataTable.docx")
         .execute();
 
```

Bağlamı kullanarak akıştan belgelerle bir DataTable'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

```

 // There is a several ways to do mail merge operation from a DataTable using documents from the stream:
 DataTable dataTable = new DataTable();
 dataTable.getColumns().add("FirstName");
 dataTable.getColumns().add("Location");
 dataTable.getColumns().add("SpecialCharsInName()");

 dataTable.getRows().add(new String[]{"James Bond", "London", "Classified"});

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Mail merge.doc")) {
     MailMergerContext mailMergerContext = new MailMergerContext();
     mailMergerContext.setSimpleDataSource(dataTable);
     mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MailMergeContextStreamDataTable.docx")) {
         MailMerger.create(mailMergerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

Bağlamı kullanarak bir DataTable'dan bölgelerle posta birleştirme işleminin nasıl yapılacağını gösterir.

```

 // There is a several ways to do mail merge with regions operation from a DataTable:
 String doc = getMyDir() + "Mail merge with regions.docx";

 DataTable dataTable = new DataTable("MyTable");
 dataTable.getColumns().add("FirstName");
 dataTable.getColumns().add("LastName");
 dataTable.getRows().add(new Object[]{"John", "Doe"});
 dataTable.getRows().add(new Object[]{"", ""});
 dataTable.getRows().add(new Object[]{"Jane", "Doe"});

 MailMergerContext mailMergerContext = new MailMergerContext();
 mailMergerContext.setRegionsDataSource(dataTable);
 mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

 MailMerger.create(mailMergerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.MailMergeContextWithRegionsDataTable.docx")
         .execute();
 
```

Bağlamı kullanarak akıştan belgelerle bir DataTable'dan bölgelerle posta birleştirme işleminin nasıl yapılacağını gösterir.

```

 // There is a several ways to do mail merge with regions operation from a DataTable using documents from the stream:
 DataTable dataTable = new DataTable("MyTable");
 dataTable.getColumns().add("FirstName");
 dataTable.getColumns().add("LastName");
 dataTable.getRows().add(new Object[]{"John", "Doe"});
 dataTable.getRows().add(new Object[]{"", ""});
 dataTable.getRows().add(new Object[]{"Jane", "Doe"});

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Mail merge.doc")) {
     MailMergerContext mailMergerContext = new MailMergerContext();
     mailMergerContext.setRegionsDataSource(dataTable);
     mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MailMergeContextStreamWithRegionsDataTable.docx")) {
         MailMerger.create(mailMergerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

Bağlamı kullanarak bir DataSet'ten bölgelerle posta birleştirme işleminin nasıl yapılacağını gösterir.

```

 // There is a several ways to do mail merge with regions operation from a DataSet:
 String doc = getMyDir() + "Mail merge with regions data set.docx";

 DataTable tableCustomers = new DataTable("Customers");
 tableCustomers.getColumns().add("CustomerID");
 tableCustomers.getColumns().add("CustomerName");
 tableCustomers.getRows().add(new Object[]{1, "John Doe"});
 tableCustomers.getRows().add(new Object[]{2, "Jane Doe"});

 DataTable tableOrders = new DataTable("Orders");
 tableOrders.getColumns().add("CustomerID");
 tableOrders.getColumns().add("ItemName");
 tableOrders.getColumns().add("Quantity");
 tableOrders.getRows().add(new Object[]{1, "Hawaiian", 2});
 tableOrders.getRows().add(new Object[]{2, "Pepperoni", 1});
 tableOrders.getRows().add(new Object[]{2, "Chicago", 1});

 DataSet dataSet = new DataSet();
 dataSet.getTables().add(tableCustomers);
 dataSet.getTables().add(tableOrders);
 dataSet.getRelations().add(tableCustomers.getColumns().get("CustomerID"), tableOrders.getColumns().get("CustomerID"));

 MailMergerContext mailMergerContext = new MailMergerContext();
 mailMergerContext.setRegionsDataSource(dataSet);
 mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

 MailMerger.create(mailMergerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.MailMergeContextWithRegionsDataTable.docx")
         .execute();
 
```

Bağlamı kullanarak akıştan belgelerle bir DataSet'ten bölgelerle posta birleştirme işleminin nasıl yapılacağını gösterir.

```

 // There is a several ways to do mail merge with regions operation from a DataSet using documents from the stream:
 DataTable tableCustomers = new DataTable("Customers");
 tableCustomers.getColumns().add("CustomerID");
 tableCustomers.getColumns().add("CustomerName");
 tableCustomers.getRows().add(new Object[]{1, "John Doe"});
 tableCustomers.getRows().add(new Object[]{2, "Jane Doe"});

 DataTable tableOrders = new DataTable("Orders");
 tableOrders.getColumns().add("CustomerID");
 tableOrders.getColumns().add("ItemName");
 tableOrders.getColumns().add("Quantity");
 tableOrders.getRows().add(new Object[]{1, "Hawaiian", 2});
 tableOrders.getRows().add(new Object[]{2, "Pepperoni", 1});
 tableOrders.getRows().add(new Object[]{2, "Chicago", 1});

 DataSet dataSet = new DataSet();
 dataSet.getTables().add(tableCustomers);
 dataSet.getTables().add(tableOrders);
 dataSet.getRelations().add(tableCustomers.getColumns().get("CustomerID"), tableOrders.getColumns().get("CustomerID"));

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Mail merge.doc")) {
     MailMergerContext mailMergerContext = new MailMergerContext();
     mailMergerContext.setRegionsDataSource(dataSet);
     mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MailMergeContextStreamWithRegionsDataSet.docx")) {
         MailMerger.create(mailMergerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [MailMergerContext()](#MailMergerContext) | Bu sınıfın yeni bir örneğini başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getFontSettings()](#getFontSettings) | İşlemci tarafından kullanılan yazı tipi ayarları. |
| [getLayoutOptions()](#getLayoutOptions) | İşlemci tarafından kullanılan belge düzeni seçenekleri. |
| [getMailMergeOptions()](#getMailMergeOptions) | Posta birleştirme seçenekleri. |
| [getWarningCallback()](#getWarningCallback) | İşlemci tarafından kullanılan uyarı geri çağırma. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | İşlemci tarafından kullanılan yazı tipi ayarları. |
| [setRegionsDataSource(System.Data.DataSet dataSet)](#setRegionsDataSource-com.aspose.words.net.System.Data.DataSet) | Bölgelerle mail birleştirme yürütmek için kullanılan veri kaynağını ayarlar. |
| [setRegionsDataSource(System.Data.DataTable dataTable)](#setRegionsDataSource-com.aspose.words.net.System.Data.DataTable) | Bölgelerle mail birleştirme yürütmek için kullanılan veri kaynağını ayarlar. |
| [setSimpleDataSource(System.Data.DataRow dataRow)](#setSimpleDataSource-com.aspose.words.net.System.Data.DataRow) | Basit mail birleştirme yürütmek için kullanılan veri kaynağını ayarlar. |
| [setSimpleDataSource(System.Data.DataTable dataTable)](#setSimpleDataSource-com.aspose.words.net.System.Data.DataTable) | Basit mail birleştirme yürütmek için kullanılan veri kaynağını ayarlar. |
| [setSimpleDataSource(String[] fieldNames, Object[] fieldValues)](#setSimpleDataSource-java.lang.String---java.lang.Object) | Basit mail birleştirme yürütmek için kullanılan veri kaynağını ayarlar. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | İşlemci tarafından kullanılan uyarı geri çağırma. |
### MailMergerContext() {#MailMergerContext}
```
public MailMergerContext()
```


Bu sınıfın yeni bir örneğini başlatır.

### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


İşlemci tarafından kullanılan yazı tipi ayarları.

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getLayoutOptions() {#getLayoutOptions}
```
public LayoutOptions getLayoutOptions()
```


İşlemci tarafından kullanılan belge düzeni seçenekleri.

**Returns:**
[LayoutOptions](../../com.aspose.words/layoutoptions/) - The corresponding [LayoutOptions](../../com.aspose.words/layoutoptions/) value.
### getMailMergeOptions() {#getMailMergeOptions}
```
public MailMergeOptions getMailMergeOptions()
```


Posta birleştirme seçenekleri.

 **Examples:** 

Bağlam kullanarak tek bir kayıt için posta birleştirme işleminin nasıl yapılacağını gösterir.

```

 // There is a several ways to do mail merge operation:
 String doc = getMyDir() + "Mail merge.doc";

 String[] fieldNames = new String[]{"FirstName", "Location", "SpecialCharsInName()"};
 String[] fieldValues = new String[]{"James Bond", "London", "Classified"};

 MailMergerContext mailMergerContext = new MailMergerContext();
 mailMergerContext.setSimpleDataSource(fieldNames, fieldValues);
 mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

 MailMerger.create(mailMergerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.MailMergeContext.docx")
         .execute();
 
```

Bağlam kullanarak akıştan tek bir kayıt için posta birleştirme işleminin nasıl yapılacağını gösterir.

```

 // There is a several ways to do mail merge operation using documents from the stream:
 String[] fieldNames = new String[]{"FirstName", "Location", "SpecialCharsInName()"};
 String[] fieldValues = new String[]{"James Bond", "London", "Classified"};

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Mail merge.doc")) {
     MailMergerContext mailMergerContext = new MailMergerContext();
     mailMergerContext.setSimpleDataSource(fieldNames, fieldValues);
     mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MailMergeContextStream.docx")) {
         MailMerger.create(mailMergerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Returns:**
[MailMergeOptions](../../com.aspose.words/mailmergeoptions/) - The corresponding [MailMergeOptions](../../com.aspose.words/mailmergeoptions/) value.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


İşlemci tarafından kullanılan uyarı geri çağırma.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


İşlemci tarafından kullanılan yazı tipi ayarları.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | İlgili [FontSettings](../../com.aspose.words/fontsettings/) değeri. |

### setRegionsDataSource(System.Data.DataSet dataSet) {#setRegionsDataSource-com.aspose.words.net.System.Data.DataSet}
```
public void setRegionsDataSource(System.Data.DataSet dataSet)
```


Bölgelerle mail birleştirme yürütmek için kullanılan veri kaynağını ayarlar.

 **Remarks:** 

Hem basit posta birleştirme veri kaynağı hem de bölgeyle posta birleştirme veri kaynağı belirtilmişse, bölgeyle posta birleştirme önce yürütülür ve ardından basit posta birleştirme yürütülür.

 **Examples:** 

Bağlamı kullanarak bir DataSet'ten bölgelerle posta birleştirme işleminin nasıl yapılacağını gösterir.

```

 // There is a several ways to do mail merge with regions operation from a DataSet:
 String doc = getMyDir() + "Mail merge with regions data set.docx";

 DataTable tableCustomers = new DataTable("Customers");
 tableCustomers.getColumns().add("CustomerID");
 tableCustomers.getColumns().add("CustomerName");
 tableCustomers.getRows().add(new Object[]{1, "John Doe"});
 tableCustomers.getRows().add(new Object[]{2, "Jane Doe"});

 DataTable tableOrders = new DataTable("Orders");
 tableOrders.getColumns().add("CustomerID");
 tableOrders.getColumns().add("ItemName");
 tableOrders.getColumns().add("Quantity");
 tableOrders.getRows().add(new Object[]{1, "Hawaiian", 2});
 tableOrders.getRows().add(new Object[]{2, "Pepperoni", 1});
 tableOrders.getRows().add(new Object[]{2, "Chicago", 1});

 DataSet dataSet = new DataSet();
 dataSet.getTables().add(tableCustomers);
 dataSet.getTables().add(tableOrders);
 dataSet.getRelations().add(tableCustomers.getColumns().get("CustomerID"), tableOrders.getColumns().get("CustomerID"));

 MailMergerContext mailMergerContext = new MailMergerContext();
 mailMergerContext.setRegionsDataSource(dataSet);
 mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

 MailMerger.create(mailMergerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.MailMergeContextWithRegionsDataTable.docx")
         .execute();
 
```

Bağlamı kullanarak akıştan belgelerle bir DataSet'ten bölgelerle posta birleştirme işleminin nasıl yapılacağını gösterir.

```

 // There is a several ways to do mail merge with regions operation from a DataSet using documents from the stream:
 DataTable tableCustomers = new DataTable("Customers");
 tableCustomers.getColumns().add("CustomerID");
 tableCustomers.getColumns().add("CustomerName");
 tableCustomers.getRows().add(new Object[]{1, "John Doe"});
 tableCustomers.getRows().add(new Object[]{2, "Jane Doe"});

 DataTable tableOrders = new DataTable("Orders");
 tableOrders.getColumns().add("CustomerID");
 tableOrders.getColumns().add("ItemName");
 tableOrders.getColumns().add("Quantity");
 tableOrders.getRows().add(new Object[]{1, "Hawaiian", 2});
 tableOrders.getRows().add(new Object[]{2, "Pepperoni", 1});
 tableOrders.getRows().add(new Object[]{2, "Chicago", 1});

 DataSet dataSet = new DataSet();
 dataSet.getTables().add(tableCustomers);
 dataSet.getTables().add(tableOrders);
 dataSet.getRelations().add(tableCustomers.getColumns().get("CustomerID"), tableOrders.getColumns().get("CustomerID"));

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Mail merge.doc")) {
     MailMergerContext mailMergerContext = new MailMergerContext();
     mailMergerContext.setRegionsDataSource(dataSet);
     mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MailMergeContextStreamWithRegionsDataSet.docx")) {
         MailMerger.create(mailMergerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset/) |  |

### setRegionsDataSource(System.Data.DataTable dataTable) {#setRegionsDataSource-com.aspose.words.net.System.Data.DataTable}
```
public void setRegionsDataSource(System.Data.DataTable dataTable)
```


Bölgelerle mail birleştirme yürütmek için kullanılan veri kaynağını ayarlar.

 **Remarks:** 

Hem basit posta birleştirme veri kaynağı hem de bölgeyle posta birleştirme veri kaynağı belirtilmişse, bölgeyle posta birleştirme önce yürütülür ve ardından basit posta birleştirme yürütülür.

 **Examples:** 

Bağlamı kullanarak bir DataTable'dan bölgelerle posta birleştirme işleminin nasıl yapılacağını gösterir.

```

 // There is a several ways to do mail merge with regions operation from a DataTable:
 String doc = getMyDir() + "Mail merge with regions.docx";

 DataTable dataTable = new DataTable("MyTable");
 dataTable.getColumns().add("FirstName");
 dataTable.getColumns().add("LastName");
 dataTable.getRows().add(new Object[]{"John", "Doe"});
 dataTable.getRows().add(new Object[]{"", ""});
 dataTable.getRows().add(new Object[]{"Jane", "Doe"});

 MailMergerContext mailMergerContext = new MailMergerContext();
 mailMergerContext.setRegionsDataSource(dataTable);
 mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

 MailMerger.create(mailMergerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.MailMergeContextWithRegionsDataTable.docx")
         .execute();
 
```

Bağlamı kullanarak akıştan belgelerle bir DataTable'dan bölgelerle posta birleştirme işleminin nasıl yapılacağını gösterir.

```

 // There is a several ways to do mail merge with regions operation from a DataTable using documents from the stream:
 DataTable dataTable = new DataTable("MyTable");
 dataTable.getColumns().add("FirstName");
 dataTable.getColumns().add("LastName");
 dataTable.getRows().add(new Object[]{"John", "Doe"});
 dataTable.getRows().add(new Object[]{"", ""});
 dataTable.getRows().add(new Object[]{"Jane", "Doe"});

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Mail merge.doc")) {
     MailMergerContext mailMergerContext = new MailMergerContext();
     mailMergerContext.setRegionsDataSource(dataTable);
     mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MailMergeContextStreamWithRegionsDataTable.docx")) {
         MailMerger.create(mailMergerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

### setSimpleDataSource(System.Data.DataRow dataRow) {#setSimpleDataSource-com.aspose.words.net.System.Data.DataRow}
```
public void setSimpleDataSource(System.Data.DataRow dataRow)
```


Basit mail birleştirme yürütmek için kullanılan veri kaynağını ayarlar.

 **Remarks:** 

Hem basit posta birleştirme veri kaynağı hem de bölgeyle posta birleştirme veri kaynağı belirtilmişse, bölgeyle posta birleştirme önce yürütülür ve ardından basit posta birleştirme yürütülür.

 **Examples:** 

Bağlam kullanarak bir DataRow'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

```

 // There is a several ways to do mail merge operation from a DataRow:
 String doc = getMyDir() + "Mail merge.doc";

 DataTable dataTable = new DataTable();
 dataTable.getColumns().add("FirstName");
 dataTable.getColumns().add("Location");
 dataTable.getColumns().add("SpecialCharsInName()");

 dataTable.getRows().add(new String[]{"James Bond", "London", "Classified"});
 DataRow dataRow = dataTable.getRows().get(0);

 MailMergerContext mailMergerContext = new MailMergerContext();
 mailMergerContext.setSimpleDataSource(dataRow);
 mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

 MailMerger.create(mailMergerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.MailMergeContextDataRow.docx")
         .execute();
 
```

Bağlam kullanarak akıştan belgelerle bir DataRow'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

```

 // There is a several ways to do mail merge operation from a DataRow using documents from the stream:
 DataTable dataTable = new DataTable();
 dataTable.getColumns().add("FirstName");
 dataTable.getColumns().add("Location");
 dataTable.getColumns().add("SpecialCharsInName()");

 dataTable.getRows().add(new String[]{"James Bond", "London", "Classified"});
 DataRow dataRow = dataTable.getRows().get(0);

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Mail merge.doc")) {
     MailMergerContext mailMergerContext = new MailMergerContext();
     mailMergerContext.setSimpleDataSource(dataRow);
     mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MailMergeContextStreamDataRow.docx")) {
         MailMerger.create(mailMergerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| dataRow | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### setSimpleDataSource(System.Data.DataTable dataTable) {#setSimpleDataSource-com.aspose.words.net.System.Data.DataTable}
```
public void setSimpleDataSource(System.Data.DataTable dataTable)
```


Basit mail birleştirme yürütmek için kullanılan veri kaynağını ayarlar.

 **Remarks:** 

Hem basit posta birleştirme veri kaynağı hem de bölgeyle posta birleştirme veri kaynağı belirtilmişse, bölgeyle posta birleştirme önce yürütülür ve ardından basit posta birleştirme yürütülür.

 **Examples:** 

Bağlamı kullanarak bir DataTable'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

```

 // There is a several ways to do mail merge operation from a DataTable:
 String doc = getMyDir() + "Mail merge.doc";

 DataTable dataTable = new DataTable();
 dataTable.getColumns().add("FirstName");
 dataTable.getColumns().add("Location");
 dataTable.getColumns().add("SpecialCharsInName()");

 dataTable.getRows().add(new String[]{"James Bond", "London", "Classified"});

 MailMergerContext mailMergerContext = new MailMergerContext();
 mailMergerContext.setSimpleDataSource(dataTable);
 mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

 MailMerger.create(mailMergerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.MailMergeContextDataTable.docx")
         .execute();
 
```

Bağlamı kullanarak akıştan belgelerle bir DataTable'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

```

 // There is a several ways to do mail merge operation from a DataTable using documents from the stream:
 DataTable dataTable = new DataTable();
 dataTable.getColumns().add("FirstName");
 dataTable.getColumns().add("Location");
 dataTable.getColumns().add("SpecialCharsInName()");

 dataTable.getRows().add(new String[]{"James Bond", "London", "Classified"});

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Mail merge.doc")) {
     MailMergerContext mailMergerContext = new MailMergerContext();
     mailMergerContext.setSimpleDataSource(dataTable);
     mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MailMergeContextStreamDataTable.docx")) {
         MailMerger.create(mailMergerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) |  |

### setSimpleDataSource(String[] fieldNames, Object[] fieldValues) {#setSimpleDataSource-java.lang.String---java.lang.Object}
```
public void setSimpleDataSource(String[] fieldNames, Object[] fieldValues)
```


Basit mail birleştirme yürütmek için kullanılan veri kaynağını ayarlar.

 **Remarks:** 

Hem basit posta birleştirme veri kaynağı hem de bölgeyle posta birleştirme veri kaynağı belirtilmişse, bölgeyle posta birleştirme önce yürütülür ve ardından basit posta birleştirme yürütülür.

 **Examples:** 

Bağlam kullanarak tek bir kayıt için posta birleştirme işleminin nasıl yapılacağını gösterir.

```

 // There is a several ways to do mail merge operation:
 String doc = getMyDir() + "Mail merge.doc";

 String[] fieldNames = new String[]{"FirstName", "Location", "SpecialCharsInName()"};
 String[] fieldValues = new String[]{"James Bond", "London", "Classified"};

 MailMergerContext mailMergerContext = new MailMergerContext();
 mailMergerContext.setSimpleDataSource(fieldNames, fieldValues);
 mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

 MailMerger.create(mailMergerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.MailMergeContext.docx")
         .execute();
 
```

Bağlam kullanarak akıştan tek bir kayıt için posta birleştirme işleminin nasıl yapılacağını gösterir.

```

 // There is a several ways to do mail merge operation using documents from the stream:
 String[] fieldNames = new String[]{"FirstName", "Location", "SpecialCharsInName()"};
 String[] fieldValues = new String[]{"James Bond", "London", "Classified"};

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Mail merge.doc")) {
     MailMergerContext mailMergerContext = new MailMergerContext();
     mailMergerContext.setSimpleDataSource(fieldNames, fieldValues);
     mailMergerContext.getMailMergeOptions().setTrimWhitespaces(true);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MailMergeContextStream.docx")) {
         MailMerger.create(mailMergerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fieldNames | java.lang.String[] |  |
| fieldValues | java.lang.Object[] |  |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


İşlemci tarafından kullanılan uyarı geri çağırma.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | İlgili [IWarningCallback](../../com.aspose.words/iwarningcallback/) değeri. |

