---
title: "MailMergeRegionInfo"
linktitle: "MailMergeRegionInfo"
second_title: "Aspose.Words per Java"
description: "Contiene informazioni su una regione di unione di stampa in Java."
type: docs
weight: 444
url: /it/java/com.aspose.words/mailmergeregioninfo/
---

**Inheritance:**
java.lang.Object
```
public class MailMergeRegionInfo
```

Contiene informazioni su una regione di mail merge.

Per saperne di più, visita l'articolo di documentazione [ Mail Merge and Reporting ][Mail Merge and Reporting].

 **Examples:** 

Mostra come ottenere MailMergeRegionInfo e lavorarci.

```

 Document doc = new Document(getMyDir() + "Mail merge regions.docx");

 // Returns a full hierarchy of regions (with fields) available in the document
 MailMergeRegionInfo regionInfo = doc.getMailMerge().getRegionsHierarchy();

 // Get top regions in the document
 ArrayList topRegions = regionInfo.getRegions();
 Assert.assertEquals(topRegions.size(), 2);
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(0)).getName(), "Region1");
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(1)).getName(), "Region2");
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(0)).getLevel(), 1);
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(1)).getLevel(), 1);

 // Get nested region in first top region
 ArrayList nestedRegions = ((MailMergeRegionInfo) topRegions.get(0)).getRegions();
 Assert.assertEquals(nestedRegions.size(), 2);
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(0)).getName(), "NestedRegion1");
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(1)).getName(), "NestedRegion2");
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(0)).getLevel(), 2);
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(1)).getLevel(), 2);

 // Get field list in first top region
 ArrayList fieldList = ((MailMergeRegionInfo) topRegions.get(0)).getFields();
 Assert.assertEquals(fieldList.size(), 4);

 FieldMergeField startFieldMergeField = ((MailMergeRegionInfo) nestedRegions.get(0)).getStartField();
 Assert.assertEquals(startFieldMergeField.getFieldName(), "TableStart:NestedRegion1");

 FieldMergeField endFieldMergeField = ((MailMergeRegionInfo) nestedRegions.get(0)).getEndField();
 Assert.assertEquals(endFieldMergeField.getFieldName(), "TableEnd:NestedRegion1");
 
```


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getEndField()](#getEndField) | Restituisce un campo di chiusura per la regione. |
| [getEndMustacheTag()](#getEndMustacheTag) | Restituisce un tag "mustache" di chiusura per la regione. |
| [getFields()](#getFields) | Restituisce un elenco di campi figlio. |
| [getLevel()](#getLevel) | Restituisce il livello di nidificazione per la regione. |
| [getMustacheTags()](#getMustacheTags) | Restituisce un elenco di tag "mustache" figlio. |
| [getName()](#getName) | Restituisce il nome della regione. |
| [getParentRegion()](#getParentRegion) | Restituisce le informazioni della regione genitore (null per la regione di livello superiore). |
| [getRegions()](#getRegions) | Restituisce un elenco di regioni figlio. |
| [getStartField()](#getStartField) | Restituisce un campo di apertura per la regione. |
| [getStartMustacheTag()](#getStartMustacheTag) | Restituisce un tag "mustache" di apertura per la regione. |
### getEndField() {#getEndField}
```
public FieldMergeField getEndField()
```


Restituisce un campo di chiusura per la regione.

 **Examples:** 

Mostra come ottenere MailMergeRegionInfo e lavorarci.

```

 Document doc = new Document(getMyDir() + "Mail merge regions.docx");

 // Returns a full hierarchy of regions (with fields) available in the document
 MailMergeRegionInfo regionInfo = doc.getMailMerge().getRegionsHierarchy();

 // Get top regions in the document
 ArrayList topRegions = regionInfo.getRegions();
 Assert.assertEquals(topRegions.size(), 2);
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(0)).getName(), "Region1");
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(1)).getName(), "Region2");
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(0)).getLevel(), 1);
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(1)).getLevel(), 1);

 // Get nested region in first top region
 ArrayList nestedRegions = ((MailMergeRegionInfo) topRegions.get(0)).getRegions();
 Assert.assertEquals(nestedRegions.size(), 2);
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(0)).getName(), "NestedRegion1");
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(1)).getName(), "NestedRegion2");
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(0)).getLevel(), 2);
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(1)).getLevel(), 2);

 // Get field list in first top region
 ArrayList fieldList = ((MailMergeRegionInfo) topRegions.get(0)).getFields();
 Assert.assertEquals(fieldList.size(), 4);

 FieldMergeField startFieldMergeField = ((MailMergeRegionInfo) nestedRegions.get(0)).getStartField();
 Assert.assertEquals(startFieldMergeField.getFieldName(), "TableStart:NestedRegion1");

 FieldMergeField endFieldMergeField = ((MailMergeRegionInfo) nestedRegions.get(0)).getEndField();
 Assert.assertEquals(endFieldMergeField.getFieldName(), "TableEnd:NestedRegion1");
 
```

**Returns:**
[FieldMergeField](../../com.aspose.words/fieldmergefield/) - An end field for the region.
### getEndMustacheTag() {#getEndMustacheTag}
```
public MustacheTag getEndMustacheTag()
```


Restituisce un tag "mustache" di chiusura per la regione.

**Returns:**
[MustacheTag](../../com.aspose.words/mustachetag/) - An end "mustache" tag for the region.
### getFields() {#getFields}
```
public ArrayList getFields()
```


Restituisce un elenco di campi figlio.

 **Examples:** 

Mostra come ottenere MailMergeRegionInfo e lavorarci.

```

 Document doc = new Document(getMyDir() + "Mail merge regions.docx");

 // Returns a full hierarchy of regions (with fields) available in the document
 MailMergeRegionInfo regionInfo = doc.getMailMerge().getRegionsHierarchy();

 // Get top regions in the document
 ArrayList topRegions = regionInfo.getRegions();
 Assert.assertEquals(topRegions.size(), 2);
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(0)).getName(), "Region1");
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(1)).getName(), "Region2");
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(0)).getLevel(), 1);
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(1)).getLevel(), 1);

 // Get nested region in first top region
 ArrayList nestedRegions = ((MailMergeRegionInfo) topRegions.get(0)).getRegions();
 Assert.assertEquals(nestedRegions.size(), 2);
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(0)).getName(), "NestedRegion1");
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(1)).getName(), "NestedRegion2");
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(0)).getLevel(), 2);
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(1)).getLevel(), 2);

 // Get field list in first top region
 ArrayList fieldList = ((MailMergeRegionInfo) topRegions.get(0)).getFields();
 Assert.assertEquals(fieldList.size(), 4);

 FieldMergeField startFieldMergeField = ((MailMergeRegionInfo) nestedRegions.get(0)).getStartField();
 Assert.assertEquals(startFieldMergeField.getFieldName(), "TableStart:NestedRegion1");

 FieldMergeField endFieldMergeField = ((MailMergeRegionInfo) nestedRegions.get(0)).getEndField();
 Assert.assertEquals(endFieldMergeField.getFieldName(), "TableEnd:NestedRegion1");
 
```

**Returns:**
java.util.ArrayList - Un elenco di campi figlio.
### getLevel() {#getLevel}
```
public int getLevel()
```


Restituisce il livello di nidificazione per la regione.

 **Examples:** 

Mostra come ottenere MailMergeRegionInfo e lavorarci.

```

 Document doc = new Document(getMyDir() + "Mail merge regions.docx");

 // Returns a full hierarchy of regions (with fields) available in the document
 MailMergeRegionInfo regionInfo = doc.getMailMerge().getRegionsHierarchy();

 // Get top regions in the document
 ArrayList topRegions = regionInfo.getRegions();
 Assert.assertEquals(topRegions.size(), 2);
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(0)).getName(), "Region1");
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(1)).getName(), "Region2");
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(0)).getLevel(), 1);
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(1)).getLevel(), 1);

 // Get nested region in first top region
 ArrayList nestedRegions = ((MailMergeRegionInfo) topRegions.get(0)).getRegions();
 Assert.assertEquals(nestedRegions.size(), 2);
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(0)).getName(), "NestedRegion1");
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(1)).getName(), "NestedRegion2");
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(0)).getLevel(), 2);
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(1)).getLevel(), 2);

 // Get field list in first top region
 ArrayList fieldList = ((MailMergeRegionInfo) topRegions.get(0)).getFields();
 Assert.assertEquals(fieldList.size(), 4);

 FieldMergeField startFieldMergeField = ((MailMergeRegionInfo) nestedRegions.get(0)).getStartField();
 Assert.assertEquals(startFieldMergeField.getFieldName(), "TableStart:NestedRegion1");

 FieldMergeField endFieldMergeField = ((MailMergeRegionInfo) nestedRegions.get(0)).getEndField();
 Assert.assertEquals(endFieldMergeField.getFieldName(), "TableEnd:NestedRegion1");
 
```

**Returns:**
int - Il livello di nidificazione per la regione.
### getMustacheTags() {#getMustacheTags}
```
public ArrayList getMustacheTags()
```


Restituisce un elenco di tag "mustache" figlio.

**Returns:**
java.util.ArrayList - Un elenco di tag "mustache" figlio.
### getName() {#getName}
```
public String getName()
```


Restituisce il nome della regione.

 **Examples:** 

Mostra come ottenere MailMergeRegionInfo e lavorarci.

```

 Document doc = new Document(getMyDir() + "Mail merge regions.docx");

 // Returns a full hierarchy of regions (with fields) available in the document
 MailMergeRegionInfo regionInfo = doc.getMailMerge().getRegionsHierarchy();

 // Get top regions in the document
 ArrayList topRegions = regionInfo.getRegions();
 Assert.assertEquals(topRegions.size(), 2);
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(0)).getName(), "Region1");
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(1)).getName(), "Region2");
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(0)).getLevel(), 1);
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(1)).getLevel(), 1);

 // Get nested region in first top region
 ArrayList nestedRegions = ((MailMergeRegionInfo) topRegions.get(0)).getRegions();
 Assert.assertEquals(nestedRegions.size(), 2);
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(0)).getName(), "NestedRegion1");
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(1)).getName(), "NestedRegion2");
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(0)).getLevel(), 2);
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(1)).getLevel(), 2);

 // Get field list in first top region
 ArrayList fieldList = ((MailMergeRegionInfo) topRegions.get(0)).getFields();
 Assert.assertEquals(fieldList.size(), 4);

 FieldMergeField startFieldMergeField = ((MailMergeRegionInfo) nestedRegions.get(0)).getStartField();
 Assert.assertEquals(startFieldMergeField.getFieldName(), "TableStart:NestedRegion1");

 FieldMergeField endFieldMergeField = ((MailMergeRegionInfo) nestedRegions.get(0)).getEndField();
 Assert.assertEquals(endFieldMergeField.getFieldName(), "TableEnd:NestedRegion1");
 
```

**Returns:**
java.lang.String - Il nome della regione.
### getParentRegion() {#getParentRegion}
```
public MailMergeRegionInfo getParentRegion()
```


Restituisce le informazioni della regione genitore (null per la regione di livello superiore).

 **Examples:** 

Mostra come creare, elencare e leggere le regioni di unione di stampa.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // These tags, which go inside MERGEFIELDs, denote the strings that signify the starts and ends of mail merge regions
 Assert.assertEquals(doc.getMailMerge().getRegionStartTag(), "TableStart");
 Assert.assertEquals(doc.getMailMerge().getRegionEndTag(), "TableEnd");

 // By using these tags, we will start and end a "MailMergeRegion1", which will contain MERGEFIELDs for two columns
 builder.insertField(" MERGEFIELD TableStart:MailMergeRegion1");
 builder.insertField(" MERGEFIELD Column1");
 builder.write(", ");
 builder.insertField(" MERGEFIELD Column2");
 builder.insertField(" MERGEFIELD TableEnd:MailMergeRegion1");

 // We can keep track of merge regions and their columns by looking at these collections
 ArrayList regions = doc.getMailMerge().getRegionsByName("MailMergeRegion1");
 Assert.assertEquals(regions.size(), 1);
 Assert.assertEquals(regions.get(0).getName(), "MailMergeRegion1");

 String[] mergeFieldNames = doc.getMailMerge().getFieldNamesForRegion("MailMergeRegion1");
 Assert.assertEquals(mergeFieldNames[0], "Column1");
 Assert.assertEquals(mergeFieldNames[1], "Column2");

 // Insert a region with the same name inside the existing region, which will make it a parent.
 // Now a "Column2" field will be inside a new region.
 builder.moveToField(regions.get(0).getFields().get(1), false);
 builder.insertField(" MERGEFIELD TableStart:MailMergeRegion1");
 builder.moveToField(regions.get(0).getFields().get(1), true);
 builder.insertField(" MERGEFIELD TableEnd:MailMergeRegion1");

 // Regions that share the same name are still accounted for and can be accessed by index
 regions = doc.getMailMerge().getRegionsByName("MailMergeRegion1");
 Assert.assertEquals(regions.size(), 2);
 // Check that the second region now has a parent region.
 Assert.assertEquals("MailMergeRegion1", regions.get(1).getParentRegion().getName());

 mergeFieldNames = doc.getMailMerge().getFieldNamesForRegion("MailMergeRegion1", 1);
 Assert.assertEquals(mergeFieldNames[0], "Column2");
 
```

**Returns:**
[MailMergeRegionInfo](../../com.aspose.words/mailmergeregioninfo/) - Parent region info (null for top-level region).
### getRegions() {#getRegions}
```
public ArrayList getRegions()
```


Restituisce un elenco di regioni figlio.

 **Examples:** 

Mostra come ottenere MailMergeRegionInfo e lavorarci.

```

 Document doc = new Document(getMyDir() + "Mail merge regions.docx");

 // Returns a full hierarchy of regions (with fields) available in the document
 MailMergeRegionInfo regionInfo = doc.getMailMerge().getRegionsHierarchy();

 // Get top regions in the document
 ArrayList topRegions = regionInfo.getRegions();
 Assert.assertEquals(topRegions.size(), 2);
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(0)).getName(), "Region1");
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(1)).getName(), "Region2");
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(0)).getLevel(), 1);
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(1)).getLevel(), 1);

 // Get nested region in first top region
 ArrayList nestedRegions = ((MailMergeRegionInfo) topRegions.get(0)).getRegions();
 Assert.assertEquals(nestedRegions.size(), 2);
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(0)).getName(), "NestedRegion1");
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(1)).getName(), "NestedRegion2");
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(0)).getLevel(), 2);
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(1)).getLevel(), 2);

 // Get field list in first top region
 ArrayList fieldList = ((MailMergeRegionInfo) topRegions.get(0)).getFields();
 Assert.assertEquals(fieldList.size(), 4);

 FieldMergeField startFieldMergeField = ((MailMergeRegionInfo) nestedRegions.get(0)).getStartField();
 Assert.assertEquals(startFieldMergeField.getFieldName(), "TableStart:NestedRegion1");

 FieldMergeField endFieldMergeField = ((MailMergeRegionInfo) nestedRegions.get(0)).getEndField();
 Assert.assertEquals(endFieldMergeField.getFieldName(), "TableEnd:NestedRegion1");
 
