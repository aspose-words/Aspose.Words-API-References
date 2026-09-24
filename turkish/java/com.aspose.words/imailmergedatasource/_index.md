---
title: "IMailMergeDataSource"
linktitle: "IMailMergeDataSource"
second_title: "Aspose.Words Java için"
description: "Bu arabirimi, Java'da nesneler listesi gibi özel bir veri kaynağından birleştirme (mail merge) yapabilmek için uygulayın."
type: docs
weight: 776
url: /tr/java/com.aspose.words/imailmergedatasource/
---
```
public interface IMailMergeDataSource
```

Bu arabirimi, nesneler listesi gibi özel bir veri kaynağından birleştirme yapabilmek için uygulayın. Ana‑detay verileri de desteklenir.

 **Remarks:** 

Bir veri kaynağı oluşturulduğunda, BOF (ilk kayıttan önce) konumuna işaret edecek şekilde başlatılmalıdır. Aspose.Words birleştirme motoru, bir sonraki kayda ilerlemek için [moveNext()](../../com.aspose.words/imailmergedatasource/\#moveNext) yöntemini çağıracak ve ardından belgede veya geçerli birleştirme bölgesinde karşılaştığı her birleştirme alanı için **M:Aspose.Words.MailMerging.IMailMergeDataSource.GetValue(System.String,System.Object@)** yöntemini çağıracaktır.

 **Examples:** 

Özel bir nesne biçimindeki veri kaynağıyla birleştirme (mail merge) nasıl yürütülür gösterir.

```

 public void customDataSource() throws Exception {
     // Create a destination document for the mail merge
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.insertField(" MERGEFIELD FullName ");
     builder.insertParagraph();
     builder.insertField(" MERGEFIELD Address ");

     // Create some data that we will use in the mail merge
     CustomerList customers = new CustomerList();
     customers.add(new Customer("Thomas Hardy", "120 Hanover Sq., London"));
     customers.add(new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"));

     // To be able to mail merge from your own data source, it must be wrapped
     // into an object that implements the IMailMergeDataSource interface
     CustomerMailMergeDataSource customersDataSource = new CustomerMailMergeDataSource(customers);

     // Now you can pass your data source into Aspose.Words
     doc.getMailMerge().execute(customersDataSource);

     doc.save(getArtifactsDir() + "MailMergeCustom.CustomDataSource.docx");
 }

 // An example of a "data entity" class in your application.
 public class Customer {
     public Customer(final String aFullName, final String anAddress) {
         mFullName = aFullName;
         mAddress = anAddress;
     }

     public String getFullName() {
         return mFullName;
     }

     public void setFullName(final String value) {
         mFullName = value;
     }

     public String getAddress() {
         return mAddress;
     }

     public void setAddress(final String value) {
         mAddress = value;
     }

     private String mFullName;
     private String mAddress;
 }

 // An example of a typed collection that contains your "data" objects.
 public class CustomerList extends ArrayList {
     public Customer get(final int index) {
         return (Customer) super.get(index);
     }

     public void set(final int index, final Customer value) {
         super.set(index, value);
     }
 }

 // A custom mail merge data source that you implement to allow Aspose.Words
 // to mail merge data from your Customer objects into Microsoft Word documents.
 public class CustomerMailMergeDataSource implements IMailMergeDataSource {
     public CustomerMailMergeDataSource(final CustomerList customers) {
         mCustomers = customers;

         // When the data source is initialized, it must be positioned before the first record.
         mRecordIndex = -1;
     }

     // The name of the data source. Used by Aspose.Words only when executing mail merge with repeatable regions.
     public String getTableName() {
         return "Customer";
     }

     // Aspose.Words calls this method to get a value for every data field.
     public boolean getValue(final String fieldName, final Ref fieldValue) throws Exception {
         if (fieldName.equals("FullName")) {
             fieldValue.set(mCustomers.get(mRecordIndex).getFullName());
             return true;
         } else if (fieldName.equals("Address")) {
             fieldValue.set(mCustomers.get(mRecordIndex).getAddress());
             return true;
         } else {
             // A field with this name was not found,
             // return false to the Aspose.Words mail merge engine
             fieldValue.set(null);
             return false;
         }
     }

     // A standard implementation for moving to a next record in a collection.
     public boolean moveNext() {
         if (!isEof()) mRecordIndex++;

         return (!isEof());
     }

     public IMailMergeDataSource getChildDataSource(final String tableName) {
         return null;
     }

     private boolean isEof() {
         return (mRecordIndex >= mCustomers.size());
     }

     private final CustomerList mCustomers;
     private int mRecordIndex;
 }
 
```
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getChildDataSource(String tableName)](#getChildDataSource-java.lang.String) | Aspose.Words birleştirme motoru, iç içe birleştirme bölgesinin başlangıcına rastladığında bu yöntemi çağırır. |
| [getTableName()](#getTableName) | Veri kaynağının adını döndürür. |
| [getValue(String fieldName, Ref fieldValue)](#getValue-java.lang.String-com.aspose.words.ref.Ref) |  |
| [moveNext()](#moveNext) | Veri kaynağındaki bir sonraki kayda ilerler. |
### getChildDataSource(String tableName) {#getChildDataSource-java.lang.String}
```
public abstract IMailMergeDataSource getChildDataSource(String tableName)
```


Aspose.Words birleştirme motoru, iç içe birleştirme bölgesinin başlangıcına rastladığında bu yöntemi çağırır.

 **Remarks:** 

Aspose.Words birleştirme motoru, bir birleştirme bölgesini veriyle doldururken MERGEFIELD TableStart:TableName biçiminde iç içe birleştirme bölgesinin başlangıcına rastladığında, geçerli veri kaynağı nesnesinde [getChildDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasource/\#getChildDataSource-java.lang.String) yöntemini çağırır. Uygulamanız, geçerli ana kaydın alt kayıtlarına erişim sağlayacak yeni bir veri kaynağı nesnesi döndürmelidir. Aspose.Words, iç içe birleştirme bölgesini doldurmak için döndürülen veri kaynağını kullanacaktır.

Aşağıda, [getChildDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasource/\#getChildDataSource-java.lang.String) uygulamasının uyması gereken kurallar yer almaktadır.

Bu veri kaynağı nesnesi tarafından temsil edilen tablonun, belirtilen ada sahip ilişkili bir alt (detay) tablosu varsa, uygulamanız mevcut kaydın alt kayıtlarına erişim sağlayacak yeni bir [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) nesnesi döndürmelidir. Buna bir örnek Orders / OrderDetails ilişkisidir. Şu anki [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) nesnesinin Orders tablosunu temsil ettiğini ve mevcut bir sipariş kaydına sahip olduğunu varsayalım. Sonra, Aspose.Words belgede "MERGEFIELD TableStart:OrderDetails" ile karşılaşır ve [getChildDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasource/\#getChildDataSource-java.lang.String) yöntemini çağırır. Aspose.Words'un mevcut sipariş için OrderDetails kaydına erişebilmesini sağlayacak bir [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) nesnesi oluşturmalı ve döndürmelisiniz.

Bu veri kaynağı nesnesinin belirtilen ada sahip tabloyla bir ilişkisi yoksa, belirtilen tablonun tüm kayıtlarına erişim sağlayacak bir [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) nesnesi döndürmelisiniz.

Belirtilen ada sahip bir tablo mevcut değilse, uygulamanız  null  döndürmelidir.

 **Examples:** 

Özel bir nesne biçimindeki veri kaynağıyla birleştirme (mail merge) nasıl yürütülür gösterir.

```

 public void customDataSource() throws Exception {
     // Create a destination document for the mail merge
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.insertField(" MERGEFIELD FullName ");
     builder.insertParagraph();
     builder.insertField(" MERGEFIELD Address ");

     // Create some data that we will use in the mail merge
     CustomerList customers = new CustomerList();
     customers.add(new Customer("Thomas Hardy", "120 Hanover Sq., London"));
     customers.add(new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"));

     // To be able to mail merge from your own data source, it must be wrapped
     // into an object that implements the IMailMergeDataSource interface
     CustomerMailMergeDataSource customersDataSource = new CustomerMailMergeDataSource(customers);

     // Now you can pass your data source into Aspose.Words
     doc.getMailMerge().execute(customersDataSource);

     doc.save(getArtifactsDir() + "MailMergeCustom.CustomDataSource.docx");
 }

 // An example of a "data entity" class in your application.
 public class Customer {
     public Customer(final String aFullName, final String anAddress) {
         mFullName = aFullName;
         mAddress = anAddress;
     }

     public String getFullName() {
         return mFullName;
     }

     public void setFullName(final String value) {
         mFullName = value;
     }

     public String getAddress() {
         return mAddress;
     }

     public void setAddress(final String value) {
         mAddress = value;
     }

     private String mFullName;
     private String mAddress;
 }

 // An example of a typed collection that contains your "data" objects.
 public class CustomerList extends ArrayList {
     public Customer get(final int index) {
         return (Customer) super.get(index);
     }

     public void set(final int index, final Customer value) {
         super.set(index, value);
     }
 }

 // A custom mail merge data source that you implement to allow Aspose.Words
 // to mail merge data from your Customer objects into Microsoft Word documents.
 public class CustomerMailMergeDataSource implements IMailMergeDataSource {
     public CustomerMailMergeDataSource(final CustomerList customers) {
         mCustomers = customers;

         // When the data source is initialized, it must be positioned before the first record.
         mRecordIndex = -1;
     }

     // The name of the data source. Used by Aspose.Words only when executing mail merge with repeatable regions.
     public String getTableName() {
         return "Customer";
     }

     // Aspose.Words calls this method to get a value for every data field.
     public boolean getValue(final String fieldName, final Ref fieldValue) throws Exception {
         if (fieldName.equals("FullName")) {
             fieldValue.set(mCustomers.get(mRecordIndex).getFullName());
             return true;
         } else if (fieldName.equals("Address")) {
             fieldValue.set(mCustomers.get(mRecordIndex).getAddress());
             return true;
         } else {
             // A field with this name was not found,
             // return false to the Aspose.Words mail merge engine
             fieldValue.set(null);
             return false;
         }
     }

     // A standard implementation for moving to a next record in a collection.
     public boolean moveNext() {
         if (!isEof()) mRecordIndex++;

         return (!isEof());
     }

     public IMailMergeDataSource getChildDataSource(final String tableName) {
         return null;
     }

     private boolean isEof() {
         return (mRecordIndex >= mCustomers.size());
     }

     private final CustomerList mCustomers;
     private int mRecordIndex;
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tableName | java.lang.String | Şablon belgesinde belirtilen birleştirme bölgesi adıdır. Büyük/küçük harfe duyarsız. |

**Returns:**
[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) - A data source object that will provide access to the data records of the specified table.
### getTableName() {#getTableName}
```
public abstract String getTableName()
```


Veri kaynağının adını döndürür.

 **Remarks:** 

[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) uyguluyorsanız, bu özelliktan veri kaynağının adını döndürün.

Aspose.Words, bu adı şablon belgesinde belirtilen birleştirme bölgesi adıyla eşleştirmek için kullanır. Veri kaynağı adı ile birleştirme bölgesi adı arasındaki karşılaştırma büyük/küçük harfe duyarlı değildir.

 **Examples:** 

Özel bir nesne biçimindeki veri kaynağıyla birleştirme (mail merge) nasıl yürütülür gösterir.

```

 public void customDataSource() throws Exception {
     // Create a destination document for the mail merge
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.insertField(" MERGEFIELD FullName ");
     builder.insertParagraph();
     builder.insertField(" MERGEFIELD Address ");

     // Create some data that we will use in the mail merge
     CustomerList customers = new CustomerList();
     customers.add(new Customer("Thomas Hardy", "120 Hanover Sq., London"));
     customers.add(new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"));

     // To be able to mail merge from your own data source, it must be wrapped
     // into an object that implements the IMailMergeDataSource interface
     CustomerMailMergeDataSource customersDataSource = new CustomerMailMergeDataSource(customers);

     // Now you can pass your data source into Aspose.Words
     doc.getMailMerge().execute(customersDataSource);

     doc.save(getArtifactsDir() + "MailMergeCustom.CustomDataSource.docx");
 }

 // An example of a "data entity" class in your application.
 public class Customer {
     public Customer(final String aFullName, final String anAddress) {
         mFullName = aFullName;
         mAddress = anAddress;
     }

     public String getFullName() {
         return mFullName;
     }

     public void setFullName(final String value) {
         mFullName = value;
     }

     public String getAddress() {
         return mAddress;
     }

     public void setAddress(final String value) {
         mAddress = value;
     }

     private String mFullName;
     private String mAddress;
 }

 // An example of a typed collection that contains your "data" objects.
 public class CustomerList extends ArrayList {
     public Customer get(final int index) {
         return (Customer) super.get(index);
     }

     public void set(final int index, final Customer value) {
         super.set(index, value);
     }
 }

 // A custom mail merge data source that you implement to allow Aspose.Words
 // to mail merge data from your Customer objects into Microsoft Word documents.
 public class CustomerMailMergeDataSource implements IMailMergeDataSource {
     public CustomerMailMergeDataSource(final CustomerList customers) {
         mCustomers = customers;

         // When the data source is initialized, it must be positioned before the first record.
         mRecordIndex = -1;
     }

     // The name of the data source. Used by Aspose.Words only when executing mail merge with repeatable regions.
     public String getTableName() {
         return "Customer";
     }

     // Aspose.Words calls this method to get a value for every data field.
     public boolean getValue(final String fieldName, final Ref fieldValue) throws Exception {
         if (fieldName.equals("FullName")) {
             fieldValue.set(mCustomers.get(mRecordIndex).getFullName());
             return true;
         } else if (fieldName.equals("Address")) {
             fieldValue.set(mCustomers.get(mRecordIndex).getAddress());
             return true;
         } else {
             // A field with this name was not found,
             // return false to the Aspose.Words mail merge engine
             fieldValue.set(null);
             return false;
         }
     }

     // A standard implementation for moving to a next record in a collection.
     public boolean moveNext() {
         if (!isEof()) mRecordIndex++;

         return (!isEof());
     }

     public IMailMergeDataSource getChildDataSource(final String tableName) {
         return null;
     }

     private boolean isEof() {
         return (mRecordIndex >= mCustomers.size());
     }

     private final CustomerList mCustomers;
     private int mRecordIndex;
 }
 
```

**Returns:**
java.lang.String - Veri kaynağının adı. Veri kaynağının adı yoksa boş bir dizedir.
### getValue(String fieldName, Ref fieldValue) {#getValue-java.lang.String-com.aspose.words.ref.Ref}
```
public abstract boolean getValue(String fieldName, Ref fieldValue)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fieldName | java.lang.String |  |
| fieldValue | [Ref](../../com.aspose.words.ref/ref/) |  |

**Returns:**
boolean
### moveNext() {#moveNext}
```
public abstract boolean moveNext()
```


Veri kaynağındaki bir sonraki kayda ilerler.

 **Examples:** 

Özel bir nesne biçimindeki veri kaynağıyla birleştirme (mail merge) nasıl yürütülür gösterir.

```

 public void customDataSource() throws Exception {
     // Create a destination document for the mail merge
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.insertField(" MERGEFIELD FullName ");
     builder.insertParagraph();
     builder.insertField(" MERGEFIELD Address ");

     // Create some data that we will use in the mail merge
     CustomerList customers = new CustomerList();
     customers.add(new Customer("Thomas Hardy", "120 Hanover Sq., London"));
     customers.add(new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"));

     // To be able to mail merge from your own data source, it must be wrapped
     // into an object that implements the IMailMergeDataSource interface
     CustomerMailMergeDataSource customersDataSource = new CustomerMailMergeDataSource(customers);

     // Now you can pass your data source into Aspose.Words
     doc.getMailMerge().execute(customersDataSource);

     doc.save(getArtifactsDir() + "MailMergeCustom.CustomDataSource.docx");
 }

 // An example of a "data entity" class in your application.
 public class Customer {
     public Customer(final String aFullName, final String anAddress) {
         mFullName = aFullName;
         mAddress = anAddress;
     }

     public String getFullName() {
         return mFullName;
     }

     public void setFullName(final String value) {
         mFullName = value;
     }

     public String getAddress() {
         return mAddress;
     }

     public void setAddress(final String value) {
         mAddress = value;
     }

     private String mFullName;
     private String mAddress;
 }

 // An example of a typed collection that contains your "data" objects.
 public class CustomerList extends ArrayList {
     public Customer get(final int index) {
         return (Customer) super.get(index);
     }

     public void set(final int index, final Customer value) {
         super.set(index, value);
     }
 }

 // A custom mail merge data source that you implement to allow Aspose.Words
 // to mail merge data from your Customer objects into Microsoft Word documents.
 public class CustomerMailMergeDataSource implements IMailMergeDataSource {
     public CustomerMailMergeDataSource(final CustomerList customers) {
         mCustomers = customers;

         // When the data source is initialized, it must be positioned before the first record.
         mRecordIndex = -1;
     }

     // The name of the data source. Used by Aspose.Words only when executing mail merge with repeatable regions.
     public String getTableName() {
         return "Customer";
     }

     // Aspose.Words calls this method to get a value for every data field.
     public boolean getValue(final String fieldName, final Ref fieldValue) throws Exception {
         if (fieldName.equals("FullName")) {
             fieldValue.set(mCustomers.get(mRecordIndex).getFullName());
             return true;
         } else if (fieldName.equals("Address")) {
             fieldValue.set(mCustomers.get(mRecordIndex).getAddress());
             return true;
         } else {
             // A field with this name was not found,
             // return false to the Aspose.Words mail merge engine
             fieldValue.set(null);
             return false;
         }
     }

     // A standard implementation for moving to a next record in a collection.
     public boolean moveNext() {
         if (!isEof()) mRecordIndex++;

         return (!isEof());
     }

     public IMailMergeDataSource getChildDataSource(final String tableName) {
         return null;
     }

     private boolean isEof() {
         return (mRecordIndex >= mCustomers.size());
     }

     private final CustomerList mCustomers;
     private int mRecordIndex;
 }
 
```

**Returns:**
boolean -  true  bir sonraki kayda başarıyla geçildiyse;  false  veri kaynağının sonuna ulaşıldıysa.
