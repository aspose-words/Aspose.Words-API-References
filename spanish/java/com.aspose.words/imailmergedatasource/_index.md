---
title: "IMailMergeDataSource"
linktitle: "IMailMergeDataSource"
second_title: "Aspose.Words para Java"
description: "Implemente esta interfaz para permitir la combinación de correspondencia desde una fuente de datos personalizada, como una lista de objetos en Java."
type: docs
weight: 776
url: /es/java/com.aspose.words/imailmergedatasource/
---
```
public interface IMailMergeDataSource
```

Implemente esta interfaz para permitir la combinación de correspondencia desde una fuente de datos personalizada, como una lista de objetos. También se admite datos maestro‑detalle.

 **Remarks:** 

Cuando se crea una fuente de datos, debe inicializarse para apuntar a BOF (antes del primer registro). El motor de combinación de correspondencia de Aspose.Words invocará [moveNext()](../../com.aspose.words/imailmergedatasource/\#moveNext) para avanzar al siguiente registro y luego invocará **M:Aspose.Words.MailMerging.IMailMergeDataSource.GetValue(System.String,System.Object@)** para cada campo de combinación que encuentre en el documento o en la región de combinación de correspondencia actual.

 **Examples:** 

Muestra cómo ejecutar una combinación de correspondencia con una fuente de datos en forma de objeto personalizado.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [getChildDataSource(String tableName)](#getChildDataSource-java.lang.String) | El motor de combinación de correspondencia de Aspose.Words invoca este método cuando encuentra el inicio de una región de combinación de correspondencia anidada. |
| [getTableName()](#getTableName) | Devuelve el nombre de la fuente de datos. |
| [getValue(String fieldName, Ref fieldValue)](#getValue-java.lang.String-com.aspose.words.ref.Ref) |  |
| [moveNext()](#moveNext) | Avanza al siguiente registro en la fuente de datos. |
### getChildDataSource(String tableName) {#getChildDataSource-java.lang.String}
```
public abstract IMailMergeDataSource getChildDataSource(String tableName)
```


El motor de combinación de correspondencia de Aspose.Words invoca este método cuando encuentra el inicio de una región de combinación de correspondencia anidada.

 **Remarks:** 

Cuando los motores de combinación de correspondencia de Aspose.Words rellenan una región de combinación con datos y encuentran el inicio de una región de combinación anidada en forma de MERGEFIELD TableStart:TableName, invocan [getChildDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasource/\#getChildDataSource-java.lang.String) en el objeto de fuente de datos actual. Su implementación debe devolver un nuevo objeto de fuente de datos que proporcione acceso a los registros hijos del registro padre actual. Aspose.Words utilizará la fuente de datos devuelta para rellenar la región de combinación anidada.

A continuación se presentan las reglas que debe seguir la implementación de [getChildDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasource/\#getChildDataSource-java.lang.String).

Si la tabla representada por este objeto de fuente de datos tiene una tabla hija (detalle) relacionada con el nombre especificado, entonces su implementación debe devolver un nuevo objeto [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) que proporcione acceso a los registros hijos del registro actual. Un ejemplo de esto es la relación Pedidos / DetallesPedido. Supongamos que el objeto [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) actual representa la tabla Pedidos y tiene un registro de pedido actual. A continuación, Aspose.Words encuentra \"MERGEFIELD TableStart:OrderDetails\" en el documento e invoca [getChildDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasource/\#getChildDataSource-java.lang.String). Necesita crear y devolver un objeto [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) que permita a Aspose.Words acceder al registro OrderDetails del pedido actual.

Si este objeto de fuente de datos no tiene una relación con la tabla del nombre especificado, entonces debe devolver un objeto [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) que proporcione acceso a todos los registros de la tabla especificada.

Si no existe una tabla con el nombre especificado, su implementación debe devolver  null .

 **Examples:** 

Muestra cómo ejecutar una combinación de correspondencia con una fuente de datos en forma de objeto personalizado.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tableName | java.lang.String | El nombre de la región de combinación de correspondencia según se especifica en el documento plantilla. No distingue entre mayúsculas y minúsculas. |

**Returns:**
[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) - A data source object that will provide access to the data records of the specified table.
### getTableName() {#getTableName}
```
public abstract String getTableName()
```


Devuelve el nombre de la fuente de datos.

 **Remarks:** 

Si está implementando [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/), devuelva el nombre de la fuente de datos desde esta propiedad.

Aspose.Words utiliza este nombre para compararlo con el nombre de la región de combinación de correspondencia especificado en el documento plantilla. La comparación entre el nombre de la fuente de datos y el nombre de la región de combinación no distingue entre mayúsculas y minúsculas.

 **Examples:** 

Muestra cómo ejecutar una combinación de correspondencia con una fuente de datos en forma de objeto personalizado.

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
java.lang.String - El nombre de la fuente de datos. Cadena vacía si la fuente de datos no tiene nombre.
### getValue(String fieldName, Ref fieldValue) {#getValue-java.lang.String-com.aspose.words.ref.Ref}
```
public abstract boolean getValue(String fieldName, Ref fieldValue)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fieldName | java.lang.String |  |
| fieldValue | [Ref](../../com.aspose.words.ref/ref/) |  |

**Returns:**
boolean
### moveNext() {#moveNext}
```
public abstract boolean moveNext()
```


Avanza al siguiente registro en la fuente de datos.

 **Examples:** 

Muestra cómo ejecutar una combinación de correspondencia con una fuente de datos en forma de objeto personalizado.

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
boolean -  true  si se avanzó al siguiente registro con éxito;  false  si se alcanzó el final de la fuente de datos.