```

**Returns:**
java.util.ArrayList - Un elenco di regioni figlio.
### getStartField() {#getStartField}
```
public FieldMergeField getStartField()
```


Restituisce un campo di apertura per la regione.

 **Examples:** 

Mostra come ottenere MailMergeRegionInfo e lavorarci.

```

 Document doc = new Document(getMyDir() + "Mail merge regions.docx");

 // Returns a full hierarchy of regions (with fields) available in the document
 MailMergeRegionInfo regionInfo = doc.getMailMerge().getRegionsHierarchy();

 // Get top regions in the document
 ArrayList topRegions = regionInfo.getRegions();
 Assert.assertEquals(topRegions.size(), 2);
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(0)).getName(), "Region1");
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(1)).getName(), "Region2");
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(0)).getLevel(), 1);
 Assert.assertEquals(((MailMergeRegionInfo) topRegions.get(1)).getLevel(), 1);

 // Get nested region in first top region
 ArrayList nestedRegions = ((MailMergeRegionInfo) topRegions.get(0)).getRegions();
 Assert.assertEquals(nestedRegions.size(), 2);
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(0)).getName(), "NestedRegion1");
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(1)).getName(), "NestedRegion2");
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(0)).getLevel(), 2);
 Assert.assertEquals(((MailMergeRegionInfo) nestedRegions.get(1)).getLevel(), 2);

 // Get field list in first top region
 ArrayList fieldList = ((MailMergeRegionInfo) topRegions.get(0)).getFields();
 Assert.assertEquals(fieldList.size(), 4);

 FieldMergeField startFieldMergeField = ((MailMergeRegionInfo) nestedRegions.get(0)).getStartField();
 Assert.assertEquals(startFieldMergeField.getFieldName(), "TableStart:NestedRegion1");

 FieldMergeField endFieldMergeField = ((MailMergeRegionInfo) nestedRegions.get(0)).getEndField();
 Assert.assertEquals(endFieldMergeField.getFieldName(), "TableEnd:NestedRegion1");
 
```

**Returns:**
[FieldMergeField](../../com.aspose.words/fieldmergefield/) - A start field for the region.
### getStartMustacheTag() {#getStartMustacheTag}
```
public MustacheTag getStartMustacheTag()
```


Restituisce un tag "mustache" di apertura per la regione.

**Returns:**
[MustacheTag](../../com.aspose.words/mustachetag/) - A start "mustache" tag for the region.
