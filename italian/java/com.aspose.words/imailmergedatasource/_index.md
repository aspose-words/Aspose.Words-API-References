---
title: "IMailMergeDataSource"
linktitle: "IMailMergeDataSource"
second_title: "Aspose.Words per Java"
description: "Implementa questa interfaccia per consentire il mail merge da una fonte dati personalizzata, ad esempio un elenco di oggetti in Java."
type: docs
weight: 776
url: /it/java/com.aspose.words/imailmergedatasource/
---
```
public interface IMailMergeDataSource
```

Implementa questa interfaccia per consentire il mail merge da una fonte dati personalizzata, ad esempio un elenco di oggetti. Sono supportati anche i dati master-detail.

 **Remarks:** 

Quando una fonte dati viene creata, dovrebbe essere inizializzata per puntare al BOF (prima del primo record). Il motore di mail merge di Aspose.Words invocherà [moveNext()](../../com.aspose.words/imailmergedatasource/\#moveNext) per avanzare al record successivo e poi invocherà **M:Aspose.Words.MailMerging.IMailMergeDataSource.GetValue(System.String,System.Object@)** per ogni campo di merge incontrato nel documento o nella regione di mail merge corrente.

 **Examples:** 

Mostra come eseguire un mail merge con una fonte dati sotto forma di oggetto personalizzato.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getChildDataSource(String tableName)](#getChildDataSource-java.lang.String) | Il motore di mail merge di Aspose.Words invoca questo metodo quando rileva l'inizio di una regione di mail merge annidata. |
| [getTableName()](#getTableName) | Restituisce il nome della fonte dati. |
| [getValue(String fieldName, Ref fieldValue)](#getValue-java.lang.String-com.aspose.words.ref.Ref) |  |
| [moveNext()](#moveNext) | Avanza al record successivo nella fonte dati. |
### getChildDataSource(String tableName) {#getChildDataSource-java.lang.String}
```
public abstract IMailMergeDataSource getChildDataSource(String tableName)
```


Il motore di mail merge di Aspose.Words invoca questo metodo quando rileva l'inizio di una regione di mail merge annidata.

 **Remarks:** 

Quando i motori di mail merge di Aspose.Words popolano una regione di mail merge con dati e incontrano l'inizio di una regione di mail merge annidata nella forma MERGEFIELD TableStart:TableName, invocano [getChildDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasource/\#getChildDataSource-java.lang.String) sull'oggetto fonte dati corrente. La tua implementazione deve restituire un nuovo oggetto fonte dati che fornisca l'accesso ai record figlio del record padre corrente. Aspose.Words utilizzerà la fonte dati restituita per popolare la regione di mail merge annidata.

Di seguito sono riportate le regole che l'implementazione di [getChildDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasource/\#getChildDataSource-java.lang.String) deve rispettare.

Se la tabella rappresentata da questo oggetto fonte dati ha una tabella figlio (dettaglio) correlata con il nome specificato, la tua implementazione deve restituire un nuovo oggetto [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) che fornisca l'accesso ai record figlio del record corrente. Un esempio è la relazione Ordini / DettagliOrdine. Supponiamo che l'oggetto [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) corrente rappresenti la tabella Ordini e abbia un record ordine corrente. Successivamente, Aspose.Words incontra "MERGEFIELD TableStart:OrderDetails" nel documento e invoca [getChildDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasource/\#getChildDataSource-java.lang.String). Devi creare e restituire un oggetto [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) che consenta ad Aspose.Words di accedere al record DettagliOrdine per l'ordine corrente.

Se questo oggetto fonte dati non ha una relazione con la tabella dal nome specificato, devi restituire un oggetto [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) che fornisca l'accesso a tutti i record della tabella specificata.

Se una tabella con il nome specificato non esiste, la tua implementazione dovrebbe restituire  null .

 **Examples:** 

Mostra come eseguire un mail merge con una fonte dati sotto forma di oggetto personalizzato.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tableName | java.lang.String | Il nome della regione di mail merge come specificato nel documento modello. Non sensibile al maiuscolo/minuscolo. |

**Returns:**
[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) - A data source object that will provide access to the data records of the specified table.
### getTableName() {#getTableName}
```
public abstract String getTableName()
```


Restituisce il nome della fonte dati.

 **Remarks:** 

Se stai implementando [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/), restituisci il nome della fonte dati da questa proprietà.

Aspose.Words utilizza questo nome per confrontarlo con il nome della regione di mail merge specificato nel documento modello. Il confronto tra il nome della fonte dati e il nome della regione di mail merge non è sensibile al maiuscolo/minuscolo.

 **Examples:** 

Mostra come eseguire un mail merge con una fonte dati sotto forma di oggetto personalizzato.

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
java.lang.String - Il nome della fonte dati. Stringa vuota se la fonte dati non ha un nome.
### getValue(String fieldName, Ref fieldValue) {#getValue-java.lang.String-com.aspose.words.ref.Ref}
```
public abstract boolean getValue(String fieldName, Ref fieldValue)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldName | java.lang.String |  |
| fieldValue | [Ref](../../com.aspose.words.ref/ref/) |  |

**Returns:**
boolean
### moveNext() {#moveNext}
```
public abstract boolean moveNext()
```


Avanza al record successivo nella fonte dati.

 **Examples:** 

Mostra come eseguire un mail merge con una fonte dati sotto forma di oggetto personalizzato.

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
boolean -  true  se è stato spostato al record successivo con successo;  false  se è stato raggiunto la fine della fonte dati.
