---
title: "IMailMergeDataSourceRoot"
linktitle: "IMailMergeDataSourceRoot"
second_title: "Aspose.Words für Java"
description: "Implementieren Sie dieses Interface, um den Seriendruck aus einer benutzerdefinierten Datenquelle mit Master-Detail-Daten in Java zu ermöglichen."
type: docs
weight: 777
url: /de/java/com.aspose.words/imailmergedatasourceroot/
---
```
public interface IMailMergeDataSourceRoot
```

Implementieren Sie dieses Interface, um einen Seriendruck aus einer benutzerdefinierten Datenquelle mit Master-Detail-Daten zu ermöglichen.

 **Examples:** 

Führt den Seriendruck aus einer benutzerdefinierten Datenquelle mit Master-Detail-Daten aus.

```

 public void customDataSourceRoot() throws Exception {
     // Create a document with two mail merge regions named "Washington" and "Seattle"
     Document doc = createSourceDocumentWithMailMergeRegions(new String[]{"Washington", "Seattle"});

     // Create two data sources
     EmployeeList employeesWashingtonBranch = new EmployeeList();
     employeesWashingtonBranch.add(new Employee("John Doe", "Sales"));
     employeesWashingtonBranch.add(new Employee("Jane Doe", "Management"));

     EmployeeList employeesSeattleBranch = new EmployeeList();
     employeesWashingtonBranch.add(new Employee("John Cardholder", "Management"));
     employeesWashingtonBranch.add(new Employee("Joe Bloggs", "Sales"));

     // Register our data sources by name in a data source root
     DataSourceRoot sourceRoot = new DataSourceRoot();
     sourceRoot.registerSource("Washington", new EmployeeListMailMergeSource(employeesWashingtonBranch));
     sourceRoot.registerSource("Seattle", new EmployeeListMailMergeSource(employeesSeattleBranch));

     // Since we have consecutive mail merge regions, we would normally have to perform two mail merges
     // However, one mail merge source data root call every relevant data source and merge automatically
     doc.getMailMerge().executeWithRegions(sourceRoot);

     doc.save(getArtifactsDir() + "MailMergeCustom.CustomDataSourceRoot.docx");
 }

 /// 
 /// Create document that contains consecutive mail merge regions, with names designated by the input array,
 /// for a data table of employees.
 /// 
 private static Document createSourceDocumentWithMailMergeRegions(String[] regions) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     for (String s : regions) {
         builder.writeln("\n" + s + " branch: ");
         builder.insertField(" MERGEFIELD TableStart:" + s);
         builder.insertField(" MERGEFIELD FullName");
         builder.write(", ");
         builder.insertField(" MERGEFIELD Department");
         builder.insertField(" MERGEFIELD TableEnd:" + s);
     }

     return doc;
 }

 /// 
 /// An example of a "data entity" class in your application.
 /// 
 private static class Employee {
     public Employee(String aFullName, String aDepartment) {
         mFullName = aFullName;
         mDepartment = aDepartment;
     }

     public String getFullName() {
         return mFullName;
     }

     private final String mFullName;

     public String getDepartment() {
         return mDepartment;
     }

     private final String mDepartment;
 }

 /// 
 /// An example of a typed collection that contains your "data" objects.
 /// 
 private static class EmployeeList extends ArrayList {
     public Employee get(int index) {
         return (Employee) super.get(index);
     }

     public void set(int index, Employee value) {
         super.set(index, value);
     }
 }

 /// 
 /// Data source root that can be passed directly into a mail merge which can register and contain many child data sources.
 /// These sources must all implement IMailMergeDataSource, and are registered and differentiated by a name
 /// which corresponds to a mail merge region that will read the respective data.
 /// 
 private static class DataSourceRoot implements IMailMergeDataSourceRoot {
     public IMailMergeDataSource getDataSource(String tableName) {
         EmployeeListMailMergeSource source = mSources.get(tableName);
         source.reset();
         return mSources.get(tableName);
     }

     public void registerSource(String sourceName, EmployeeListMailMergeSource source) {
         mSources.put(sourceName, source);
     }

     private final HashMap mSources = new HashMap<>();
 }

 /// 
 /// Custom mail merge data source.
 /// 
 private static class EmployeeListMailMergeSource implements IMailMergeDataSource {
     public EmployeeListMailMergeSource(EmployeeList employees) {
         mEmployees = employees;
         mRecordIndex = -1;
     }

     /// 
     /// A standard implementation for moving to a next record in a collection.
     /// 
     public boolean moveNext() {
         if (!isEof())
             mRecordIndex++;

         return (!isEof());
     }

     private boolean isEof() {
         return (mRecordIndex >= mEmployees.size());
     }

     public void reset() {
         mRecordIndex = -1;
     }

     /// 
     /// The name of the data source. Used by Aspose.Words only when executing mail merge with repeatable regions.
     /// 
     public String getTableName() {
         return "Employees";
     }

     /// 
     /// Aspose.Words calls this method to get a value for every data field.
     /// 
     public boolean getValue(String fieldName, Ref fieldValue) {
         switch (fieldName) {
             case "FullName":
                 fieldValue.set(mEmployees.get(mRecordIndex).getFullName());
                 return true;
             case "Department":
                 fieldValue.set(mEmployees.get(mRecordIndex).getDepartment());
                 return true;
             default:
                 // A field with this name was not found,
                 // return false to the Aspose.Words mail merge engine
                 fieldValue.set(null);
                 return false;
         }
     }

     /// 
     /// Child data sources are for nested mail merges.
     /// 
     public IMailMergeDataSource getChildDataSource(String tableName) {
         throw new UnsupportedOperationException();
     }

     private final EmployeeList mEmployees;
     private int mRecordIndex;
 }
 
```
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getDataSource(String tableName)](#getDataSource-java.lang.String) | Die Aspose.Words-Seriendruck-Engine ruft diese Methode auf, wenn sie den Beginn einer Mail-Merge-Region auf oberster Ebene erkennt. |
### getDataSource(String tableName) {#getDataSource-java.lang.String}
```
public abstract IMailMergeDataSource getDataSource(String tableName)
```


Die Aspose.Words-Seriendruck-Engine ruft diese Methode auf, wenn sie den Beginn einer Mail-Merge-Region auf oberster Ebene erkennt.

 **Remarks:** 

Wenn die Aspose.Words-Seriendruck-Engine ein Dokument mit Daten füllt und auf MERGEFIELD TableStart:TableName stößt, ruft sie [getDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasourceroot/\#getDataSource-java.lang.String) für dieses Objekt auf. Ihre Implementierung muss ein neues Datenquellenobjekt zurückgeben. Aspose.Words verwendet die zurückgegebene Datenquelle, um die Seriendruck-Region zu füllen.

Wenn eine Datenquelle (Tabelle) mit dem angegebenen Namen nicht existiert, sollte Ihre Implementierung  null  zurückgeben.

 **Examples:** 

Führt den Seriendruck aus einer benutzerdefinierten Datenquelle mit Master-Detail-Daten aus.

```

 public void customDataSourceRoot() throws Exception {
     // Create a document with two mail merge regions named "Washington" and "Seattle"
     Document doc = createSourceDocumentWithMailMergeRegions(new String[]{"Washington", "Seattle"});

     // Create two data sources
     EmployeeList employeesWashingtonBranch = new EmployeeList();
     employeesWashingtonBranch.add(new Employee("John Doe", "Sales"));
     employeesWashingtonBranch.add(new Employee("Jane Doe", "Management"));

     EmployeeList employeesSeattleBranch = new EmployeeList();
     employeesWashingtonBranch.add(new Employee("John Cardholder", "Management"));
     employeesWashingtonBranch.add(new Employee("Joe Bloggs", "Sales"));

     // Register our data sources by name in a data source root
     DataSourceRoot sourceRoot = new DataSourceRoot();
     sourceRoot.registerSource("Washington", new EmployeeListMailMergeSource(employeesWashingtonBranch));
     sourceRoot.registerSource("Seattle", new EmployeeListMailMergeSource(employeesSeattleBranch));

     // Since we have consecutive mail merge regions, we would normally have to perform two mail merges
     // However, one mail merge source data root call every relevant data source and merge automatically
     doc.getMailMerge().executeWithRegions(sourceRoot);

     doc.save(getArtifactsDir() + "MailMergeCustom.CustomDataSourceRoot.docx");
 }

 /// 
 /// Create document that contains consecutive mail merge regions, with names designated by the input array,
 /// for a data table of employees.
 /// 
 private static Document createSourceDocumentWithMailMergeRegions(String[] regions) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     for (String s : regions) {
         builder.writeln("\n" + s + " branch: ");
         builder.insertField(" MERGEFIELD TableStart:" + s);
         builder.insertField(" MERGEFIELD FullName");
         builder.write(", ");
         builder.insertField(" MERGEFIELD Department");
         builder.insertField(" MERGEFIELD TableEnd:" + s);
     }

     return doc;
 }

 /// 
 /// An example of a "data entity" class in your application.
 /// 
 private static class Employee {
     public Employee(String aFullName, String aDepartment) {
         mFullName = aFullName;
         mDepartment = aDepartment;
     }

     public String getFullName() {
         return mFullName;
     }

     private final String mFullName;

     public String getDepartment() {
         return mDepartment;
     }

     private final String mDepartment;
 }

 /// 
 /// An example of a typed collection that contains your "data" objects.
 /// 
 private static class EmployeeList extends ArrayList {
     public Employee get(int index) {
         return (Employee) super.get(index);
     }

     public void set(int index, Employee value) {
         super.set(index, value);
     }
 }

 /// 
 /// Data source root that can be passed directly into a mail merge which can register and contain many child data sources.
 /// These sources must all implement IMailMergeDataSource, and are registered and differentiated by a name
 /// which corresponds to a mail merge region that will read the respective data.
 /// 
 private static class DataSourceRoot implements IMailMergeDataSourceRoot {
     public IMailMergeDataSource getDataSource(String tableName) {
         EmployeeListMailMergeSource source = mSources.get(tableName);
         source.reset();
         return mSources.get(tableName);
     }

     public void registerSource(String sourceName, EmployeeListMailMergeSource source) {
         mSources.put(sourceName, source);
     }

     private final HashMap mSources = new HashMap<>();
 }

 /// 
 /// Custom mail merge data source.
 /// 
 private static class EmployeeListMailMergeSource implements IMailMergeDataSource {
     public EmployeeListMailMergeSource(EmployeeList employees) {
         mEmployees = employees;
         mRecordIndex = -1;
     }

     /// 
     /// A standard implementation for moving to a next record in a collection.
     /// 
     public boolean moveNext() {
         if (!isEof())
             mRecordIndex++;

         return (!isEof());
     }

     private boolean isEof() {
         return (mRecordIndex >= mEmployees.size());
     }

     public void reset() {
         mRecordIndex = -1;
     }

     /// 
     /// The name of the data source. Used by Aspose.Words only when executing mail merge with repeatable regions.
     /// 
     public String getTableName() {
         return "Employees";
     }

     /// 
     /// Aspose.Words calls this method to get a value for every data field.
     /// 
     public boolean getValue(String fieldName, Ref fieldValue) {
         switch (fieldName) {
             case "FullName":
                 fieldValue.set(mEmployees.get(mRecordIndex).getFullName());
                 return true;
             case "Department":
                 fieldValue.set(mEmployees.get(mRecordIndex).getDepartment());
                 return true;
             default:
                 // A field with this name was not found,
                 // return false to the Aspose.Words mail merge engine
                 fieldValue.set(null);
                 return false;
         }
     }

     /// 
     /// Child data sources are for nested mail merges.
     /// 
     public IMailMergeDataSource getChildDataSource(String tableName) {
         throw new UnsupportedOperationException();
     }

     private final EmployeeList mEmployees;
     private int mRecordIndex;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| tableName | java.lang.String | Der Name des Seriendruckbereichs, wie im Vorlagendokument angegeben. Groß‑ und Kleinschreibung wird ignoriert. |

**Returns:**
[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) - A data source object that will provide access to the data records of the specified table.
