---
title: "ImportFormatMode"
linktitle: "ImportFormatMode"
second_title: "Aspose.Words per Java"
description: "Specifica come la formattazione viene unita durante l'importazione di contenuti da un altro documento in Java."
type: docs
weight: 400
url: /it/java/com.aspose.words/importformatmode/
---

**Inheritance:**
java.lang.Object
```
public class ImportFormatMode
```

Specifica come la formattazione viene unita durante l'importazione di contenuti da un altro documento.

 **Remarks:** 

Quando copi nodi da un documento a un altro, questa opzione specifica come la formattazione viene risolta quando entrambi i documenti hanno uno stile con lo stesso nome, ma formattazioni diverse.

La formattazione viene risolta come segue:

1.  Gli stili predefiniti vengono abbinati usando il loro identificatore di stile indipendente dalla locale. Gli stili definiti dall'utente vengono abbinati usando il nome dello stile sensibile al maiuscolo/minuscolo.
2.  Se non viene trovato uno stile corrispondente nel documento di destinazione, lo stile (e tutti gli stili a cui fa riferimento) vengono copiati nel documento di destinazione e i nodi importati vengono aggiornati per fare riferimento al nuovo stile.
3.  Se uno stile corrispondente esiste già nel documento di destinazione, ciò che accade dipende dal parametro  importFormatMode  passato a **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** come descritto di seguito.

Quando si utilizza l'opzione [USE\\_DESTINATION\\_STYLES](../../com.aspose.words/importformatmode/\\#USE-DESTINATION-STYLES), se uno stile corrispondente esiste già nel documento di destinazione, lo stile non viene copiato e i nodi importati vengono aggiornati per fare riferimento allo stile esistente.

Lo svantaggio dell'utilizzo di [USE\\_DESTINATION\\_STYLES](../../com.aspose.words/importformatmode/\\#USE-DESTINATION-STYLES) è che il testo importato potrebbe apparire diverso nel documento di destinazione rispetto al documento di origine. Per esempio, lo stile \"Heading 1\" nel documento di origine utilizza il font Arial 16pt e lo stile \"Heading 1\" nel documento di destinazione utilizza il font Times New Roman 14pt. Quando si importa il testo con lo stile \"Heading 1\" senza altra formattazione diretta, apparirà con il font Times New Roman 14pt nel documento di destinazione.

[KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) option allows to make sure the imported content looks the same in the destination document like it looks in the source document. If a matching style already exists in the destination document, the source style formatting is expanded into direct Node attributes and the style is changed to Normal. If the style does not exist in the destination document, then the source style is imported into the destination document and applied to the imported node. Note, that it is not always possible to preserve the source style even if it does not exist in the destination document. In this case formatting of such style will be expanded into direct Node attributes in favor of preserving original Node formatting.

Lo svantaggio dell'utilizzo di [KEEP\\_SOURCE\\_FORMATTING](../../com.aspose.words/importformatmode/\\#KEEP-SOURCE-FORMATTING) è che, se esegui più importazioni, potresti finire con molti stili nel documento di destinazione e ciò potrebbe rendere difficile utilizzare una formattazione di stile coerente in Microsoft Word per questo documento.

L'utilizzo dell'opzione [KEEP\\_DIFFERENT\\_STYLES](../../com.aspose.words/importformatmode/\\#KEEP-DIFFERENT-STYLES) consente di riutilizzare gli stili di destinazione se la formattazione fornita è identica a quella degli stili nel documento di origine. Se lo stile nel documento di destinazione è diverso da quello di origine, allora viene importato.

 **Examples:** 

Mostra come inserire un documento in un altro documento.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.insertBreak(BreakType.PAGE_BREAK);

 Document docToInsert = new Document(getMyDir() + "Formatted elements.docx");

 builder.insertDocument(docToInsert, ImportFormatMode.KEEP_SOURCE_FORMATTING);
 builder.getDocument().save(getArtifactsDir() + "DocumentBuilder.InsertDocument.docx");
 
```

**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**
## Campi

| Campo | Descrizione |
| --- | --- |
| [KEEP_DIFFERENT_STYLES](#KEEP-DIFFERENT-STYLES) | Copia solo gli stili che sono diversi da quelli nel documento di origine. |
| [KEEP_SOURCE_FORMATTING](#KEEP-SOURCE-FORMATTING) | Copia tutti gli stili necessari nel documento di destinazione, generando nomi di stile unici se necessario. |
| [USE_DESTINATION_STYLES](#USE-DESTINATION-STYLES) | Utilizza gli stili del documento di destinazione e copia i nuovi stili. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String importFormatModeName)](#fromName-java.lang.String) |  |
| [getName(int importFormatMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int importFormatMode)](#toString-int) |  |
### KEEP_DIFFERENT_STYLES {#KEEP-DIFFERENT-STYLES}
```
public static int KEEP_DIFFERENT_STYLES
```


Copia solo gli stili che sono diversi da quelli nel documento di origine.

### KEEP_SOURCE_FORMATTING {#KEEP-SOURCE-FORMATTING}
```
public static int KEEP_SOURCE_FORMATTING
```


Copia tutti gli stili necessari nel documento di destinazione, generando nomi di stile unici se necessario.

### USE_DESTINATION_STYLES {#USE-DESTINATION-STYLES}
```
public static int USE_DESTINATION_STYLES
```


Utilizza gli stili del documento di destinazione e copia i nuovi stili. Questa è l'opzione predefinita.

### length {#length}
```
public static int length
```


### fromName(String importFormatModeName) {#fromName-java.lang.String}
```
public static int fromName(String importFormatModeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| importFormatModeName | java.lang.String |  |

**Returns:**
int
### getName(int importFormatMode) {#getName-int}
```
public static String getName(int importFormatMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| importFormatMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int importFormatMode) {#toString-int}
```
public static String toString(int importFormatMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| importFormatMode | int |  |

**Returns:**
java.lang.String
