---
title: "MailMergeSettings"
linktitle: "MailMergeSettings"
second_title: "Aspose.Words per Java"
description: "Specifica tutte le informazioni di mail merge per un documento in Java."
type: docs
weight: 445
url: /it/java/com.aspose.words/mailmergesettings/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class MailMergeSettings implements Cloneable
```

Specifica tutte le informazioni di mail merge per un documento.

Per saperne di più, visita l'articolo di documentazione [ Mail Merge and Reporting ][Mail Merge and Reporting].

 **Remarks:** 

È possibile utilizzare questo oggetto per specificare una fonte dati di mail merge per un documento e queste informazioni (insieme ai campi dati disponibili) appariranno in Microsoft Word quando l'utente apre questo documento. In alternativa, è possibile utilizzare questo oggetto per interrogare le impostazioni di mail merge che l'utente ha specificato in Microsoft Word per questo documento.

Normalmente non è necessario creare oggetti di questa classe direttamente perché le impostazioni di mail merge di un documento sono sempre disponibili tramite la proprietà [Document.getMailMergeSettings()](../../com.aspose.words/document/\#getMailMergeSettings) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document/\#setMailMergeSettings-com.aspose.words.MailMergeSettings).

Per rilevare se questo documento è un documento principale di mail merge, controlla il valore della proprietà [getMainDocumentType()](../../com.aspose.words/mailmergesettings/\#getMainDocumentType) / [setMainDocumentType(int)](../../com.aspose.words/mailmergesettings/\#setMainDocumentType-int).

Per rimuovere le impostazioni di mail merge e le informazioni sulla fonte dati da un documento è possibile utilizzare il metodo [clear()](../../com.aspose.words/mailmergesettings/\#clear). Aspose.Words non scriverà le impostazioni di mail merge in un documento se la proprietà [getMainDocumentType()](../../com.aspose.words/mailmergesettings/\#getMainDocumentType) / [setMainDocumentType(int)](../../com.aspose.words/mailmergesettings/\#setMainDocumentType-int) è impostata su [MailMergeMainDocumentType.NOT_A_MERGE_DOCUMENT](../../com.aspose.words/mailmergemaindocumenttype/\#NOT-A-MERGE-DOCUMENT) o se la proprietà [getDataType()](../../com.aspose.words/mailmergesettings/\#getDataType) / [setDataType(int)](../../com.aspose.words/mailmergesettings/\#setDataType-int) è impostata su [MailMergeDataType.NONE](../../com.aspose.words/mailmergedatatype/\#NONE).

Il modo migliore per imparare a utilizzare le proprietà di questo oggetto è creare un documento con una fonte dati desiderata manualmente in Microsoft Word e poi aprire quel documento usando Aspose.Words ed esaminare le proprietà degli oggetti [Document.getMailMergeSettings()](../../com.aspose.words/document/\#getMailMergeSettings) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document/\#setMailMergeSettings-com.aspose.words.MailMergeSettings) e [getOdso()](../../com.aspose.words/mailmergesettings/\#getOdso) / [setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings/\#setOdso-com.aspose.words.Odso). Questo è un buon approccio da adottare se si desidera imparare a configurare programmaticamente una fonte dati, per esempio.

Aspose.Words conserva le informazioni di mail merge durante il caricamento, il salvataggio e la conversione dei documenti tra diversi formati, ma non utilizza queste informazioni quando esegue la propria stampa unione usando l'oggetto [MailMerge](../../com.aspose.words/mailmerge/).


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [clear()](#clear) | Cancella le impostazioni di mail merge in modo che, quando il documento viene salvato, non vengano salvate impostazioni di mail merge e il documento diventi un documento normale. |
| [deepClone()](#deepClone) | Restituisce una copia profonda di questo oggetto. |
| [getActiveRecord()](#getActiveRecord) | Specifica l'indice basato su 1 del record della fonte dati che deve essere visualizzato in Microsoft Word. |
| [getAddressFieldName()](#getAddressFieldName) | Specifica la colonna nella fonte dati che contiene gli indirizzi e‑mail. |
| [getCheckErrors()](#getCheckErrors) | Specifica il tipo di segnalazione degli errori che Microsoft Word deve eseguire durante una stampa unione. |
| [getConnectString()](#getConnectString) | Specifica la stringa di connessione utilizzata per collegarsi a una fonte dati esterna. |
| [getDataSource()](#getDataSource) | Specifica il percorso della fonte dati di mail merge. |
| [getDataType()](#getDataType) | Specifica il tipo della fonte dati di mail merge e il metodo di accesso ai dati. |
| [getDestination()](#getDestination) | Specifica come Microsoft Word produrrà i risultati di una stampa unione. |
| [getDoNotSupressBlankLines()](#getDoNotSupressBlankLines) | Specifica come un'applicazione che esegue la stampa unione deve gestire le righe vuote nei documenti uniti risultanti dalla stampa unione. |
| [getHeaderSource()](#getHeaderSource) | Specifica il percorso della sorgente dell'intestazione della stampa unione. |
| [getLinkToQuery()](#getLinkToQuery) | Non sono sicuro di questo. |
| [getMailAsAttachment()](#getMailAsAttachment) | Specifica che i documenti prodotti durante un'operazione di stampa unione devono essere inviati via e‑mail come allegato anziché nel corpo dell'e‑mail reale. |
| [getMailSubject()](#getMailSubject) | Specifica il testo che deve apparire nella riga dell'oggetto delle e‑mail o dei fax prodotti durante la stampa unione. |
| [getMainDocumentType()](#getMainDocumentType) | Specifica il tipo di documento principale della stampa unione. |
| [getOdso()](#getOdso) | Ottiene l'oggetto che specifica le impostazioni di Office Data Source Object (ODSO). |
| [getQuery()](#getQuery) | Contiene la stringa Structured Query Language che deve essere eseguita contro la fonte dati esterna specificata per restituire il set di record da importare nel documento quando viene eseguita l'operazione di stampa unione. |
| [getViewMergedData()](#getViewMergedData) | Specifica che Microsoft Word deve visualizzare i dati dalla fonte dati esterna specificata dove sono stati inseriti i campi di stampa (ad es. |
| [setActiveRecord(int value)](#setActiveRecord-int) | Specifica l'indice basato su 1 del record della fonte dati che deve essere visualizzato in Microsoft Word. |
| [setAddressFieldName(String value)](#setAddressFieldName-java.lang.String) | Specifica la colonna nella fonte dati che contiene gli indirizzi e‑mail. |
| [setCheckErrors(int value)](#setCheckErrors-int) | Specifica il tipo di segnalazione degli errori che Microsoft Word deve eseguire durante una stampa unione. |
| [setConnectString(String value)](#setConnectString-java.lang.String) | Specifica la stringa di connessione utilizzata per collegarsi a una fonte dati esterna. |
| [setDataSource(String value)](#setDataSource-java.lang.String) | Specifica il percorso della fonte dati di mail merge. |
| [setDataType(int value)](#setDataType-int) | Specifica il tipo della fonte dati di mail merge e il metodo di accesso ai dati. |
| [setDestination(int value)](#setDestination-int) | Specifica come Microsoft Word produrrà i risultati di una stampa unione. |
| [setDoNotSupressBlankLines(boolean value)](#setDoNotSupressBlankLines-boolean) | Specifica come un'applicazione che esegue la stampa unione deve gestire le righe vuote nei documenti uniti risultanti dalla stampa unione. |
| [setHeaderSource(String value)](#setHeaderSource-java.lang.String) | Specifica il percorso della sorgente dell'intestazione della stampa unione. |
| [setLinkToQuery(boolean value)](#setLinkToQuery-boolean) | Non sono sicuro di questo. |
| [setMailAsAttachment(boolean value)](#setMailAsAttachment-boolean) | Specifica che i documenti prodotti durante un'operazione di stampa unione devono essere inviati via e‑mail come allegato anziché nel corpo dell'e‑mail reale. |
| [setMailSubject(String value)](#setMailSubject-java.lang.String) | Specifica il testo che deve apparire nella riga dell'oggetto delle e‑mail o dei fax prodotti durante la stampa unione. |
| [setMainDocumentType(int value)](#setMainDocumentType-int) | Specifica il tipo di documento principale della stampa unione. |
| [setOdso(Odso value)](#setOdso-com.aspose.words.Odso) | Imposta l'oggetto che specifica le impostazioni di Office Data Source Object (ODSO). |
| [setQuery(String value)](#setQuery-java.lang.String) | Contiene la stringa Structured Query Language che deve essere eseguita contro la fonte dati esterna specificata per restituire il set di record da importare nel documento quando viene eseguita l'operazione di stampa unione. |
| [setViewMergedData(boolean value)](#setViewMergedData-boolean) | Specifica che Microsoft Word deve visualizzare i dati dalla fonte dati esterna specificata dove sono stati inseriti i campi di stampa (ad es. |
### clear() {#clear}
```
public void clear()
```


Cancella le impostazioni di mail merge in modo che, quando il documento viene salvato, non vengano salvate impostazioni di mail merge e il documento diventi un documento normale.

### deepClone() {#deepClone}
```
public MailMergeSettings deepClone()
```


Restituisce una copia profonda di questo oggetto.

**Returns:**
[MailMergeSettings](../../com.aspose.words/mailmergesettings/)
### getActiveRecord() {#getActiveRecord}
```
public int getActiveRecord()
```


Specifica l'indice basato su 1 del record della fonte dati che deve essere visualizzato in Microsoft Word. Il valore predefinito è 1.

**Returns:**
int - Il valore  int  corrispondente.
### getAddressFieldName() {#getAddressFieldName}
```
public String getAddressFieldName()
```


Specifica la colonna nella fonte dati che contiene gli indirizzi e‑mail. Il valore predefinito è una stringa vuota.

**Returns:**
java.lang.String - Il valore java.lang.String corrispondente.
### getCheckErrors() {#getCheckErrors}
```
public int getCheckErrors()
```


Specifica il tipo di segnalazione degli errori che Microsoft Word deve eseguire durante una stampa unione. Il valore predefinito è [MailMergeCheckErrors.DEFAULT](../../com.aspose.words/mailmergecheckerrors/\#DEFAULT).

**Returns:**
int - Il valore int corrispondente. Il valore restituito è una delle costanti [MailMergeCheckErrors](../../com.aspose.words/mailmergecheckerrors/).
### getConnectString() {#getConnectString}
```
public String getConnectString()
```


Specifica la stringa di connessione utilizzata per collegarsi a una fonte dati esterna. Il valore predefinito è una stringa vuota.

**Returns:**
java.lang.String - Il valore java.lang.String corrispondente.
### getDataSource() {#getDataSource}
```
public String getDataSource()
```


Specifica il percorso della fonte dati della stampa unione. Il valore predefinito è una stringa vuota.

**Returns:**
java.lang.String - Il valore java.lang.String corrispondente.
### getDataType() {#getDataType}
```
public int getDataType()
```


Specifica il tipo di fonte dati della stampa unione e il metodo di accesso ai dati. Il valore predefinito è [MailMergeDataType.DEFAULT](../../com.aspose.words/mailmergedatatype/\#DEFAULT).

**Returns:**
int - Il valore int corrispondente. Il valore restituito è una delle costanti [MailMergeDataType](../../com.aspose.words/mailmergedatatype/).
### getDestination() {#getDestination}
```
public int getDestination()
```


Specifica come Microsoft Word produrrà i risultati di una stampa unione. Il valore predefinito è [MailMergeDestination.DEFAULT](../../com.aspose.words/mailmergedestination/\#DEFAULT).

**Returns:**
int - Il valore int corrispondente. Il valore restituito è una delle costanti [MailMergeDestination](../../com.aspose.words/mailmergedestination/).
### getDoNotSupressBlankLines() {#getDoNotSupressBlankLines}
```
public boolean getDoNotSupressBlankLines()
```


Specifica come un'applicazione che esegue la stampa unione deve gestire le righe vuote nei documenti uniti risultanti dalla stampa unione. Il valore predefinito è false.

**Returns:**
boolean - Il valore booleano corrispondente.
### getHeaderSource() {#getHeaderSource}
```
public String getHeaderSource()
```


Specifica il percorso della sorgente dell'intestazione della stampa unione. Il valore predefinito è una stringa vuota.

**Returns:**
java.lang.String - Il valore java.lang.String corrispondente.
### getLinkToQuery() {#getLinkToQuery}
```
public boolean getLinkToQuery()
```


Non sono sicuro di questo. Il Microsoft Word Automation Reference suggerisce che questo specifichi che la query viene eseguita ogni volta che il documento è aperto in Microsoft Word. Ma la specifica OOXML suggerisce che questo specifichi che la query contiene un riferimento a un file di query esterno che contiene la query effettiva. Il valore predefinito è false.

**Returns:**
boolean - Il valore booleano corrispondente.
### getMailAsAttachment() {#getMailAsAttachment}
```
public boolean getMailAsAttachment()
```


Specifica che i documenti prodotti durante un'operazione di stampa unione devono essere inviati via e‑mail come allegato anziché nel corpo dell'e‑mail reale. Il valore predefinito è false.

**Returns:**
boolean - Il valore booleano corrispondente.
### getMailSubject() {#getMailSubject}
```
public String getMailSubject()
```


Specifica il testo che deve apparire nella riga dell'oggetto delle e-mail o dei fax prodotti durante l'unione di stampa. Il valore predefinito è una stringa vuota.

**Returns:**
java.lang.String - Il valore java.lang.String corrispondente.
### getMainDocumentType() {#getMainDocumentType}
```
public int getMainDocumentType()
```


Specifica il tipo di documento principale per l'unione di stampa. Il valore predefinito è [MailMergeMainDocumentType.DEFAULT](../../com.aspose.words/mailmergemaindocumenttype/\#DEFAULT).

 **Remarks:** 

Il documento principale è il documento che contiene informazioni identiche per ogni versione del documento unito.

**Returns:**
int - Il valore intero corrispondente. Il valore restituito è una delle costanti [MailMergeMainDocumentType](../../com.aspose.words/mailmergemaindocumenttype/).
### getOdso() {#getOdso}
```
public Odso getOdso()
```


Ottiene l'oggetto che specifica le impostazioni di Office Data Source Object (ODSO).

 **Remarks:** 

Questo oggetto non è mai null.

**Returns:**
[Odso](../../com.aspose.words/odso/) - The object that specifies the Office Data Source Object (ODSO) settings.
### getQuery() {#getQuery}
```
public String getQuery()
```


Contiene la stringa Structured Query Language che deve essere eseguita contro la fonte dati esterna specificata per restituire l'insieme di record da importare nel documento quando viene eseguita l'operazione di unione di stampa. Il valore predefinito è una stringa vuota.

**Returns:**
java.lang.String - Il valore java.lang.String corrispondente.
### getViewMergedData() {#getViewMergedData}
```
public boolean getViewMergedData()
```


Specifica che Microsoft Word deve visualizzare i dati dalla fonte dati esterna specificata dove sono stati inseriti i campi di unione (ad es. anteprima dei dati uniti). Il valore predefinito è false.

**Returns:**
boolean - Il valore booleano corrispondente.
### setActiveRecord(int value) {#setActiveRecord-int}
```
public void setActiveRecord(int value)
```


Specifica l'indice basato su 1 del record della fonte dati che deve essere visualizzato in Microsoft Word. Il valore predefinito è 1.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | Il valore  int  corrispondente. |

### setAddressFieldName(String value) {#setAddressFieldName-java.lang.String}
```
public void setAddressFieldName(String value)
```


Specifica la colonna nella fonte dati che contiene gli indirizzi e‑mail. Il valore predefinito è una stringa vuota.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il valore java.lang.String corrispondente. |

### setCheckErrors(int value) {#setCheckErrors-int}
```
public void setCheckErrors(int value)
```


Specifica il tipo di segnalazione degli errori che Microsoft Word deve eseguire durante una stampa unione. Il valore predefinito è [MailMergeCheckErrors.DEFAULT](../../com.aspose.words/mailmergecheckerrors/\#DEFAULT).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore intero corrispondente. Il valore deve essere una delle costanti [MailMergeCheckErrors](../../com.aspose.words/mailmergecheckerrors/). |

### setConnectString(String value) {#setConnectString-java.lang.String}
```
public void setConnectString(String value)
```


Specifica la stringa di connessione utilizzata per collegarsi a una fonte dati esterna. Il valore predefinito è una stringa vuota.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il valore java.lang.String corrispondente. |

### setDataSource(String value) {#setDataSource-java.lang.String}
```
public void setDataSource(String value)
```


Specifica il percorso della fonte dati della stampa unione. Il valore predefinito è una stringa vuota.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il valore java.lang.String corrispondente. |

### setDataType(int value) {#setDataType-int}
```
public void setDataType(int value)
```


Specifica il tipo di fonte dati della stampa unione e il metodo di accesso ai dati. Il valore predefinito è [MailMergeDataType.DEFAULT](../../com.aspose.words/mailmergedatatype/\#DEFAULT).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore intero corrispondente. Il valore deve essere una delle costanti [MailMergeDataType](../../com.aspose.words/mailmergedatatype/). |

### setDestination(int value) {#setDestination-int}
```
public void setDestination(int value)
```


Specifica come Microsoft Word produrrà i risultati di una stampa unione. Il valore predefinito è [MailMergeDestination.DEFAULT](../../com.aspose.words/mailmergedestination/\#DEFAULT).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore intero corrispondente. Il valore deve essere una delle costanti [MailMergeDestination](../../com.aspose.words/mailmergedestination/). |

### setDoNotSupressBlankLines(boolean value) {#setDoNotSupressBlankLines-boolean}
```
public void setDoNotSupressBlankLines(boolean value)
```


Specifica come un'applicazione che esegue la stampa unione deve gestire le righe vuote nei documenti uniti risultanti dalla stampa unione. Il valore predefinito è false.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setHeaderSource(String value) {#setHeaderSource-java.lang.String}
```
public void setHeaderSource(String value)
```


Specifica il percorso della sorgente dell'intestazione della stampa unione. Il valore predefinito è una stringa vuota.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il valore java.lang.String corrispondente. |

### setLinkToQuery(boolean value) {#setLinkToQuery-boolean}
```
public void setLinkToQuery(boolean value)
```


Non sono sicuro di questo. Il Microsoft Word Automation Reference suggerisce che questo specifichi che la query viene eseguita ogni volta che il documento è aperto in Microsoft Word. Ma la specifica OOXML suggerisce che questo specifichi che la query contiene un riferimento a un file di query esterno che contiene la query effettiva. Il valore predefinito è false.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setMailAsAttachment(boolean value) {#setMailAsAttachment-boolean}
```
public void setMailAsAttachment(boolean value)
```


Specifica che i documenti prodotti durante un'operazione di stampa unione devono essere inviati via e‑mail come allegato anziché nel corpo dell'e‑mail reale. Il valore predefinito è false.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setMailSubject(String value) {#setMailSubject-java.lang.String}
```
public void setMailSubject(String value)
```


Specifica il testo che deve apparire nella riga dell'oggetto delle e-mail o dei fax prodotti durante l'unione di stampa. Il valore predefinito è una stringa vuota.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il valore java.lang.String corrispondente. |

### setMainDocumentType(int value) {#setMainDocumentType-int}
```
public void setMainDocumentType(int value)
```


Specifica il tipo di documento principale per l'unione di stampa. Il valore predefinito è [MailMergeMainDocumentType.DEFAULT](../../com.aspose.words/mailmergemaindocumenttype/\#DEFAULT).

 **Remarks:** 

Il documento principale è il documento che contiene informazioni identiche per ogni versione del documento unito.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore intero corrispondente. Il valore deve essere una delle costanti [MailMergeMainDocumentType](../../com.aspose.words/mailmergemaindocumenttype/). |

### setOdso(Odso value) {#setOdso-com.aspose.words.Odso}
```
public void setOdso(Odso value)
```


Imposta l'oggetto che specifica le impostazioni di Office Data Source Object (ODSO).

 **Remarks:** 

Questo oggetto non è mai null.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | [Odso](../../com.aspose.words/odso/) | L'oggetto che specifica le impostazioni dell'Office Data Source Object (ODSO). |

### setQuery(String value) {#setQuery-java.lang.String}
```
public void setQuery(String value)
```


Contiene la stringa Structured Query Language che deve essere eseguita contro la fonte dati esterna specificata per restituire l'insieme di record da importare nel documento quando viene eseguita l'operazione di unione di stampa. Il valore predefinito è una stringa vuota.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il valore java.lang.String corrispondente. |

### setViewMergedData(boolean value) {#setViewMergedData-boolean}
```
public void setViewMergedData(boolean value)
```


Specifica che Microsoft Word deve visualizzare i dati dalla fonte dati esterna specificata dove sono stati inseriti i campi di unione (ad es. anteprima dei dati uniti). Il valore predefinito è false.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

