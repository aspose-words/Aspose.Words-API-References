---
title: "OdsoFieldMapData"
linktitle: "OdsoFieldMapData"
second_title: "Aspose.Words per Java"
description: "Specifica come una colonna nella fonte dati esterna deve essere mappata ai campi di unione predefiniti all'interno del documento in Java."
type: docs
weight: 489
url: /it/java/com.aspose.words/odsofieldmapdata/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class OdsoFieldMapData implements Cloneable
```

Specifica come una colonna nella fonte dati esterna deve essere mappata ai campi di stampa unione predefiniti nel documento.

Per saperne di più, visita l'articolo di documentazione [ Mail Merge and Reporting ][Mail Merge and Reporting].

 **Remarks:** 

Microsoft Word fornisce alcuni nomi di campi di unione predefiniti che consente di inserire in un documento come MERGEFIELD o di utilizzare nei campi ADDRESSBLOCK o GREETINGLINE. Le informazioni specificate in [OdsoFieldMapData](../../com.aspose.words/odsofieldmapdata/) consentono di mappare una colonna nella fonte dati esterna a un singolo campo di unione predefinito.


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [deepClone()](#deepClone) | Restituisce una copia profonda di questo oggetto. |
| [getColumn()](#getColumn) | Specifica l'indice basato su zero della colonna all'interno di una fonte dati esterna che deve essere mappata al nome locale di un campo MERGEFIELD specifico. |
| [getMappedName()](#getMappedName) | Specifica il nome del campo di unione predefinito che deve essere mappato al numero di colonna specificato dalla proprietà [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) in questa mappatura di campo. |
| [getName()](#getName) | Specifica il nome della colonna all'interno di una fonte dati esterna per la colonna il cui indice è specificato dalla proprietà [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int). |
| [getType()](#getType) | Specifica se un determinato campo di unione mail è stato mappato a una colonna nella fonte dati esterna specificata o meno. |
| [setColumn(int value)](#setColumn-int) | Specifica l'indice basato su zero della colonna all'interno di una fonte dati esterna che deve essere mappata al nome locale di un campo MERGEFIELD specifico. |
| [setMappedName(String value)](#setMappedName-java.lang.String) | Specifica il nome del campo di unione predefinito che deve essere mappato al numero di colonna specificato dalla proprietà [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) in questa mappatura di campo. |
| [setName(String value)](#setName-java.lang.String) | Specifica il nome della colonna all'interno di una fonte dati esterna per la colonna il cui indice è specificato dalla proprietà [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int). |
| [setType(int value)](#setType-int) | Specifica se un determinato campo di unione mail è stato mappato a una colonna nella fonte dati esterna specificata o meno. |
### deepClone() {#deepClone}
```
public OdsoFieldMapData deepClone()
```


Restituisce una copia profonda di questo oggetto.

**Returns:**
[OdsoFieldMapData](../../com.aspose.words/odsofieldmapdata/)
### getColumn() {#getColumn}
```
public int getColumn()
```


Specifica l'indice basato su zero della colonna all'interno di una fonte dati esterna che deve essere mappata al nome locale di un campo MERGEFIELD specifico. Il valore predefinito è 0.

**Returns:**
int - Il valore  int  corrispondente.
### getMappedName() {#getMappedName}
```
public String getMappedName()
```


Specifica il nome del campo di unione predefinito che deve essere mappato al numero di colonna specificato dalla proprietà [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) in questa mappatura di campo. Il valore predefinito è una stringa vuota.

**Returns:**
java.lang.String - Il valore java.lang.String corrispondente.
### getName() {#getName}
```
public String getName()
```


Specifica il nome della colonna all'interno di una fonte dati esterna per la colonna il cui indice è specificato dalla proprietà [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int). Il valore predefinito è una stringa vuota.

**Returns:**
java.lang.String - Il valore java.lang.String corrispondente.
### getType() {#getType}
```
public int getType()
```


Specifica se un determinato campo di unione mail è stato mappato a una colonna nella fonte dati esterna specificata o meno. Il valore predefinito è [OdsoFieldMappingType.DEFAULT](../../com.aspose.words/odsofieldmappingtype/\#DEFAULT).

**Returns:**
int - Il valore int corrispondente. Il valore restituito è uno dei costanti [OdsoFieldMappingType](../../com.aspose.words/odsofieldmappingtype/).
### setColumn(int value) {#setColumn-int}
```
public void setColumn(int value)
```


Specifica l'indice basato su zero della colonna all'interno di una fonte dati esterna che deve essere mappata al nome locale di un campo MERGEFIELD specifico. Il valore predefinito è 0.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | Il valore  int  corrispondente. |

### setMappedName(String value) {#setMappedName-java.lang.String}
```
public void setMappedName(String value)
```


Specifica il nome del campo di unione predefinito che deve essere mappato al numero di colonna specificato dalla proprietà [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) in questa mappatura di campo. Il valore predefinito è una stringa vuota.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il valore java.lang.String corrispondente. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Specifica il nome della colonna all'interno di una fonte dati esterna per la colonna il cui indice è specificato dalla proprietà [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int). Il valore predefinito è una stringa vuota.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il valore java.lang.String corrispondente. |

### setType(int value) {#setType-int}
```
public void setType(int value)
```


Specifica se un determinato campo di unione mail è stato mappato a una colonna nella fonte dati esterna specificata o meno. Il valore predefinito è [OdsoFieldMappingType.DEFAULT](../../com.aspose.words/odsofieldmappingtype/\#DEFAULT).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore int corrispondente. Il valore deve essere uno dei costanti [OdsoFieldMappingType](../../com.aspose.words/odsofieldmappingtype/). |

