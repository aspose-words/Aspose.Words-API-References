---
title: "IMailMergeDataSourceRoot"
linktitle: "IMailMergeDataSourceRoot"
second_title: "Aspose.Words pour Java"
description: "Implémentez cette interface pour permettre la fusion de courrier à partir d'une source de données personnalisée avec des données maître-détail en Java."
type: docs
weight: 777
url: /fr/java/com.aspose.words/imailmergedatasourceroot/
---
```
public interface IMailMergeDataSourceRoot
```

Implémentez cette interface pour permettre la fusion de courrier à partir d'une source de données personnalisée contenant des données maître-détail.

 **Examples:** 

Effectue la fusion de courrier à partir d'une source de données personnalisée avec des données maître-détail.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [getDataSource(String tableName)](#getDataSource-java.lang.String) | Le moteur de fusion de courrier Aspose.Words invoque cette méthode lorsqu'il rencontre le début d'une région de fusion de courrier de niveau supérieur. |
### getDataSource(String tableName) {#getDataSource-java.lang.String}
```
public abstract IMailMergeDataSource getDataSource(String tableName)
```


Le moteur de fusion de courrier Aspose.Words invoque cette méthode lorsqu'il rencontre le début d'une région de fusion de courrier de niveau supérieur.

 **Remarks:** 

Lorsque les moteurs de fusion de courrier Aspose.Words remplissent un document avec des données et rencontrent MERGEFIELD TableStart:TableName, ils invoquent [getDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasourceroot/\#getDataSource-java.lang.String) sur cet objet. Votre implémentation doit renvoyer un nouvel objet source de données. Aspose.Words utilisera la source de données renvoyée pour remplir la région de fusion de courrier.

Si une source de données (table) portant le nom spécifié n'existe pas, votre implémentation doit renvoyer  null .

 **Examples:** 

Effectue la fusion de courrier à partir d'une source de données personnalisée avec des données maître-détail.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| tableName | java.lang.String | Le nom de la région de fusion de courrier tel que spécifié dans le document modèle. Insensible à la casse. |

**Returns:**
[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource/) - A data source object that will provide access to the data records of the specified table.
