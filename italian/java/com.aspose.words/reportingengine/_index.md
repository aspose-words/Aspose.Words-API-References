---
title: "ReportingEngine"
linktitle: "ReportingEngine"
second_title: "Aspose.Words per Java"
description: "Fornisce routine per popolare documenti modello con dati e un insieme di impostazioni per controllare queste routine in Java."
type: docs
weight: 574
url: /it/java/com.aspose.words/reportingengine/
---

**Inheritance:**
java.lang.Object
```
public class ReportingEngine
```

Fornisce routine per popolare i documenti modello con i dati e un insieme di impostazioni per controllare queste routine.

Per saperne di più, visita l'articolo di documentazione [ LINQ Reporting Engine ][LINQ Reporting Engine].


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [ReportingEngine()](#ReportingEngine) | Inizializza una nuova istanza di questa classe. |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [buildReport(Document document, Object dataSource)](#buildReport-com.aspose.words.Document-java.lang.Object) | Popola il documento modello specificato con i dati dalla fonte specificata rendendolo un report pronto. |
| [buildReport(Document document, Object dataSource, String dataSourceName)](#buildReport-com.aspose.words.Document-java.lang.Object-java.lang.String) | Popola il documento modello specificato con i dati dalla fonte specificata rendendolo un report pronto. |
| [buildReport(Document document, Object[] dataSources, String[] dataSourceNames)](#buildReport-com.aspose.words.Document-java.lang.Object---java.lang.String) | Popola il documento modello specificato con i dati dalle fonti specificate rendendolo un report pronto. |
| [equals(Object obj)](#equals-java.lang.Object) |  |
| [getKnownTypes()](#getKnownTypes) | Ottiene un insieme non ordinato (ad es. |
| [getMissingMemberMessage()](#getMissingMemberMessage) | Ottiene un valore stringa stampato al posto di un'espressione modello che rappresenta un riferimento semplice a un membro mancante di un oggetto. |
| [getOptions()](#getOptions) | Ottiene un insieme di flag che controllano il comportamento di questa istanza di [ReportingEngine](../../com.aspose.words/reportingengine/) durante la generazione di un report. |
| [getRestrictedTypes()](#getRestrictedTypes) | Restituisce i tipi i cui membri, così come i membri dei tipi derivati, devono essere inaccessibili al motore tramite la sintassi del modello. |
| [getUseReflectionOptimization()](#getUseReflectionOptimization) | Ottiene un valore che indica se le invocazioni dei membri di tipo personalizzato eseguite tramite l'API di riflessione sono ottimizzate usando la generazione dinamica di classi o meno. |
| [hashCode()](#hashCode) |  |
| [setMissingMemberMessage(String value)](#setMissingMemberMessage-java.lang.String) | Imposta un valore stringa stampato al posto di un'espressione modello che rappresenta un riferimento semplice a un membro mancante di un oggetto. |
| [setOptions(int value)](#setOptions-int) | Imposta un insieme di flag che controllano il comportamento di questa istanza di [ReportingEngine](../../com.aspose.words/reportingengine/) durante la generazione di un report. |
| [setRestrictedTypes(Class[] types)](#setRestrictedTypes-java.lang.Class...) | Specifica i tipi i cui membri, così come i membri dei tipi derivati, devono essere inaccessibili al motore tramite la sintassi del modello. |
| [setUseReflectionOptimization(boolean value)](#setUseReflectionOptimization-boolean) | Imposta un valore che indica se le invocazioni dei membri di tipo personalizzato eseguite tramite l'API di riflessione sono ottimizzate usando la generazione dinamica di classi o meno. |
### ReportingEngine() {#ReportingEngine}
```
public ReportingEngine()
```


Inizializza una nuova istanza di questa classe.

### buildReport(Document document, Object dataSource) {#buildReport-com.aspose.words.Document-java.lang.Object}
```
public boolean buildReport(Document document, Object dataSource)
```


Popola il documento modello specificato con i dati dalla fonte specificata rendendolo un report pronto.

 **Remarks:** 

Utilizzando questo overload è possibile fare riferimento ai membri della fonte dati nel documento modello, ma non è possibile fare riferimento all'oggetto della fonte dati stesso. È consigliato usare l'overload [buildReport(com.aspose.words.Document, java.lang.Object, java.lang.String)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object--java.lang.String) per ottenere questo risultato.

Un oggetto fonte dati può essere di uno dei seguenti tipi:

 *  [XmlDataSource](../../com.aspose.words/xmldatasource/)
 *  [JsonDataSource](../../com.aspose.words/jsondatasource/)
 *  [CsvDataSource](../../com.aspose.words/csvdatasource/)
 *  [DataSet](../../com.aspose.words.net.system.data/dataset/)
 *  [DataTable](../../com.aspose.words.net.system.data/datatable/)
 *  [DataRow](../../com.aspose.words.net.system.data/datarow/)
 *  [IDataReader](../../com.aspose.words.net.system.data/idatareader/)
 *  [IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
 *  [DataView](../../com.aspose.words.net.system.data/dataview/)
 *  [DataRowView](../../com.aspose.words.net.system.data/datarowview/)
 *  Any other arbitrary Java type

Per informazioni su come lavorare con fonti dati di diversi tipi nei documenti modello, vedere il riferimento alla sintassi del modello(https://docs.aspose.com/display/wordsjava/Template+Syntax).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | Un documento modello da popolare con i dati. |
| dataSource | java.lang.Object | Un oggetto fonte dati. |

**Returns:**
boolean - Un flag che indica se l'analisi del documento modello è avvenuta con successo. Il flag restituito ha senso solo se il valore della proprietà [getOptions()](../../com.aspose.words/reportingengine/\#getOptions) / [setOptions(int)](../../com.aspose.words/reportingengine/\#setOptions-int) include l'opzione [ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions/\#INLINE-ERROR-MESSAGES).
### buildReport(Document document, Object dataSource, String dataSourceName) {#buildReport-com.aspose.words.Document-java.lang.Object-java.lang.String}
```
public boolean buildReport(Document document, Object dataSource, String dataSourceName)
```


Popola il documento modello specificato con i dati dalla fonte specificata rendendolo un report pronto.

 **Remarks:** 

Utilizzando questo overload è possibile fare riferimento ai membri della fonte dati e all'oggetto della fonte dati stesso nel modello. Se non si intende fare riferimento all'oggetto della fonte dati, è possibile omettere  dataSourceName  passando  null  o usare l'overload [buildReport(com.aspose.words.Document, java.lang.Object)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object).

Un oggetto fonte dati può essere di uno dei seguenti tipi:

 *  [XmlDataSource](../../com.aspose.words/xmldatasource/)
 *  [JsonDataSource](../../com.aspose.words/jsondatasource/)
 *  [CsvDataSource](../../com.aspose.words/csvdatasource/)
 *  [DataSet](../../com.aspose.words.net.system.data/dataset/)
 *  [DataTable](../../com.aspose.words.net.system.data/datatable/)
 *  [DataRow](../../com.aspose.words.net.system.data/datarow/)
 *  [IDataReader](../../com.aspose.words.net.system.data/idatareader/)
 *  [IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
 *  [DataView](../../com.aspose.words.net.system.data/dataview/)
 *  [DataRowView](../../com.aspose.words.net.system.data/datarowview/)
 *  Any other arbitrary Java type

Per informazioni su come lavorare con fonti dati di diversi tipi nei documenti modello, vedere il riferimento alla sintassi del modello(https://docs.aspose.com/display/wordsjava/Template+Syntax).

 **Examples:** 

Mostra come consentire membri mancanti.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

Mostra come visualizzare i valori come testo in dollari.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("<<[ds.getValue1()]:dollarText>>\r<<[ds.getValue2()]:dollarText>>");

 NumericTestClass testData = new NumericTestBuilder().withValues(1234, 5621718.589).build();

 ReportingEngine report = new ReportingEngine();
 report.getKnownTypes().add(NumericTestClass.class);
 report.buildReport(doc, testData, "ds");

 doc.save(getArtifactsDir() + "ReportingEngine.DollarTextFormat.docx");
 
```

Mostra come rimuovere i paragrafi in modo selettivo.

```

 // Template contains tags with an exclamation mark. For such tags, empty paragraphs will be removed.
 Document doc = new Document(getMyDir() + "Reporting engine template - Selective remove paragraphs.docx");

 ReportingEngine engine = new ReportingEngine();
 engine.buildReport(doc, false, "value");

 doc.save(getArtifactsDir() + "ReportingEngine.SelectiveDeletionOfParagraphs.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | Un documento modello da popolare con i dati. |
| dataSource | java.lang.Object | Un oggetto fonte dati. |
| dataSourceName | java.lang.String | Un nome per fare riferimento all'oggetto fonte dati nel modello. |

**Returns:**
boolean - Un flag che indica se l'analisi del documento modello è avvenuta con successo. Il flag restituito ha senso solo se il valore della proprietà [getOptions()](../../com.aspose.words/reportingengine/\#getOptions) / [setOptions(int)](../../com.aspose.words/reportingengine/\#setOptions-int) include l'opzione [ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions/\#INLINE-ERROR-MESSAGES).
### buildReport(Document document, Object[] dataSources, String[] dataSourceNames) {#buildReport-com.aspose.words.Document-java.lang.Object---java.lang.String}
```
public boolean buildReport(Document document, Object[] dataSources, String[] dataSourceNames)
```


Popola il documento modello specificato con i dati dalle fonti specificate rendendolo un report pronto.

 **Remarks:** 

Utilizzando questo overload è possibile fare riferimento a più oggetti fonte dati e ai loro membri nel modello. Il nome della prima fonte dati può essere omesso (cioè una stringa vuota o  null ) se si intende fare riferimento ai membri della fonte dati ma non all'oggetto della fonte dati stesso. I nomi delle altre fonti dati devono essere specificati e unici.

Se si intende utilizzare una singola fonte dati, considerare l'uso degli overload [buildReport(com.aspose.words.Document, java.lang.Object)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object) e [buildReport(com.aspose.words.Document, java.lang.Object, java.lang.String)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object--java.lang.String) invece.

Un oggetto fonte dati può essere di uno dei seguenti tipi:

 *  [XmlDataSource](../../com.aspose.words/xmldatasource/)
 *  [JsonDataSource](../../com.aspose.words/jsondatasource/)
 *  [CsvDataSource](../../com.aspose.words/csvdatasource/)
 *  [DataSet](../../com.aspose.words.net.system.data/dataset/)
 *  [DataTable](../../com.aspose.words.net.system.data/datatable/)
 *  [DataRow](../../com.aspose.words.net.system.data/datarow/)
 *  [IDataReader](../../com.aspose.words.net.system.data/idatareader/)
 *  [IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
 *  [DataView](../../com.aspose.words.net.system.data/dataview/)
 *  [DataRowView](../../com.aspose.words.net.system.data/datarowview/)
 *  Any other arbitrary Java type

Per informazioni su come lavorare con fonti dati di diversi tipi nei documenti modello, vedere il riferimento alla sintassi del modello(https://docs.aspose.com/display/wordsjava/Template+Syntax).

 **Examples:** 

Mostra come mantenere la numerazione inserita invariata.

```

 // By default, numbered lists from a template document are continued when their identifiers match those from a document being inserted.
 // With "-sourceNumbering" numbering should be separated and kept as is.
 Document template = DocumentHelper.createSimpleDocument("<>" + System.lineSeparator() + "<>");

 DocumentTestClass doc = new DocumentTestBuilder()
         .withDocument(new Document(getMyDir() + "List item.docx")).build();

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.REMOVE_EMPTY_PARAGRAPHS); }
 engine.buildReport(template, new Object[] { doc }, new String[] { "src" });

 template.save(getArtifactsDir() + "ReportingEngine.SourseListNumbering.docx");
 
```

Mostra come lavorare con i grafici da Word 2016.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Word 2016 Charts (Java).docx");

 ReportingEngine engine = new ReportingEngine();
 engine.buildReport(doc, new Object[] { Common.getShares(), Common.getShareQuotes() },
         new String[] { "shares", "quotes" });

 doc.save(getArtifactsDir() + "ReportingEngine.Word2016Charts.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | Un documento modello da popolare con i dati. |
| dataSources | java.lang.Object[] | Un array di oggetti data source. |
| dataSourceNames | java.lang.String[] | Un array di nomi per fare riferimento agli oggetti data source all'interno del modello. |

**Returns:**
boolean - Un flag che indica se l'analisi del documento modello è avvenuta con successo. Il flag restituito ha senso solo se il valore della proprietà [getOptions()](../../com.aspose.words/reportingengine/\#getOptions) / [setOptions(int)](../../com.aspose.words/reportingengine/\#setOptions-int) include l'opzione [ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions/\#INLINE-ERROR-MESSAGES).
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
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

 **Examples:** 

Mostra come consentire membri mancanti.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

**Returns:**
java.lang.String - Un valore stringa stampato al posto di un'espressione modello che rappresenta un riferimento semplice a un membro mancante di un oggetto.
### getOptions() {#getOptions}
```
public int getOptions()
```


Ottiene un insieme di flag che controllano il comportamento di questa istanza di [ReportingEngine](../../com.aspose.words/reportingengine/) durante la generazione di un report.

 **Examples:** 

Mostra come consentire membri mancanti.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

Mostra come impostare le opzioni per Reporting Engine

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Fields (Java).docx");

 // Note that enabling of the option makes the engine to update fields while building a report,
 // so there is no need to update fields separately after that.
 ReportingEngine engine = new ReportingEngine();
 engine.setOptions(ReportBuildOptions.UPDATE_FIELDS_SYNTAX_AWARE);
 engine.buildReport(doc, new String[] { "First topic", "Second topic", "Third topic" }, "topics");

 doc.save(getArtifactsDir() + "ReportingEngine.UpdateFieldsSyntaxAware.docx");
 
```

**Returns:**
int - Un insieme di flag che controllano il comportamento di questa istanza di [ReportingEngine](../../com.aspose.words/reportingengine/) durante la generazione di un report. Il valore restituito è una combinazione bitwise delle costanti di [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/).
### getRestrictedTypes() {#getRestrictedTypes}
```
public static Class[] getRestrictedTypes()
```


Restituisce i tipi i cui membri, così come i membri dei tipi derivati, devono essere inaccessibili al motore tramite la sintassi del modello.

 **Remarks:** 

L'array restituito contiene elementi precedentemente impostati usando [setRestrictedTypes(java.lang.Class[])](../../com.aspose.words/reportingengine/\#setRestrictedTypes-java.lang.Class).

Modificare gli elementi dell'array restituito non ha effetto sui tipi limitati. Per modificare i tipi limitati, usa [setRestrictedTypes(java.lang.Class[])](../../com.aspose.words/reportingengine/\#setRestrictedTypes-java.lang.Class) invece.

**Returns:**
java.lang.Class[] - Tipi i cui membri, così come i membri dei tipi derivati, devono essere inaccessibili al motore tramite la sintassi del modello.
### getUseReflectionOptimization() {#getUseReflectionOptimization}
```
public static boolean getUseReflectionOptimization()
```


Restituisce un valore che indica se le invocazioni dei membri di tipo personalizzato eseguite tramite l'API di reflection sono ottimizzate usando la generazione dinamica di classi o meno. Il valore predefinito è  true .

 **Remarks:** 

Ci sono alcuni scenari in cui è preferibile disabilitare questa ottimizzazione. Ad esempio, se si lavora continuamente con piccole collezioni di elementi dati, allora l'overhead della generazione dinamica di classi può risultare più evidente rispetto all'overhead delle chiamate dirette all'API di reflection. L'opzione non ha effetto quando viene eseguita su iOS e l'ottimizzazione della reflection non è utilizzata.

**Returns:**
boolean - Un valore che indica se le invocazioni dei membri di tipo personalizzato eseguite tramite l'API di reflection sono ottimizzate usando la generazione dinamica di classi o meno.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### setMissingMemberMessage(String value) {#setMissingMemberMessage-java.lang.String}
```
public void setMissingMemberMessage(String value)
```


Imposta un valore stringa stampato al posto di un'espressione modello che rappresenta un riferimento semplice a un membro mancante di un oggetto. Il valore predefinito è una stringa vuota.

 **Remarks:** 

La proprietà dovrebbe essere usata in combinazione con l'opzione [ReportBuildOptions.ALLOW\_MISSING\_MEMBERS](../../com.aspose.words/reportbuildoptions/\#ALLOW-MISSING-MEMBERS). Altrimenti, viene sollevata un'eccezione quando si incontra un membro mancante di un oggetto.

La proprietà influisce solo sulla stampa di un'espressione modello che rappresenta un riferimento semplice a un membro mancante dell'oggetto. Ad esempio, la stampa di un operatore binario, uno dei cui operandi fa riferimento a un membro mancante dell'oggetto, non è influenzata.

Il valore di questa proprietà non può essere impostato a null.

 **Examples:** 

Mostra come consentire membri mancanti.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

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

Mostra come consentire membri mancanti.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

Mostra come impostare le opzioni per Reporting Engine

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Fields (Java).docx");

 // Note that enabling of the option makes the engine to update fields while building a report,
 // so there is no need to update fields separately after that.
 ReportingEngine engine = new ReportingEngine();
 engine.setOptions(ReportBuildOptions.UPDATE_FIELDS_SYNTAX_AWARE);
 engine.buildReport(doc, new String[] { "First topic", "Second topic", "Third topic" }, "topics");

 doc.save(getArtifactsDir() + "ReportingEngine.UpdateFieldsSyntaxAware.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Un insieme di flag che controllano il comportamento di questa istanza di [ReportingEngine](../../com.aspose.words/reportingengine/) durante la generazione di un report. Il valore deve essere una combinazione bitwise delle costanti di [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/). |

### setRestrictedTypes(Class[] types) {#setRestrictedTypes-java.lang.Class...}
```
public static void setRestrictedTypes(Class[] types)
```


Specifica i tipi i cui membri, così come i membri dei tipi derivati, devono essere inaccessibili al motore tramite la sintassi del modello.

 **Remarks:** 

I tipi limitati dovrebbero essere impostati prima della prima generazione di un report. Dopo che è stato invocato BuildReportbuildReport, i tipi limitati non possono essere modificati e viene sollevata un'eccezione se si tenta di farlo. Il momento migliore per impostare i tipi limitati è all'avvio dell'applicazione.

Nota che un gran numero di tipi limitati può influire sulle prestazioni, quindi è meglio limitare solo quei tipi i cui membri sono davvero sensibili.

Lancia java.lang.IllegalArgumentException nei seguenti casi:

\-  types  è null.

\- Uno degli elementi di  types  è  null .

\- Uno degli elementi di  types  rappresenta un tipo invisibile, cioè un tipo non pubblico o un tipo annidato pubblico che ha un tipo esterno non pubblico.

\- Uno degli elementi di  types  rappresenta un tipo array.

\-  types  contiene voci duplicate.

 **Examples:** 

Mostra come negare l'accesso ai membri di tipi considerati non sicuri.

```

 Document doc =
         DocumentHelper.createSimpleDocument(
                 "<><<[typeVar]>>");

 // Note, that you can't set restricted types during or after building a report.
 ReportingEngine.setRestrictedTypes(Class.class);
 // We set "AllowMissingMembers" option to avoid exceptions during building a report.
 ReportingEngine engine = new ReportingEngine();
 engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
 engine.buildReport(doc, new Object());

 // We get an empty string because we can't access the GetType() method.
 Assert.assertEquals(doc.getText().trim(), "");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| types | java.lang.Class[] | Tipi da limitare. |

### setUseReflectionOptimization(boolean value) {#setUseReflectionOptimization-boolean}
```
public static void setUseReflectionOptimization(boolean value)
```


Imposta un valore che indica se le invocazioni dei membri di tipo personalizzato eseguite tramite l'API di reflection sono ottimizzate usando la generazione dinamica di classi o meno. Il valore predefinito è  true .

 **Remarks:** 

Ci sono alcuni scenari in cui è preferibile disabilitare questa ottimizzazione. Ad esempio, se si lavora continuamente con piccole collezioni di elementi dati, allora l'overhead della generazione dinamica di classi può risultare più evidente rispetto all'overhead delle chiamate dirette all'API di reflection. L'opzione non ha effetto quando viene eseguita su iOS e l'ottimizzazione della reflection non è utilizzata.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Un valore che indica se le invocazioni dei membri di tipo personalizzato eseguite tramite l'API di reflection sono ottimizzate usando la generazione dinamica di classi o meno. |

