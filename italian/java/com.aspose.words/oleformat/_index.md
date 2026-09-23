---
title: "OleFormat"
linktitle: "OleFormat"
second_title: "Aspose.Words per Java"
description: "Fornisce l'accesso ai dati di un oggetto OLE o di un controllo ActiveX in Java."
type: docs
weight: 501
url: /it/java/com.aspose.words/oleformat/
---

**Inheritance:**
java.lang.Object
```
public class OleFormat
```

Fornisce l'accesso ai dati di un oggetto OLE o di un controllo ActiveX.

Per saperne di più, visita l'articolo della documentazione [ Working with Ole Objects ][Working with Ole Objects].

 **Remarks:** 

Utilizza la proprietà [Shape.getOleFormat()](../../com.aspose.words/shape/\#getOleFormat) per accedere ai dati di un oggetto OLE. Non è necessario creare istanze della classe [OleFormat](../../com.aspose.words/oleformat/) direttamente.

 **Examples:** 

Mostra come estrarre oggetti OLE incorporati in file.

```

 Document doc = new Document(getMyDir() + "OLE spreadsheet.docm");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 // The OLE object in the first shape is a Microsoft Excel spreadsheet.
 OleFormat oleFormat = shape.getOleFormat();

 Assert.assertEquals("Excel.Sheet.12", oleFormat.getProgId());

 // Our object is neither auto updating nor locked from updates.
 Assert.assertFalse(oleFormat.getAutoUpdate());
 Assert.assertEquals(oleFormat.isLocked(), false);

 // If we plan on saving the OLE object to a file in the local file system,
 // we can use the "SuggestedExtension" property to determine which file extension to apply to the file.
 Assert.assertEquals(".xlsx", oleFormat.getSuggestedExtension());

 // Below are two ways of saving an OLE object to a file in the local file system.
 // 1 -  Save it via a stream:
 OutputStream fs = new FileOutputStream(getArtifactsDir() + "OLE spreadsheet extracted via stream" + oleFormat.getSuggestedExtension());
 try {
     oleFormat.save(fs);
 } finally {
     if (fs != null) fs.close();
 }

 // 2 -  Save it directly to a filename:
 oleFormat.save(getArtifactsDir() + "OLE spreadsheet saved directly" + oleFormat.getSuggestedExtension());
 
```


[Working with Ole Objects]: https://docs.aspose.com/words/java/working-with-ole-objects/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getAutoUpdate()](#getAutoUpdate) | Specifica se il collegamento all'oggetto OLE viene aggiornato automaticamente o meno in Microsoft Word. |
| [getClsid()](#getClsid) | Ottiene il CLSID dell'oggetto OLE. |
| [getIconCaption()](#getIconCaption) | Ottiene la didascalia dell'icona dell'oggetto OLE. |
| [getOleControl()](#getOleControl) | Ottiene gli oggetti [getOleControl()](../../com.aspose.words/oleformat/\#getOleControl) se questo oggetto OLE è un controllo ActiveX. |
| [getOleEntry(String oleEntryName)](#getOleEntry-java.lang.String) |  |
| [getOleIcon()](#getOleIcon) | Ottiene l'aspetto di disegno dell'oggetto OLE. |
| [getOlePackage()](#getOlePackage) | Fornisce l'accesso a [OlePackage](../../com.aspose.words/olepackage/) se l'oggetto OLE è un pacchetto OLE. |
| [getProgId()](#getProgId) | Ottiene il ProgID dell'oggetto OLE. |
| [getRawData()](#getRawData) | Ottiene i dati grezzi dell'oggetto OLE. |
| [getSourceFullName()](#getSourceFullName) | Ottiene il percorso e il nome del file sorgente per l'oggetto OLE collegato. |
| [getSourceItem()](#getSourceItem) | Ottiene una stringa usata per identificare la parte del file sorgente che viene collegata. |
| [getSuggestedExtension()](#getSuggestedExtension) | Ottiene l'estensione del file suggerita per l'oggetto incorporato corrente se si desidera salvarlo in un file. |
| [getSuggestedFileName()](#getSuggestedFileName) | Ottiene il nome del file suggerito per l'oggetto incorporato corrente se si desidera salvarlo in un file. |
| [isLink()](#isLink) | Restituisce  true  se l'oggetto OLE è collegato (quando [getSourceFullName()](../../com.aspose.words/oleformat/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceFullName-java.lang.String) è specificato). |
| [isLocked()](#isLocked) | Specifica se il collegamento all'oggetto OLE è bloccato dagli aggiornamenti. |
| [isLocked(boolean value)](#isLocked-boolean) | Specifica se il collegamento all'oggetto OLE è bloccato dagli aggiornamenti. |
| [save(OutputStream stream)](#save-java.io.OutputStream) |  |
| [save(String fileName)](#save-java.lang.String) | Salva i dati dell'oggetto incorporato in un file con il nome specificato. |
| [setAutoUpdate(boolean value)](#setAutoUpdate-boolean) | Specifica se il collegamento all'oggetto OLE viene aggiornato automaticamente o meno in Microsoft Word. |
| [setProgId(String value)](#setProgId-java.lang.String) | Imposta il ProgID dell'oggetto OLE. |
| [setSourceFullName(String value)](#setSourceFullName-java.lang.String) | Imposta il percorso e il nome del file sorgente per l'oggetto OLE collegato. |
| [setSourceItem(String value)](#setSourceItem-java.lang.String) | Imposta una stringa usata per identificare la parte del file sorgente che viene collegata. |
### getAutoUpdate() {#getAutoUpdate}
```
public boolean getAutoUpdate()
```


Specifica se il collegamento all'oggetto OLE viene aggiornato automaticamente o meno in Microsoft Word.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come estrarre oggetti OLE incorporati in file.

```

 Document doc = new Document(getMyDir() + "OLE spreadsheet.docm");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 // The OLE object in the first shape is a Microsoft Excel spreadsheet.
 OleFormat oleFormat = shape.getOleFormat();

 Assert.assertEquals("Excel.Sheet.12", oleFormat.getProgId());

 // Our object is neither auto updating nor locked from updates.
 Assert.assertFalse(oleFormat.getAutoUpdate());
 Assert.assertEquals(oleFormat.isLocked(), false);

 // If we plan on saving the OLE object to a file in the local file system,
 // we can use the "SuggestedExtension" property to determine which file extension to apply to the file.
 Assert.assertEquals(".xlsx", oleFormat.getSuggestedExtension());

 // Below are two ways of saving an OLE object to a file in the local file system.
 // 1 -  Save it via a stream:
 OutputStream fs = new FileOutputStream(getArtifactsDir() + "OLE spreadsheet extracted via stream" + oleFormat.getSuggestedExtension());
 try {
     oleFormat.save(fs);
 } finally {
     if (fs != null) fs.close();
 }

 // 2 -  Save it directly to a filename:
 oleFormat.save(getArtifactsDir() + "OLE spreadsheet saved directly" + oleFormat.getSuggestedExtension());
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getClsid() {#getClsid}
```
public UUID getClsid()
```


Ottiene il CLSID dell'oggetto OLE.

 **Examples:** 

Mostra come accedere a un controllo OLE incorporato in un documento e ai suoi controlli figli.

```

 Document doc = new Document(getMyDir() + "OLE ActiveX controls.docm");

 // Shapes store and display OLE objects in the document's body.
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 Assert.assertEquals("6e182020-f460-11ce-9bcd-00aa00608e01", shape.getOleFormat().getClsid().toString());

 Forms2OleControl oleControl = (Forms2OleControl) shape.getOleFormat().getOleControl();

 // Some OLE controls may contain child controls, such as the one in this document with three options buttons.
 Forms2OleControlCollection oleControlCollection = oleControl.getChildNodes();

 Assert.assertEquals(3, oleControlCollection.getCount());

 Assert.assertEquals("C#", oleControlCollection.get(0).getCaption());
 Assert.assertEquals("1", oleControlCollection.get(0).getValue());

 Assert.assertEquals("Visual Basic", oleControlCollection.get(1).getCaption());
 Assert.assertEquals("0", oleControlCollection.get(1).getValue());

 Assert.assertEquals("Delphi", oleControlCollection.get(2).getCaption());
 Assert.assertEquals("0", oleControlCollection.get(2).getValue());
 
```

**Returns:**
java.util.UUID - Il CLSID dell'oggetto OLE.
### getIconCaption() {#getIconCaption}
```
public String getIconCaption()
```


Ottiene la didascalia dell'icona dell'oggetto OLE.

Nel caso in cui l'oggetto OLE non abbia un'icona o la didascalia non possa essere recuperata, restituisce una stringa vuota.

 **Examples:** 

Mostra come inserire oggetti OLE collegati e non collegati.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Embed a Microsoft Visio drawing into the document as an OLE object.
 builder.insertOleObject(getImageDir() + "Microsoft Visio drawing.vsd", "Package", false, false, new FileInputStream(getImageDir() + "Transparent background logo.png"));

 // Insert a link to the file in the local file system and display it as an icon.
 builder.insertOleObject(getImageDir() + "Microsoft Visio drawing.vsd", "Package", true, true, new FileInputStream(getImageDir() + "Transparent background logo.png"));

 // Inserting OLE objects creates shapes that store these objects.
 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(2, shapeList.size());
 Assert.assertEquals(2, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.OLE_OBJECT));

 // If a shape contains an OLE object, it will have a valid "OleFormat" property,
 // which we can use to verify some aspects of the shape.
 OleFormat oleFormat = shapeList.get(0).getOleFormat();

 Assert.assertEquals(false, oleFormat.isLink());
 Assert.assertEquals(false, oleFormat.getOleIcon());

 oleFormat = shapeList.get(1).getOleFormat();

 Assert.assertEquals(true, oleFormat.isLink());
 Assert.assertEquals(true, oleFormat.getOleIcon());

 Assert.assertTrue(oleFormat.getSourceFullName().endsWith("Images" + File.separator + "Microsoft Visio drawing.vsd"));
 Assert.assertEquals("", oleFormat.getSourceItem());

 Assert.assertEquals("Microsoft Visio drawing.vsd", oleFormat.getIconCaption());

 doc.save(getArtifactsDir() + "Shape.OleLinks.docx");

 // If the object contains OLE data, we can access it using a stream.
 byte[] oleEntryBytes = oleFormat.getOleEntry("CompObj");
 Assert.assertEquals(76, oleEntryBytes.length);
 
```

**Returns:**
java.lang.String - Didascalia dell'icona dell'oggetto OLE.
### getOleControl() {#getOleControl}
```
public OleControl getOleControl()
```


Ottiene gli oggetti [getOleControl()](../../com.aspose.words/oleformat/\#getOleControl) se questo oggetto OLE è un controllo ActiveX. Altrimenti questa proprietà è null.

 **Examples:** 

Mostra come verificare le proprietà di un controllo ActiveX.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 OleControl oleControl = shape.getOleFormat().getOleControl();

 Assert.assertEquals(oleControl.getName(), "CheckBox1");

 if (oleControl.isForms2OleControl()) {
     Forms2OleControl checkBox = (Forms2OleControl) oleControl;
     Assert.assertEquals(checkBox.getCaption(), "First");
     Assert.assertEquals(checkBox.getValue(), "0");
     Assert.assertEquals(checkBox.getEnabled(), true);
     Assert.assertEquals(checkBox.getType(), Forms2OleControlType.CHECK_BOX);
     Assert.assertEquals(checkBox.getChildNodes(), null);
 }
 
```

**Returns:**
[OleControl](../../com.aspose.words/olecontrol/) - [getOleControl()](../../com.aspose.words/oleformat/\#getOleControl) objects if this OLE object is an ActiveX control.
### getOleEntry(String oleEntryName) {#getOleEntry-java.lang.String}
```
public byte[] getOleEntry(String oleEntryName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| oleEntryName | java.lang.String |  |

**Returns:**
byte[]
### getOleIcon() {#getOleIcon}
```
public boolean getOleIcon()
```


Restituisce l'aspetto di disegno dell'oggetto OLE. Quando  true , l'oggetto OLE viene visualizzato come icona. Quando  false , l'oggetto OLE viene visualizzato come contenuto.

 **Remarks:** 

Aspose.Words non consente di impostare questa proprietà per evitare confusione. Se fosse possibile modificare l'aspetto di disegno in Aspose.Words, Microsoft Word continuerebbe a visualizzare l'oggetto OLE nel suo aspetto di disegno originale finché non si modifica o aggiorna l'oggetto OLE in Microsoft Word.

 **Examples:** 

Mostra come inserire oggetti OLE collegati e non collegati.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Embed a Microsoft Visio drawing into the document as an OLE object.
 builder.insertOleObject(getImageDir() + "Microsoft Visio drawing.vsd", "Package", false, false, new FileInputStream(getImageDir() + "Transparent background logo.png"));

 // Insert a link to the file in the local file system and display it as an icon.
 builder.insertOleObject(getImageDir() + "Microsoft Visio drawing.vsd", "Package", true, true, new FileInputStream(getImageDir() + "Transparent background logo.png"));

 // Inserting OLE objects creates shapes that store these objects.
 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(2, shapeList.size());
 Assert.assertEquals(2, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.OLE_OBJECT));

 // If a shape contains an OLE object, it will have a valid "OleFormat" property,
 // which we can use to verify some aspects of the shape.
 OleFormat oleFormat = shapeList.get(0).getOleFormat();

 Assert.assertEquals(false, oleFormat.isLink());
 Assert.assertEquals(false, oleFormat.getOleIcon());

 oleFormat = shapeList.get(1).getOleFormat();

 Assert.assertEquals(true, oleFormat.isLink());
 Assert.assertEquals(true, oleFormat.getOleIcon());

 Assert.assertTrue(oleFormat.getSourceFullName().endsWith("Images" + File.separator + "Microsoft Visio drawing.vsd"));
 Assert.assertEquals("", oleFormat.getSourceItem());

 Assert.assertEquals("Microsoft Visio drawing.vsd", oleFormat.getIconCaption());

 doc.save(getArtifactsDir() + "Shape.OleLinks.docx");

 // If the object contains OLE data, we can access it using a stream.
 byte[] oleEntryBytes = oleFormat.getOleEntry("CompObj");
 Assert.assertEquals(76, oleEntryBytes.length);
 
```

**Returns:**
boolean - L'aspetto di disegno dell'oggetto OLE.
### getOlePackage() {#getOlePackage}
```
public OlePackage getOlePackage()
```


Fornisce l'accesso a [OlePackage](../../com.aspose.words/olepackage/) se l'oggetto OLE è un OLE Package. Restituisce  null  altrimenti.

 **Remarks:** 

OLE Package è una tecnologia legacy che consente di avvolgere qualsiasi formato di file non presente nel registro OLE di un sistema Windows in un pacchetto generico, permettendo di incorporare quasi qualsiasi cosa in un documento. Vedi il tipo [OlePackage](../../com.aspose.words/olepackage/) per ulteriori informazioni.

 **Examples:** 

Mostra come inserire un oggetto OLE in un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // OLE objects allow us to open other files in the local file system using another installed application
 // in our operating system by double-clicking on the shape that contains the OLE object in the document body.
 // In this case, our external file will be a ZIP archive.
 byte[] zipFileBytes = DocumentHelper.getBytesFromStream(new FileInputStream(getDatabaseDir() + "cat001.zip"));

 InputStream stream = new ByteArrayInputStream(zipFileBytes);
 InputStream representingImage = new FileInputStream(getImageDir() + "Logo.jpg");
 try {
     Shape shape = builder.insertOleObject(stream, "Package", true, representingImage);

     OlePackage setOlePackage = shape.getOleFormat().getOlePackage();
     setOlePackage.setFileName("Package file name.zip");
     setOlePackage.setDisplayName("Package display name.zip");

     doc.save(getArtifactsDir() + "Shape.InsertOlePackage.docx");
 } finally {
     if (stream != null) {
         stream.close();
     }
 }
 
```

**Returns:**
[OlePackage](../../com.aspose.words/olepackage/) - The corresponding [OlePackage](../../com.aspose.words/olepackage/) value.
### getProgId() {#getProgId}
```
public String getProgId()
```


Ottiene il ProgID dell'oggetto OLE.

 **Remarks:** 

La proprietà ProgID non è sempre presente nei documenti Microsoft Word e non può essere considerata attendibile.

Non può essere  null .

Il valore predefinito è una stringa vuota.

 **Examples:** 

Mostra come estrarre oggetti OLE incorporati in file.

```

 Document doc = new Document(getMyDir() + "OLE spreadsheet.docm");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 // The OLE object in the first shape is a Microsoft Excel spreadsheet.
 OleFormat oleFormat = shape.getOleFormat();

 Assert.assertEquals("Excel.Sheet.12", oleFormat.getProgId());

 // Our object is neither auto updating nor locked from updates.
 Assert.assertFalse(oleFormat.getAutoUpdate());
 Assert.assertEquals(oleFormat.isLocked(), false);

 // If we plan on saving the OLE object to a file in the local file system,
 // we can use the "SuggestedExtension" property to determine which file extension to apply to the file.
 Assert.assertEquals(".xlsx", oleFormat.getSuggestedExtension());

 // Below are two ways of saving an OLE object to a file in the local file system.
 // 1 -  Save it via a stream:
 OutputStream fs = new FileOutputStream(getArtifactsDir() + "OLE spreadsheet extracted via stream" + oleFormat.getSuggestedExtension());
 try {
     oleFormat.save(fs);
 } finally {
     if (fs != null) fs.close();
 }

 // 2 -  Save it directly to a filename:
 oleFormat.save(getArtifactsDir() + "OLE spreadsheet saved directly" + oleFormat.getSuggestedExtension());
 
```

**Returns:**
java.lang.String - Il ProgID dell'oggetto OLE.
### getRawData() {#getRawData}
```
public byte[] getRawData()
```


Ottiene i dati grezzi dell'oggetto OLE.

 **Examples:** 

Mostra come accedere ai dati grezzi di un oggetto OLE incorporato.

```

 Document doc = new Document(getMyDir() + "OLE objects.docx");

 for (Node shape : (Iterable) doc.getChildNodes(NodeType.SHAPE, true)) {
     OleFormat oleFormat = ((Shape) shape).getOleFormat();
     if (oleFormat != null) {
         byte[] oleRawData = oleFormat.getRawData();

         Assert.assertEquals(24576, oleRawData.length);
     }
 }
 
```

**Returns:**
byte[]
### getSourceFullName() {#getSourceFullName}
```
public String getSourceFullName()
```


Ottiene il percorso e il nome del file sorgente per l'oggetto OLE collegato.

 **Remarks:** 

Il valore predefinito è una stringa vuota.

Se [getSourceFullName()](../../com.aspose.words/oleformat/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceFullName-java.lang.String) non è una stringa vuota, l'oggetto OLE è collegato.

 **Examples:** 

Mostra come inserire oggetti OLE collegati e non collegati.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Embed a Microsoft Visio drawing into the document as an OLE object.
 builder.insertOleObject(getImageDir() + "Microsoft Visio drawing.vsd", "Package", false, false, new FileInputStream(getImageDir() + "Transparent background logo.png"));

 // Insert a link to the file in the local file system and display it as an icon.
 builder.insertOleObject(getImageDir() + "Microsoft Visio drawing.vsd", "Package", true, true, new FileInputStream(getImageDir() + "Transparent background logo.png"));

 // Inserting OLE objects creates shapes that store these objects.
 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(2, shapeList.size());
 Assert.assertEquals(2, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.OLE_OBJECT));

 // If a shape contains an OLE object, it will have a valid "OleFormat" property,
 // which we can use to verify some aspects of the shape.
 OleFormat oleFormat = shapeList.get(0).getOleFormat();

 Assert.assertEquals(false, oleFormat.isLink());
 Assert.assertEquals(false, oleFormat.getOleIcon());

 oleFormat = shapeList.get(1).getOleFormat();

 Assert.assertEquals(true, oleFormat.isLink());
 Assert.assertEquals(true, oleFormat.getOleIcon());

 Assert.assertTrue(oleFormat.getSourceFullName().endsWith("Images" + File.separator + "Microsoft Visio drawing.vsd"));
 Assert.assertEquals("", oleFormat.getSourceItem());

 Assert.assertEquals("Microsoft Visio drawing.vsd", oleFormat.getIconCaption());

 doc.save(getArtifactsDir() + "Shape.OleLinks.docx");

 // If the object contains OLE data, we can access it using a stream.
 byte[] oleEntryBytes = oleFormat.getOleEntry("CompObj");
 Assert.assertEquals(76, oleEntryBytes.length);
 
```

**Returns:**
java.lang.String - Il percorso e il nome del file sorgente per l'oggetto OLE collegato.
### getSourceItem() {#getSourceItem}
```
public String getSourceItem()
```


Ottiene una stringa usata per identificare la parte del file sorgente che viene collegata.

 **Remarks:** 

Il valore predefinito è una stringa vuota.

Ad esempio, se il file sorgente è una cartella di lavoro Microsoft Excel, la proprietà [getSourceItem()](../../com.aspose.words/oleformat/\#getSourceItem) / [setSourceItem(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceItem-java.lang.String) potrebbe restituire "Workbook1!R3C1:R4C2" se l'oggetto OLE contiene solo alcune celle del foglio di lavoro.

 **Examples:** 

Mostra come inserire oggetti OLE collegati e non collegati.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Embed a Microsoft Visio drawing into the document as an OLE object.
 builder.insertOleObject(getImageDir() + "Microsoft Visio drawing.vsd", "Package", false, false, new FileInputStream(getImageDir() + "Transparent background logo.png"));

 // Insert a link to the file in the local file system and display it as an icon.
 builder.insertOleObject(getImageDir() + "Microsoft Visio drawing.vsd", "Package", true, true, new FileInputStream(getImageDir() + "Transparent background logo.png"));

 // Inserting OLE objects creates shapes that store these objects.
 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(2, shapeList.size());
 Assert.assertEquals(2, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.OLE_OBJECT));

 // If a shape contains an OLE object, it will have a valid "OleFormat" property,
 // which we can use to verify some aspects of the shape.
 OleFormat oleFormat = shapeList.get(0).getOleFormat();

 Assert.assertEquals(false, oleFormat.isLink());
 Assert.assertEquals(false, oleFormat.getOleIcon());

 oleFormat = shapeList.get(1).getOleFormat();

 Assert.assertEquals(true, oleFormat.isLink());
 Assert.assertEquals(true, oleFormat.getOleIcon());

 Assert.assertTrue(oleFormat.getSourceFullName().endsWith("Images" + File.separator + "Microsoft Visio drawing.vsd"));
 Assert.assertEquals("", oleFormat.getSourceItem());

 Assert.assertEquals("Microsoft Visio drawing.vsd", oleFormat.getIconCaption());

 doc.save(getArtifactsDir() + "Shape.OleLinks.docx");

 // If the object contains OLE data, we can access it using a stream.
 byte[] oleEntryBytes = oleFormat.getOleEntry("CompObj");
 Assert.assertEquals(76, oleEntryBytes.length);
 
```

**Returns:**
java.lang.String - Una stringa utilizzata per identificare la porzione del file sorgente che viene collegata.
### getSuggestedExtension() {#getSuggestedExtension}
```
public String getSuggestedExtension()
```


Ottiene l'estensione del file suggerita per l'oggetto incorporato corrente se si desidera salvarlo in un file.

 **Examples:** 

Mostra come estrarre oggetti OLE incorporati in file.

```

 Document doc = new Document(getMyDir() + "OLE spreadsheet.docm");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 // The OLE object in the first shape is a Microsoft Excel spreadsheet.
 OleFormat oleFormat = shape.getOleFormat();

 Assert.assertEquals("Excel.Sheet.12", oleFormat.getProgId());

 // Our object is neither auto updating nor locked from updates.
 Assert.assertFalse(oleFormat.getAutoUpdate());
 Assert.assertEquals(oleFormat.isLocked(), false);

 // If we plan on saving the OLE object to a file in the local file system,
 // we can use the "SuggestedExtension" property to determine which file extension to apply to the file.
 Assert.assertEquals(".xlsx", oleFormat.getSuggestedExtension());

 // Below are two ways of saving an OLE object to a file in the local file system.
 // 1 -  Save it via a stream:
 OutputStream fs = new FileOutputStream(getArtifactsDir() + "OLE spreadsheet extracted via stream" + oleFormat.getSuggestedExtension());
 try {
     oleFormat.save(fs);
 } finally {
     if (fs != null) fs.close();
 }

 // 2 -  Save it directly to a filename:
 oleFormat.save(getArtifactsDir() + "OLE spreadsheet saved directly" + oleFormat.getSuggestedExtension());
 
```

**Returns:**
java.lang.String - L'estensione di file suggerita per l'oggetto incorporato corrente se si desidera salvarlo in un file.
### getSuggestedFileName() {#getSuggestedFileName}
```
public String getSuggestedFileName()
```


Ottiene il nome del file suggerito per l'oggetto incorporato corrente se si desidera salvarlo in un file.

 **Examples:** 

Mostra come ottenere il nome file suggerito per un oggetto OLE.

```

 Document doc = new Document(getMyDir() + "OLE shape.rtf");

 Shape oleShape = (Shape) doc.getFirstSection().getBody().getChild(NodeType.SHAPE, 0, true);

 // OLE objects can provide a suggested filename and extension,
 // which we can use when saving the object's contents into a file in the local file system.
 String suggestedFileName = oleShape.getOleFormat().getSuggestedFileName();

 Assert.assertEquals("CSV.csv", suggestedFileName);

 OutputStream fileStream = new FileOutputStream(getArtifactsDir() + suggestedFileName);
 try {
     oleShape.getOleFormat().save(fileStream);
 } finally {
     if (fileStream != null) fileStream.close();
 }
 
```

**Returns:**
java.lang.String - Il nome file suggerito per l'oggetto incorporato corrente se si desidera salvarlo in un file.
### isLink() {#isLink}
```
public boolean isLink()
```


Restituisce  true  se l'oggetto OLE è collegato (quando [getSourceFullName()](../../com.aspose.words/oleformat/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceFullName-java.lang.String) è specificato).

 **Examples:** 

Mostra come inserire oggetti OLE collegati e non collegati.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Embed a Microsoft Visio drawing into the document as an OLE object.
 builder.insertOleObject(getImageDir() + "Microsoft Visio drawing.vsd", "Package", false, false, new FileInputStream(getImageDir() + "Transparent background logo.png"));

 // Insert a link to the file in the local file system and display it as an icon.
 builder.insertOleObject(getImageDir() + "Microsoft Visio drawing.vsd", "Package", true, true, new FileInputStream(getImageDir() + "Transparent background logo.png"));

 // Inserting OLE objects creates shapes that store these objects.
 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(2, shapeList.size());
 Assert.assertEquals(2, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.OLE_OBJECT));

 // If a shape contains an OLE object, it will have a valid "OleFormat" property,
 // which we can use to verify some aspects of the shape.
 OleFormat oleFormat = shapeList.get(0).getOleFormat();

 Assert.assertEquals(false, oleFormat.isLink());
 Assert.assertEquals(false, oleFormat.getOleIcon());

 oleFormat = shapeList.get(1).getOleFormat();

 Assert.assertEquals(true, oleFormat.isLink());
 Assert.assertEquals(true, oleFormat.getOleIcon());

 Assert.assertTrue(oleFormat.getSourceFullName().endsWith("Images" + File.separator + "Microsoft Visio drawing.vsd"));
 Assert.assertEquals("", oleFormat.getSourceItem());

 Assert.assertEquals("Microsoft Visio drawing.vsd", oleFormat.getIconCaption());

 doc.save(getArtifactsDir() + "Shape.OleLinks.docx");

 // If the object contains OLE data, we can access it using a stream.
 byte[] oleEntryBytes = oleFormat.getOleEntry("CompObj");
 Assert.assertEquals(76, oleEntryBytes.length);
 
```

**Returns:**
boolean -  true  se l'oggetto OLE è collegato (quando [getSourceFullName()](../../com.aspose.words/oleformat/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceFullName-java.lang.String) è specificato).
### isLocked() {#isLocked}
```
public boolean isLocked()
```


Specifica se il collegamento all'oggetto OLE è bloccato dagli aggiornamenti.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come estrarre oggetti OLE incorporati in file.

```

 Document doc = new Document(getMyDir() + "OLE spreadsheet.docm");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 // The OLE object in the first shape is a Microsoft Excel spreadsheet.
 OleFormat oleFormat = shape.getOleFormat();

 Assert.assertEquals("Excel.Sheet.12", oleFormat.getProgId());

 // Our object is neither auto updating nor locked from updates.
 Assert.assertFalse(oleFormat.getAutoUpdate());
 Assert.assertEquals(oleFormat.isLocked(), false);

 // If we plan on saving the OLE object to a file in the local file system,
 // we can use the "SuggestedExtension" property to determine which file extension to apply to the file.
 Assert.assertEquals(".xlsx", oleFormat.getSuggestedExtension());

 // Below are two ways of saving an OLE object to a file in the local file system.
 // 1 -  Save it via a stream:
 OutputStream fs = new FileOutputStream(getArtifactsDir() + "OLE spreadsheet extracted via stream" + oleFormat.getSuggestedExtension());
 try {
     oleFormat.save(fs);
 } finally {
     if (fs != null) fs.close();
 }

 // 2 -  Save it directly to a filename:
 oleFormat.save(getArtifactsDir() + "OLE spreadsheet saved directly" + oleFormat.getSuggestedExtension());
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### isLocked(boolean value) {#isLocked-boolean}
```
public void isLocked(boolean value)
```


Specifica se il collegamento all'oggetto OLE è bloccato dagli aggiornamenti.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come estrarre oggetti OLE incorporati in file.

```

 Document doc = new Document(getMyDir() + "OLE spreadsheet.docm");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 // The OLE object in the first shape is a Microsoft Excel spreadsheet.
 OleFormat oleFormat = shape.getOleFormat();

 Assert.assertEquals("Excel.Sheet.12", oleFormat.getProgId());

 // Our object is neither auto updating nor locked from updates.
 Assert.assertFalse(oleFormat.getAutoUpdate());
 Assert.assertEquals(oleFormat.isLocked(), false);

 // If we plan on saving the OLE object to a file in the local file system,
 // we can use the "SuggestedExtension" property to determine which file extension to apply to the file.
 Assert.assertEquals(".xlsx", oleFormat.getSuggestedExtension());

 // Below are two ways of saving an OLE object to a file in the local file system.
 // 1 -  Save it via a stream:
 OutputStream fs = new FileOutputStream(getArtifactsDir() + "OLE spreadsheet extracted via stream" + oleFormat.getSuggestedExtension());
 try {
     oleFormat.save(fs);
 } finally {
     if (fs != null) fs.close();
 }

 // 2 -  Save it directly to a filename:
 oleFormat.save(getArtifactsDir() + "OLE spreadsheet saved directly" + oleFormat.getSuggestedExtension());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### save(OutputStream stream) {#save-java.io.OutputStream}
```
public void save(OutputStream stream)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | java.io.OutputStream |  |

### save(String fileName) {#save-java.lang.String}
```
public void save(String fileName)
```


Salva i dati dell'oggetto incorporato in un file con il nome specificato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | java.lang.String | Nome del file per salvare i dati dell'oggetto OLE. |

### setAutoUpdate(boolean value) {#setAutoUpdate-boolean}
```
public void setAutoUpdate(boolean value)
```


Specifica se il collegamento all'oggetto OLE viene aggiornato automaticamente o meno in Microsoft Word.

 **Remarks:** 

Il valore predefinito è  false .

 **Examples:** 

Mostra come estrarre oggetti OLE incorporati in file.

```

 Document doc = new Document(getMyDir() + "OLE spreadsheet.docm");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 // The OLE object in the first shape is a Microsoft Excel spreadsheet.
 OleFormat oleFormat = shape.getOleFormat();

 Assert.assertEquals("Excel.Sheet.12", oleFormat.getProgId());

 // Our object is neither auto updating nor locked from updates.
 Assert.assertFalse(oleFormat.getAutoUpdate());
 Assert.assertEquals(oleFormat.isLocked(), false);

 // If we plan on saving the OLE object to a file in the local file system,
 // we can use the "SuggestedExtension" property to determine which file extension to apply to the file.
 Assert.assertEquals(".xlsx", oleFormat.getSuggestedExtension());

 // Below are two ways of saving an OLE object to a file in the local file system.
 // 1 -  Save it via a stream:
 OutputStream fs = new FileOutputStream(getArtifactsDir() + "OLE spreadsheet extracted via stream" + oleFormat.getSuggestedExtension());
 try {
     oleFormat.save(fs);
 } finally {
     if (fs != null) fs.close();
 }

 // 2 -  Save it directly to a filename:
 oleFormat.save(getArtifactsDir() + "OLE spreadsheet saved directly" + oleFormat.getSuggestedExtension());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setProgId(String value) {#setProgId-java.lang.String}
```
public void setProgId(String value)
```


Imposta il ProgID dell'oggetto OLE.

 **Remarks:** 

La proprietà ProgID non è sempre presente nei documenti Microsoft Word e non può essere considerata attendibile.

Non può essere  null .

Il valore predefinito è una stringa vuota.

 **Examples:** 

Mostra come estrarre oggetti OLE incorporati in file.

```

 Document doc = new Document(getMyDir() + "OLE spreadsheet.docm");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 // The OLE object in the first shape is a Microsoft Excel spreadsheet.
 OleFormat oleFormat = shape.getOleFormat();

 Assert.assertEquals("Excel.Sheet.12", oleFormat.getProgId());

 // Our object is neither auto updating nor locked from updates.
 Assert.assertFalse(oleFormat.getAutoUpdate());
 Assert.assertEquals(oleFormat.isLocked(), false);

 // If we plan on saving the OLE object to a file in the local file system,
 // we can use the "SuggestedExtension" property to determine which file extension to apply to the file.
 Assert.assertEquals(".xlsx", oleFormat.getSuggestedExtension());

 // Below are two ways of saving an OLE object to a file in the local file system.
 // 1 -  Save it via a stream:
 OutputStream fs = new FileOutputStream(getArtifactsDir() + "OLE spreadsheet extracted via stream" + oleFormat.getSuggestedExtension());
 try {
     oleFormat.save(fs);
 } finally {
     if (fs != null) fs.close();
 }

 // 2 -  Save it directly to a filename:
 oleFormat.save(getArtifactsDir() + "OLE spreadsheet saved directly" + oleFormat.getSuggestedExtension());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il ProgID dell'oggetto OLE. |

### setSourceFullName(String value) {#setSourceFullName-java.lang.String}
```
public void setSourceFullName(String value)
```


Imposta il percorso e il nome del file sorgente per l'oggetto OLE collegato.

 **Remarks:** 

Il valore predefinito è una stringa vuota.

Se [getSourceFullName()](../../com.aspose.words/oleformat/\#getSourceFullName) / [setSourceFullName(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceFullName-java.lang.String) non è una stringa vuota, l'oggetto OLE è collegato.

 **Examples:** 

Mostra come inserire oggetti OLE collegati e non collegati.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Embed a Microsoft Visio drawing into the document as an OLE object.
 builder.insertOleObject(getImageDir() + "Microsoft Visio drawing.vsd", "Package", false, false, new FileInputStream(getImageDir() + "Transparent background logo.png"));

 // Insert a link to the file in the local file system and display it as an icon.
 builder.insertOleObject(getImageDir() + "Microsoft Visio drawing.vsd", "Package", true, true, new FileInputStream(getImageDir() + "Transparent background logo.png"));

 // Inserting OLE objects creates shapes that store these objects.
 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(2, shapeList.size());
 Assert.assertEquals(2, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.OLE_OBJECT));

 // If a shape contains an OLE object, it will have a valid "OleFormat" property,
 // which we can use to verify some aspects of the shape.
 OleFormat oleFormat = shapeList.get(0).getOleFormat();

 Assert.assertEquals(false, oleFormat.isLink());
 Assert.assertEquals(false, oleFormat.getOleIcon());

 oleFormat = shapeList.get(1).getOleFormat();

 Assert.assertEquals(true, oleFormat.isLink());
 Assert.assertEquals(true, oleFormat.getOleIcon());

 Assert.assertTrue(oleFormat.getSourceFullName().endsWith("Images" + File.separator + "Microsoft Visio drawing.vsd"));
 Assert.assertEquals("", oleFormat.getSourceItem());

 Assert.assertEquals("Microsoft Visio drawing.vsd", oleFormat.getIconCaption());

 doc.save(getArtifactsDir() + "Shape.OleLinks.docx");

 // If the object contains OLE data, we can access it using a stream.
 byte[] oleEntryBytes = oleFormat.getOleEntry("CompObj");
 Assert.assertEquals(76, oleEntryBytes.length);
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il percorso e il nome del file sorgente per l'oggetto OLE collegato. |

### setSourceItem(String value) {#setSourceItem-java.lang.String}
```
public void setSourceItem(String value)
```


Imposta una stringa usata per identificare la parte del file sorgente che viene collegata.

 **Remarks:** 

Il valore predefinito è una stringa vuota.

Ad esempio, se il file sorgente è una cartella di lavoro Microsoft Excel, la proprietà [getSourceItem()](../../com.aspose.words/oleformat/\#getSourceItem) / [setSourceItem(java.lang.String)](../../com.aspose.words/oleformat/\#setSourceItem-java.lang.String) potrebbe restituire "Workbook1!R3C1:R4C2" se l'oggetto OLE contiene solo alcune celle del foglio di lavoro.

 **Examples:** 

Mostra come inserire oggetti OLE collegati e non collegati.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Embed a Microsoft Visio drawing into the document as an OLE object.
 builder.insertOleObject(getImageDir() + "Microsoft Visio drawing.vsd", "Package", false, false, new FileInputStream(getImageDir() + "Transparent background logo.png"));

 // Insert a link to the file in the local file system and display it as an icon.
 builder.insertOleObject(getImageDir() + "Microsoft Visio drawing.vsd", "Package", true, true, new FileInputStream(getImageDir() + "Transparent background logo.png"));

 // Inserting OLE objects creates shapes that store these objects.
 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(2, shapeList.size());
 Assert.assertEquals(2, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.OLE_OBJECT));

 // If a shape contains an OLE object, it will have a valid "OleFormat" property,
 // which we can use to verify some aspects of the shape.
 OleFormat oleFormat = shapeList.get(0).getOleFormat();

 Assert.assertEquals(false, oleFormat.isLink());
 Assert.assertEquals(false, oleFormat.getOleIcon());

 oleFormat = shapeList.get(1).getOleFormat();

 Assert.assertEquals(true, oleFormat.isLink());
 Assert.assertEquals(true, oleFormat.getOleIcon());

 Assert.assertTrue(oleFormat.getSourceFullName().endsWith("Images" + File.separator + "Microsoft Visio drawing.vsd"));
 Assert.assertEquals("", oleFormat.getSourceItem());

 Assert.assertEquals("Microsoft Visio drawing.vsd", oleFormat.getIconCaption());

 doc.save(getArtifactsDir() + "Shape.OleLinks.docx");

 // If the object contains OLE data, we can access it using a stream.
 byte[] oleEntryBytes = oleFormat.getOleEntry("CompObj");
 Assert.assertEquals(76, oleEntryBytes.length);
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Una stringa utilizzata per identificare la porzione del file sorgente che viene collegata. |

