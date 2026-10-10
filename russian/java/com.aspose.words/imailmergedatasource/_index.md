---
title: "IMailMergeDataSource"
linktitle: "IMailMergeDataSource"
second_title: "Aspose.Words для Java"
description: "Реализуйте этот интерфейс, чтобы обеспечить слияние писем из пользовательского источника данных, например списка объектов в Java."
type: docs
weight: 776
url: /ru/java/com.aspose.words/imailmergedatasource/
---
```
public interface IMailMergeDataSource
```

Реализуйте этот интерфейс, чтобы обеспечить слияние писем из пользовательского источника данных, например списка объектов. Также поддерживаются данные мастер‑деталь.

 **Remarks:** 

Когда создаётся источник данных, его следует инициализировать, указывая на BOF (до первой записи). Движок слияния писем Aspose.Words вызовет [moveNext()](../../com.aspose.words/imailmergedatasource/\#moveNext), чтобы перейти к следующей записи, а затем вызовет **M:Aspose.Words.MailMerging.IMailMergeDataSource.GetValue(System.String,System.Object@)** для каждого поля слияния, которое он встретит в документе или текущем регионе слияния.

 **Examples:** 

Показывает, как выполнить слияние писем с источником данных в виде пользовательского объекта.

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
## Методы

| Метод | Описание |
| --- | --- |
| [getChildDataSource(String tableName)](#getChildDataSource-java.lang.String) | Движок слияния писем Aspose.Words вызывает этот метод, когда встречает начало вложенного региона слияния писем. |
| [getTableName()](#getTableName) | Возвращает имя источника данных. |
| [getValue(String fieldName, Ref fieldValue)](#getValue-java.lang.String-com.aspose.words.ref.Ref) |  |
| [moveNext()](#moveNext) | Переходит к следующей записи в источнике данных. |
### getChildDataSource(String tableName) {#getChildDataSource-java.lang.String}
```
public abstract IMailMergeDataSource getChildDataSource(String tableName)
```


Движок слияния писем Aspose.Words вызывает этот метод, когда встречает начало вложенного региона слияния писем.

 **Remarks:** 

Когда движок слияния писем Aspose.Words заполняет регион слияния данными и встречает начало вложенного региона слияния в виде MERGEFIELD TableStart:TableName, он вызывает [getChildDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasource/\#getChildDataSource-java.lang.String) у текущего объекта источника данных. Ваша реализация должна вернуть новый объект источника данных, который предоставит доступ к дочерним записям текущей родительской записи. Aspose.Words использует возвращённый источник данных для заполнения вложенного региона слияния.

Ниже перечислены правила, которым должна соответствовать реализация [getChildDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasource/\#getChildDataSource-java.lang.String).

Если таблица, представляемая этим объектом источника данных, имеет связанную дочернюю (детальную) таблицу с указанным именем, ваша реализация должна вернуть новый объект [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/), который предоставит доступ к дочерним записям текущей записи. Примером является связь Orders / OrderDetails. Предположим, что текущий объект [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) представляет таблицу Orders и содержит текущую запись заказа. Затем Aspose.Words встречает в документе \"MERGEFIELD TableStart:OrderDetails\" и вызывает [getChildDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasource/\#getChildDataSource-java.lang.String). Вам необходимо создать и вернуть объект [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/), который позволит Aspose.Words получить доступ к записи OrderDetails для текущего заказа.

Если у этого объекта источника данных нет связи с таблицей с указанным именем, вам нужно вернуть объект [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/), который предоставит доступ ко всем записям указанной таблицы.

Если таблица с указанным именем не существует, ваша реализация должна вернуть  null .

 **Examples:** 

Показывает, как выполнить слияние писем с источником данных в виде пользовательского объекта.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| tableName | java.lang.String | Имя региона слияния писем, указанное в шаблоне документа. Без учёта регистра. |

**Returns:**
[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) - A data source object that will provide access to the data records of the specified table.
### getTableName() {#getTableName}
```
public abstract String getTableName()
```


Возвращает имя источника данных.

 **Remarks:** 

Если вы реализуете [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/), возвращайте имя источника данных из этого свойства.

Aspose.Words использует это имя для сопоставления с именем региона слияния писем, указанным в шаблоне документа. Сравнение имени источника данных и имени региона слияния писем не чувствительно к регистру.

 **Examples:** 

Показывает, как выполнить слияние писем с источником данных в виде пользовательского объекта.

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
java.lang.String — имя источника данных. Пустая строка, если у источника данных нет имени.
### getValue(String fieldName, Ref fieldValue) {#getValue-java.lang.String-com.aspose.words.ref.Ref}
```
public abstract boolean getValue(String fieldName, Ref fieldValue)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldName | java.lang.String |  |
| fieldValue | [Ref](../../com.aspose.words.ref/ref/) |  |

**Returns:**
boolean
### moveNext() {#moveNext}
```
public abstract boolean moveNext()
```


Переходит к следующей записи в источнике данных.

 **Examples:** 

Показывает, как выполнить слияние писем с источником данных в виде пользовательского объекта.

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
boolean —  true  если успешно переместились к следующей записи;  false  если достигнут конец источника данных.
