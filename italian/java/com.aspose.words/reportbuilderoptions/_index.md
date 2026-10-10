---
title: "ReportBuilderOptions"
linktitle: "ReportBuilderOptions"
second_title: "Aspose.Words per Java"
description: "Rappresenta le opzioni per la funzionalità LINQ Reporting Engine in Java."
type: docs
weight: 573
url: /it/java/com.aspose.words/reportbuilderoptions/
---

**Inheritance:**
java.lang.Object
```
public class ReportBuilderOptions
```

Rappresenta le opzioni per la funzionalità di LINQ Reporting Engine.

 **Examples:** 

Mostra come popolare il documento con i dati.

```

 public void buildReportData() throws Exception {
     // There is a several ways to populate document with data:
     String doc = getMyDir() + "Reporting engine template - If greedy (Java).docx";

     AsposeData obj = new AsposeData();
     {
         obj.setList(new ArrayList<>());
         {
             obj.getList().add("abc");
         }
     }

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.1.docx", obj);
     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.2.docx", obj, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.3.docx", SaveFormat.DOCX, obj);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.4.docx", SaveFormat.DOCX, obj, options);
 }

 public static class AsposeData {
     public ArrayList getList() {
         return mList;
     }

     ;

     public void setList(ArrayList value) {
         mList = value;
     }

     ;

     private ArrayList mList;
 }
 
```
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [ReportBuilderOptions()](#ReportBuilderOptions) | Inizializza una nuova istanza di questa classe. |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getKnownTypes()](#getKnownTypes) | Ottiene un insieme non ordinato (ad es. |
| [getMissingMemberMessage()](#getMissingMemberMessage) | Ottiene un valore stringa stampato al posto di un'espressione modello che rappresenta un riferimento semplice a un membro mancante di un oggetto. |
| [getOptions()](#getOptions) | Ottiene un insieme di flag che controllano il comportamento di questa istanza di [ReportingEngine](../../com.aspose.words/reportingengine/) durante la generazione di un report. |
| [setMissingMemberMessage(String value)](#setMissingMemberMessage-java.lang.String) | Imposta un valore stringa stampato al posto di un'espressione modello che rappresenta un riferimento semplice a un membro mancante di un oggetto. |
| [setOptions(int value)](#setOptions-int) | Imposta un insieme di flag che controllano il comportamento di questa istanza di [ReportingEngine](../../com.aspose.words/reportingengine/) durante la generazione di un report. |
### ReportBuilderOptions() {#ReportBuilderOptions}
```
public ReportBuilderOptions()
```


Inizializza una nuova istanza di questa classe.

### getKnownTypes() {#getKnownTypes}
```
public KnownTypeSet getKnownTypes()
```


Ottiene un insieme non ordinato (cioè una collezione di elementi unici) contenente oggetti java.lang.Class i cui nomi completamente o parzialmente qualificati possono essere utilizzati nei modelli di report elaborati da questa istanza del motore per invocare i membri statici dei relativi tipi, eseguire conversioni di tipo, ecc.

**Returns:**
[KnownTypeSet](../../com.aspose.words/knowntypeset/) - An unordered set (i.e.
### getMissingMemberMessage() {#getMissingMemberMessage}
```
public String getMissingMemberMessage()
```


Ottiene un valore stringa stampato al posto di un'espressione modello che rappresenta un riferimento semplice a un membro mancante di un oggetto. Il valore predefinito è una stringa vuota.

 **Remarks:** 

La proprietà dovrebbe essere usata in combinazione con l'opzione [ReportBuildOptions.ALLOW\_MISSING\_MEMBERS](../../com.aspose.words/reportbuildoptions/\#ALLOW-MISSING-MEMBERS). Altrimenti, viene sollevata un'eccezione quando si incontra un membro mancante di un oggetto.

La proprietà influisce solo sulla stampa di un'espressione modello che rappresenta un riferimento semplice a un membro mancante dell'oggetto. Ad esempio, la stampa di un operatore binario, uno dei cui operandi fa riferimento a un membro mancante dell'oggetto, non è influenzata.

Il valore di questa proprietà non può essere impostato a null.

**Returns:**
java.lang.String - Un valore stringa stampato al posto di un'espressione modello che rappresenta un riferimento semplice a un membro mancante di un oggetto.
### getOptions() {#getOptions}
```
public int getOptions()
```


Ottiene un insieme di flag che controllano il comportamento di questa istanza di [ReportingEngine](../../com.aspose.words/reportingengine/) durante la generazione di un report.

 **Examples:** 

Mostra come popolare il documento con i dati.

```

 public void buildReportData() throws Exception {
     // There is a several ways to populate document with data:
     String doc = getMyDir() + "Reporting engine template - If greedy (Java).docx";

     AsposeData obj = new AsposeData();
     {
         obj.setList(new ArrayList<>());
         {
             obj.getList().add("abc");
         }
     }

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.1.docx", obj);
     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.2.docx", obj, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.3.docx", SaveFormat.DOCX, obj);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.4.docx", SaveFormat.DOCX, obj, options);
 }

 public static class AsposeData {
     public ArrayList getList() {
         return mList;
     }

     ;

     public void setList(ArrayList value) {
         mList = value;
     }

     ;

     private ArrayList mList;
 }
 
```

**Returns:**
int - Un insieme di flag che controllano il comportamento di questa istanza di [ReportingEngine](../../com.aspose.words/reportingengine/) durante la generazione di un report. Il valore restituito è una combinazione bitwise delle costanti di [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/).
### setMissingMemberMessage(String value) {#setMissingMemberMessage-java.lang.String}
```
public void setMissingMemberMessage(String value)
```


Imposta un valore stringa stampato al posto di un'espressione modello che rappresenta un riferimento semplice a un membro mancante di un oggetto. Il valore predefinito è una stringa vuota.

 **Remarks:** 

La proprietà dovrebbe essere usata in combinazione con l'opzione [ReportBuildOptions.ALLOW\_MISSING\_MEMBERS](../../com.aspose.words/reportbuildoptions/\#ALLOW-MISSING-MEMBERS). Altrimenti, viene sollevata un'eccezione quando si incontra un membro mancante di un oggetto.

La proprietà influisce solo sulla stampa di un'espressione modello che rappresenta un riferimento semplice a un membro mancante dell'oggetto. Ad esempio, la stampa di un operatore binario, uno dei cui operandi fa riferimento a un membro mancante dell'oggetto, non è influenzata.

Il valore di questa proprietà non può essere impostato a null.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Un valore stringa stampato al posto di un'espressione modello che rappresenta un riferimento semplice a un membro mancante di un oggetto. |

### setOptions(int value) {#setOptions-int}
```
public void setOptions(int value)
```


Imposta un insieme di flag che controllano il comportamento di questa istanza di [ReportingEngine](../../com.aspose.words/reportingengine/) durante la generazione di un report.

 **Examples:** 

Mostra come popolare il documento con i dati.

```

 public void buildReportData() throws Exception {
     // There is a several ways to populate document with data:
     String doc = getMyDir() + "Reporting engine template - If greedy (Java).docx";

     AsposeData obj = new AsposeData();
     {
         obj.setList(new ArrayList<>());
         {
             obj.getList().add("abc");
         }
     }

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.1.docx", obj);
     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.2.docx", obj, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.3.docx", SaveFormat.DOCX, obj);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.4.docx", SaveFormat.DOCX, obj, options);
 }

 public static class AsposeData {
     public ArrayList getList() {
         return mList;
     }

     ;

     public void setList(ArrayList value) {
         mList = value;
     }

     ;

     private ArrayList mList;
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Un insieme di flag che controllano il comportamento di questa istanza di [ReportingEngine](../../com.aspose.words/reportingengine/) durante la generazione di un report. Il valore deve essere una combinazione bitwise delle costanti di [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/). |

