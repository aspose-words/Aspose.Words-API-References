---
title: "WebExtensionStoreType"
linktitle: "WebExtensionStoreType"
second_title: "Aspose.Words für Java"
description: "Enumeriert die verfügbaren Typen eines Web-Extension-Stores in Java."
type: docs
weight: 734
url: /de/java/com.aspose.words/webextensionstoretype/
---

**Inheritance:**
java.lang.Object
```
public class WebExtensionStoreType
```

Enumeriert verfügbare Typen eines Web-Erweiterungsstores.

 **Examples:** 

Zeigt, wie man eine Web-Extension zu einem Dokument hinzufügt.

```

 Document doc = new Document();

 // Create task pane with "MyScript" add-in, which will be used by the document,
 // then set its default location.
 TaskPane myScriptTaskPane = new TaskPane();
 doc.getWebExtensionTaskPanes().add(myScriptTaskPane);
 myScriptTaskPane.setDockState(TaskPaneDockState.RIGHT);
 myScriptTaskPane.isVisible(true);
 myScriptTaskPane.setWidth(300.0);
 myScriptTaskPane.isLocked(true);

 // If there are multiple task panes in the same docking location, we can set this index to arrange them.
 myScriptTaskPane.setRow(1);

 // Create an add-in called "MyScript Math Sample", which the task pane will display within.
 WebExtension webExtension = myScriptTaskPane.getWebExtension();

 // Set application store reference parameters for our add-in, such as the ID.
 webExtension.getReference().setId("WA104380646");
 webExtension.getReference().setVersion("1.0.0.0");
 webExtension.getReference().setStoreType(WebExtensionStoreType.OMEX);
 webExtension.getReference().setStore("English (United States)");
 webExtension.getProperties().add(new WebExtensionProperty("MyScript", "MyScript Math Sample"));
 webExtension.getBindings().add(new WebExtensionBinding("MyScript", WebExtensionBindingType.TEXT, "104380646"));

 // Allow the user to interact with the add-in.
 webExtension.isFrozen(false);

 // We can access the web extension in Microsoft Word via Developer -> Add-ins.
 doc.save(getArtifactsDir() + "Document.WebExtension.docx");

 // Remove all web extension task panes at once like this.
 doc.getWebExtensionTaskPanes().clear();

 Assert.assertEquals(0, doc.getWebExtensionTaskPanes().getCount());

 doc = new Document(getArtifactsDir() + "Document.WebExtension.docx");

 myScriptTaskPane = doc.getWebExtensionTaskPanes().get(0);
 Assert.assertEquals(TaskPaneDockState.RIGHT, myScriptTaskPane.getDockState());
 Assert.assertTrue(myScriptTaskPane.isVisible());
 Assert.assertEquals(300.0d, myScriptTaskPane.getWidth());
 Assert.assertTrue(myScriptTaskPane.isLocked());
 Assert.assertEquals(1, myScriptTaskPane.getRow());

 webExtension = myScriptTaskPane.getWebExtension();
 Assert.assertEquals("", webExtension.getId());

 Assert.assertEquals("WA104380646", webExtension.getReference().getId());
 Assert.assertEquals("1.0.0.0", webExtension.getReference().getVersion());
 Assert.assertEquals(WebExtensionStoreType.OMEX, webExtension.getReference().getStoreType());
 Assert.assertEquals("English (United States)", webExtension.getReference().getStore());
 Assert.assertEquals(0, webExtension.getAlternateReferences().getCount());

 Assert.assertEquals("MyScript", webExtension.getProperties().get(0).getName());
 Assert.assertEquals("MyScript Math Sample", webExtension.getProperties().get(0).getValue());

 Assert.assertEquals("MyScript", webExtension.getBindings().get(0).getId());
 Assert.assertEquals(WebExtensionBindingType.TEXT, webExtension.getBindings().get(0).getBindingType());
 Assert.assertEquals("104380646", webExtension.getBindings().get(0).getAppRef());

 Assert.assertFalse(webExtension.isFrozen());
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [DEFAULT](#DEFAULT) | Standardwert. |
| [EXCHANGE](#EXCHANGE) | Gibt an, dass der Store-Typ ein Exchange-Server ist. |
| [EX_CATALOG](#EX-CATALOG) | Gibt an, dass der Store-Typ eine zentralisierte Bereitstellung über Exchange ist. |
| [FILE_SYSTEM](#FILE-SYSTEM) | Gibt an, dass der Speichertyp ein Dateisystemfreigabe ist. |
| [OMEX](#OMEX) | Gibt an, dass der Speichertyp Office.com ist. |
| [REGISTRY](#REGISTRY) | Gibt an, dass der Speichertyp die Systemregistrierung ist. |
| [SP_APP](#SP-APP) |  |
| [SP_CATALOG](#SP-CATALOG) |  |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String webExtensionStoreTypeName)](#fromName-java.lang.String) |  |
| [getName(int webExtensionStoreType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int webExtensionStoreType)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Standardwert.

### EXCHANGE {#EXCHANGE}
```
public static int EXCHANGE
```


Gibt an, dass der Store-Typ ein Exchange-Server ist.

### EX_CATALOG {#EX-CATALOG}
```
public static int EX_CATALOG
```


Gibt an, dass der Store-Typ eine zentralisierte Bereitstellung über Exchange ist.

### FILE_SYSTEM {#FILE-SYSTEM}
```
public static int FILE_SYSTEM
```


Gibt an, dass der Speichertyp ein Dateisystemfreigabe ist.

### OMEX {#OMEX}
```
public static int OMEX
```


Gibt an, dass der Speichertyp Office.com ist.

### REGISTRY {#REGISTRY}
```
public static int REGISTRY
```


Gibt an, dass der Speichertyp die Systemregistrierung ist.

### SP_APP {#SP-APP}
```
public static int SP_APP
```


### SP_CATALOG {#SP-CATALOG}
```
public static int SP_CATALOG
```


### length {#length}
```
public static int length
```


### fromName(String webExtensionStoreTypeName) {#fromName-java.lang.String}
```
public static int fromName(String webExtensionStoreTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| webExtensionStoreTypeName | java.lang.String |  |

**Returns:**
int
### getName(int webExtensionStoreType) {#getName-int}
```
public static String getName(int webExtensionStoreType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| webExtensionStoreType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int webExtensionStoreType) {#toString-int}
```
public static String toString(int webExtensionStoreType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| webExtensionStoreType | int |  |

**Returns:**
java.lang.String
