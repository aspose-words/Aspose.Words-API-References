---
title: "IMailMergeDataSource"
linktitle: "IMailMergeDataSource"
second_title: "Aspose.Words لـ Java"
description: "قم بتنفيذ هذه الواجهة للسماح بدمج البريد من مصدر بيانات مخصص مثل قائمة من الكائنات في جافا."
type: docs
weight: 776
url: /ar/java/com.aspose.words/imailmergedatasource/
---
```
public interface IMailMergeDataSource
```

قم بتنفيذ هذه الواجهة للسماح بدمج البريد من مصدر بيانات مخصص، مثل قائمة من الكائنات. كما يتم دعم بيانات الرئيس‑التفصيل.

 **Remarks:** 

عند إنشاء مصدر بيانات، يجب تهيئته للإشارة إلى BOF (قبل السجل الأول). سيقوم محرك دمج البريد في Aspose.Words باستدعاء [moveNext()](../../com.aspose.words/imailmergedatasource/\#moveNext) للتقدم إلى السجل التالي ثم يستدعي **M:Aspose.Words.MailMerging.IMailMergeDataSource.GetValue(System.String,System.Object@)** لكل حقل دمج يصادفه في المستند أو منطقة دمج البريد الحالية.

 **Examples:** 

يظهر كيفية تنفيذ دمج البريد باستخدام مصدر بيانات على شكل كائن مخصص.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getChildDataSource(String tableName)](#getChildDataSource-java.lang.String) | يقوم محرك دمج البريد في Aspose.Words باستدعاء هذه الطريقة عندما يصادف بداية منطقة دمج بريد متداخلة. |
| [getTableName()](#getTableName) | يرجع اسم مصدر البيانات. |
| [getValue(String fieldName, Ref fieldValue)](#getValue-java.lang.String-com.aspose.words.ref.Ref) |  |
| [moveNext()](#moveNext) | يتقدم إلى السجل التالي في مصدر البيانات. |
### getChildDataSource(String tableName) {#getChildDataSource-java.lang.String}
```
public abstract IMailMergeDataSource getChildDataSource(String tableName)
```


يقوم محرك دمج البريد في Aspose.Words باستدعاء هذه الطريقة عندما يصادف بداية منطقة دمج بريد متداخلة.

 **Remarks:** 

عند قيام محركات دمج البريد في Aspose.Words بملء منطقة دمج البريد بالبيانات وصادفت بداية منطقة دمج بريد متداخلة على شكل MERGEFIELD TableStart:TableName، فإنها تستدعي [getChildDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasource/\#getChildDataSource-java.lang.String) على كائن مصدر البيانات الحالي. يحتاج تنفيذك إلى إرجاع كائن مصدر بيانات جديد يتيح الوصول إلى سجلات الأطفال للسجل الأب الحالي. سيستخدم Aspose.Words مصدر البيانات المرتجع لملء منطقة دمج البريد المتداخلة.

فيما يلي القواعد التي يجب أن يتبعها تنفيذ [getChildDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasource/\#getChildDataSource-java.lang.String).

إذا كان الجدول الممثّل بهذا الكائن مصدر البيانات يحتوي على جدول طفل (تفصيل) مرتبط بالاسم المحدد، فإن تنفيذك يحتاج إلى إرجاع كائن [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) جديد يتيح الوصول إلى سجلات الطفل للسجل الحالي. مثال على ذلك هو علاقة Orders / OrderDetails. لنفترض أن كائن [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) الحالي يمثل جدول Orders ولديه سجل طلب حالي. بعد ذلك، يصادف Aspose.Words \"MERGEFIELD TableStart:OrderDetails\" في المستند ويستدعي [getChildDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasource/\#getChildDataSource-java.lang.String). تحتاج إلى إنشاء وإرجاع كائن [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) يسمح لـ Aspose.Words بالوصول إلى سجل OrderDetails للطلب الحالي.

إذا لم يكن لهذا الكائن مصدر البيانات علاقة بالجدول الذي يحمل الاسم المحدد، فستحتاج إلى إرجاع كائن [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) يتيح الوصول إلى جميع سجلات الجدول المحدد.

إذا لم يكن هناك جدول بالاسم المحدد، يجب على تنفيذك إرجاع  null .

 **Examples:** 

يظهر كيفية تنفيذ دمج البريد باستخدام مصدر بيانات على شكل كائن مخصص.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| tableName | java.lang.String | اسم منطقة دمج البريد كما هو محدد في مستند القالب. غير حساس لحالة الأحرف. |

**Returns:**
[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) - A data source object that will provide access to the data records of the specified table.
### getTableName() {#getTableName}
```
public abstract String getTableName()
```


يرجع اسم مصدر البيانات.

 **Remarks:** 

إذا كنت تقوم بتنفيذ [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/)، فأرجع اسم مصدر البيانات من هذه الخاصية.

يستخدم Aspose.Words هذا الاسم لمطابقته مع اسم منطقة دمج البريد المحدد في مستند القالب. المقارنة بين اسم مصدر البيانات واسم منطقة دمج البريد غير حساسة لحالة الأحرف.

 **Examples:** 

يظهر كيفية تنفيذ دمج البريد باستخدام مصدر بيانات على شكل كائن مخصص.

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
java.lang.String - اسم مصدر البيانات. سلسلة فارغة إذا لم يكن لمصدر البيانات اسم.
### getValue(String fieldName, Ref fieldValue) {#getValue-java.lang.String-com.aspose.words.ref.Ref}
```
public abstract boolean getValue(String fieldName, Ref fieldValue)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fieldName | java.lang.String |  |
| fieldValue | [Ref](../../com.aspose.words.ref/ref/) |  |

**Returns:**
boolean
### moveNext() {#moveNext}
```
public abstract boolean moveNext()
```


يتقدم إلى السجل التالي في مصدر البيانات.

 **Examples:** 

يظهر كيفية تنفيذ دمج البريد باستخدام مصدر بيانات على شكل كائن مخصص.

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
boolean -  true  إذا تم الانتقال إلى السجل التالي بنجاح؛  false  إذا تم الوصول إلى نهاية مصدر البيانات.
