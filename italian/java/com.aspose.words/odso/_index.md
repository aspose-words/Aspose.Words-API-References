---
title: "Odso"
linktitle: "Odso"
second_title: "Aspose.Words per Java"
description: "Specifica le impostazioni dell'Office Data Source Object ODSO per una fonte dati di stampa unione in Java."
type: docs
weight: 487
url: /it/java/com.aspose.words/odso/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Odso implements Cloneable
```

Specifica le impostazioni dell'Office Data Source Object (ODSO) per una fonte dati di stampa unione.

Per saperne di più, visita l'articolo di documentazione [ Mail Merge and Reporting ][Mail Merge and Reporting].

 **Remarks:** 

ODSO sembra essere il modo "nuovo" in cui le versioni più recenti di Microsoft Word preferiscono utilizzare quando si specificano determinati tipi di fonti dati per un documento di stampa unione. ODSO probabilmente è apparso per la prima volta in Microsoft Word 2000.

L'uso di ODSO è poco documentato e il modo migliore per imparare a utilizzare le proprietà di questo oggetto è creare un documento con una fonte dati desiderata manualmente in Microsoft Word e poi aprire quel documento usando Aspose.Words ed esaminare le proprietà degli oggetti [Document.getMailMergeSettings()](../../com.aspose.words/document/\#getMailMergeSettings) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document/\#setMailMergeSettings-com.aspose.words.MailMergeSettings) e [MailMergeSettings.getOdso()](../../com.aspose.words/mailmergesettings/\#getOdso) / [MailMergeSettings.setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings/\#setOdso-com.aspose.words.Odso) . Questo è un buon approccio da adottare se si desidera imparare a configurare programmaticamente una fonte dati, per esempio.

Normalmente non è necessario creare oggetti di questa classe direttamente perché le impostazioni ODSO sono sempre disponibili tramite la proprietà [MailMergeSettings.getOdso()](../../com.aspose.words/mailmergesettings/\#getOdso) / [MailMergeSettings.setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings/\#setOdso-com.aspose.words.Odso).


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [deepClone()](#deepClone) | Restituisce una copia profonda di questo oggetto. |
| [getColumnDelimiter()](#getColumnDelimiter) | Specifica il carattere che deve essere interpretato come delimitatore di colonna utilizzato per separare le colonne nelle fonti dati esterne. |
| [getDataSource()](#getDataSource) | Specifica la posizione della fonte dati esterna da collegare a un documento per eseguire l'unione di stampa. |
| [getDataSourceType()](#getDataSourceType) | Specifica il tipo della fonte dati esterna da collegare come parte delle informazioni di connessione ODSO per questa unione di stampa. |
| [getFieldMapDatas()](#getFieldMapDatas) | Ottiene una raccolta di oggetti che specificano come le colonne della fonte dati esterna vengano mappate ai nomi dei campi di unione predefiniti nel documento. |
| [getFirstRowContainsColumnNames()](#getFirstRowContainsColumnNames) | Specifica che un'applicazione host deve trattare la prima riga di dati nella fonte dati esterna specificata come riga di intestazione contenente i nomi di ciascuna colonna nella fonte dati. |
| [getRecipientDatas()](#getRecipientDatas) | Ottiene una raccolta di oggetti che specificano l'inclusione/esclusione di record individuali nell'unione di stampa. |
| [getTableName()](#getTableName) | Specifica il particolare insieme di dati a cui una fonte deve essere collegata all'interno di una fonte dati esterna. |
| [getUdlConnectString()](#getUdlConnectString) | Specifica la stringa di connessione Universal Data Link (UDL) utilizzata per collegarsi a una fonte dati esterna. |
| [setColumnDelimiter(char value)](#setColumnDelimiter-char) | Specifica il carattere che deve essere interpretato come delimitatore di colonna utilizzato per separare le colonne nelle fonti dati esterne. |
| [setDataSource(String value)](#setDataSource-java.lang.String) | Specifica la posizione della fonte dati esterna da collegare a un documento per eseguire l'unione di stampa. |
| [setDataSourceType(int value)](#setDataSourceType-int) | Specifica il tipo della fonte dati esterna da collegare come parte delle informazioni di connessione ODSO per questa unione di stampa. |
| [setFieldMapDatas(OdsoFieldMapDataCollection value)](#setFieldMapDatas-com.aspose.words.OdsoFieldMapDataCollection) | Imposta una raccolta di oggetti che specificano come le colonne della fonte dati esterna vengano mappate ai nomi dei campi di unione predefiniti nel documento. |
| [setFirstRowContainsColumnNames(boolean value)](#setFirstRowContainsColumnNames-boolean) | Specifica che un'applicazione host deve trattare la prima riga di dati nella fonte dati esterna specificata come riga di intestazione contenente i nomi di ciascuna colonna nella fonte dati. |
| [setRecipientDatas(OdsoRecipientDataCollection value)](#setRecipientDatas-com.aspose.words.OdsoRecipientDataCollection) | Imposta una raccolta di oggetti che specificano l'inclusione/esclusione di record individuali nell'unione di stampa. |
| [setTableName(String value)](#setTableName-java.lang.String) | Specifica il particolare insieme di dati a cui una fonte deve essere collegata all'interno di una fonte dati esterna. |
| [setUdlConnectString(String value)](#setUdlConnectString-java.lang.String) | Specifica la stringa di connessione Universal Data Link (UDL) utilizzata per collegarsi a una fonte dati esterna. |
### deepClone() {#deepClone}
```
public Odso deepClone()
```


Restituisce una copia profonda di questo oggetto.

**Returns:**
[Odso](../../com.aspose.words/odso/)
### getColumnDelimiter() {#getColumnDelimiter}
```
public char getColumnDelimiter()
```


Specifica il carattere che deve essere interpretato come delimitatore di colonna utilizzato per separare le colonne nelle fonti dati esterne. Il valore predefinito è 0, il che significa che non è definito alcun delimitatore di colonna.

 **Remarks:** 

RK non l'ho mai visto in uso.

**Returns:**
char - Il valore  char  corrispondente.
### getDataSource() {#getDataSource}
```
public String getDataSource()
```


Specifica la posizione della fonte dati esterna da collegare a un documento per eseguire l'unione di stampa. Il valore predefinito è una stringa vuota.

**Returns:**
java.lang.String - Il valore java.lang.String corrispondente.
### getDataSourceType() {#getDataSourceType}
```
public int getDataSourceType()
```


Specifica il tipo della fonte dati esterna da collegare come parte delle informazioni di connessione ODSO per questa unione di stampa. Il valore predefinito è [OdsoDataSourceType.DEFAULT](../../com.aspose.words/odsodatasourcetype/\#DEFAULT).

 **Remarks:** 

Questa impostazione è puramente un suggerimento del tipo di fonte dati utilizzato per questa unione di stampa.

**Returns:**
int - Il valore  int  corrispondente. Il valore restituito è una delle costanti [OdsoDataSourceType](../../com.aspose.words/odsodatasourcetype/).
### getFieldMapDatas() {#getFieldMapDatas}
```
public OdsoFieldMapDataCollection getFieldMapDatas()
```


Ottiene una raccolta di oggetti che specificano come le colonne della fonte dati esterna vengano mappate ai nomi dei campi di unione predefiniti nel documento. Questo oggetto non è mai  null .

**Returns:**
[OdsoFieldMapDataCollection](../../com.aspose.words/odsofieldmapdatacollection/) - A collection of objects that specify how columns from the external data source are mapped to the predefined merge field names in the document.
### getFirstRowContainsColumnNames() {#getFirstRowContainsColumnNames}
```
public boolean getFirstRowContainsColumnNames()
```


Specifica che un'applicazione host deve trattare la prima riga di dati nella fonte dati esterna specificata come riga di intestazione contenente i nomi di ciascuna colonna nella fonte dati. Il valore predefinito è  false .

 **Remarks:** 

RK non l'ho mai visto in uso.

**Returns:**
boolean - Il valore booleano corrispondente.
### getRecipientDatas() {#getRecipientDatas}
```
public OdsoRecipientDataCollection getRecipientDatas()
```


Ottiene una raccolta di oggetti che specificano l'inclusione/esclusione di record individuali nell'unione di stampa. Questo oggetto non è mai  null .

**Returns:**
[OdsoRecipientDataCollection](../../com.aspose.words/odsorecipientdatacollection/) - A collection of objects that specify inclusion/exclusion of individual records in the mail merge.
### getTableName() {#getTableName}
```
public String getTableName()
```


Specifica il particolare insieme di dati a cui una fonte deve essere collegata all'interno di una fonte dati esterna. Il valore predefinito è una stringa vuota.

**Returns:**
java.lang.String - Il valore java.lang.String corrispondente.
### getUdlConnectString() {#getUdlConnectString}
```
public String getUdlConnectString()
```


Specifica la stringa di connessione Universal Data Link (UDL) utilizzata per connettersi a una fonte dati esterna. Il valore predefinito è una stringa vuota.

**Returns:**
java.lang.String - Il valore java.lang.String corrispondente.
### setColumnDelimiter(char value) {#setColumnDelimiter-char}
```
public void setColumnDelimiter(char value)
```


Specifica il carattere che deve essere interpretato come delimitatore di colonna utilizzato per separare le colonne nelle fonti dati esterne. Il valore predefinito è 0, il che significa che non è definito alcun delimitatore di colonna.

 **Remarks:** 

RK non l'ho mai visto in uso.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | char | Il valore corrispondente  char  . |

### setDataSource(String value) {#setDataSource-java.lang.String}
```
public void setDataSource(String value)
```


Specifica la posizione della fonte dati esterna da collegare a un documento per eseguire l'unione di stampa. Il valore predefinito è una stringa vuota.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il valore java.lang.String corrispondente. |

### setDataSourceType(int value) {#setDataSourceType-int}
```
public void setDataSourceType(int value)
```


Specifica il tipo della fonte dati esterna da collegare come parte delle informazioni di connessione ODSO per questa unione di stampa. Il valore predefinito è [OdsoDataSourceType.DEFAULT](../../com.aspose.words/odsodatasourcetype/\#DEFAULT).

 **Remarks:** 

Questa impostazione è puramente un suggerimento del tipo di fonte dati utilizzato per questa unione di stampa.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore corrispondente  int  . Il valore deve essere uno dei costanti [OdsoDataSourceType](../../com.aspose.words/odsodatasourcetype/). |

### setFieldMapDatas(OdsoFieldMapDataCollection value) {#setFieldMapDatas-com.aspose.words.OdsoFieldMapDataCollection}
```
public void setFieldMapDatas(OdsoFieldMapDataCollection value)
```


Imposta una raccolta di oggetti che specificano come le colonne della fonte dati esterna vengono mappate ai nomi dei campi di unione predefiniti nel documento. Questo oggetto non è mai  null .

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | [OdsoFieldMapDataCollection](../../com.aspose.words/odsofieldmapdatacollection/) | Una raccolta di oggetti che specificano come le colonne della fonte dati esterna vengono mappate ai nomi dei campi di unione predefiniti nel documento. |

### setFirstRowContainsColumnNames(boolean value) {#setFirstRowContainsColumnNames-boolean}
```
public void setFirstRowContainsColumnNames(boolean value)
```


Specifica che un'applicazione host deve trattare la prima riga di dati nella fonte dati esterna specificata come riga di intestazione contenente i nomi di ciascuna colonna nella fonte dati. Il valore predefinito è  false .

 **Remarks:** 

RK non l'ho mai visto in uso.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setRecipientDatas(OdsoRecipientDataCollection value) {#setRecipientDatas-com.aspose.words.OdsoRecipientDataCollection}
```
public void setRecipientDatas(OdsoRecipientDataCollection value)
```


Imposta una raccolta di oggetti che specificano l'inclusione/esclusione di record individuali nell'unione di stampa. Questo oggetto non è mai  null .

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | [OdsoRecipientDataCollection](../../com.aspose.words/odsorecipientdatacollection/) | Una raccolta di oggetti che specificano l'inclusione/esclusione di record individuali nell'unione di stampa. |

### setTableName(String value) {#setTableName-java.lang.String}
```
public void setTableName(String value)
```


Specifica il particolare insieme di dati a cui una fonte deve essere collegata all'interno di una fonte dati esterna. Il valore predefinito è una stringa vuota.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il valore java.lang.String corrispondente. |

### setUdlConnectString(String value) {#setUdlConnectString-java.lang.String}
```
public void setUdlConnectString(String value)
```


Specifica la stringa di connessione Universal Data Link (UDL) utilizzata per connettersi a una fonte dati esterna. Il valore predefinito è una stringa vuota.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il valore java.lang.String corrispondente. |

