---
title: "XmlDataLoadOptions"
linktitle: "XmlDataLoadOptions"
second_title: "Aspose.Words per Java"
description: "Rappresenta le opzioni per il caricamento di dati XML in Java."
type: docs
weight: 745
url: /it/java/com.aspose.words/xmldataloadoptions/
---

**Inheritance:**
java.lang.Object
```
public class XmlDataLoadOptions
```

Rappresenta le opzioni per il caricamento dei dati XML.

Per saperne di più, visita l'articolo di documentazione [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

Un'istanza di questa classe può essere passata ai costruttori di [XmlDataSource](../../com.aspose.words/xmldatasource/).


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [XmlDataLoadOptions()](#XmlDataLoadOptions) | Inizializza una nuova istanza di questa classe con le opzioni predefinite. |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getAlwaysGenerateRootObject()](#getAlwaysGenerateRootObject) | Ottiene un flag che indica se una fonte dati generata conterrà sempre un oggetto per un elemento radice XML. |
| [setAlwaysGenerateRootObject(boolean value)](#setAlwaysGenerateRootObject-boolean) | Imposta un flag che indica se una fonte dati generata conterrà sempre un oggetto per un elemento radice XML. |
### XmlDataLoadOptions() {#XmlDataLoadOptions}
```
public XmlDataLoadOptions()
```


Inizializza una nuova istanza di questa classe con le opzioni predefinite.

### getAlwaysGenerateRootObject() {#getAlwaysGenerateRootObject}
```
public boolean getAlwaysGenerateRootObject()
```


Ottiene un flag che indica se una fonte dati generata conterrà sempre un oggetto per un elemento radice XML. Se un elemento radice XML non ha attributi e tutti i suoi elementi figlio hanno gli stessi nomi, tale oggetto non viene creato per impostazione predefinita.

 **Remarks:** 

Il valore predefinito è  false .

**Returns:**
boolean - Un flag che indica se una fonte dati generata conterrà sempre un oggetto per un elemento radice XML.
### setAlwaysGenerateRootObject(boolean value) {#setAlwaysGenerateRootObject-boolean}
```
public void setAlwaysGenerateRootObject(boolean value)
```


Imposta un flag che indica se una fonte dati generata conterrà sempre un oggetto per un elemento radice XML. Se un elemento radice XML non ha attributi e tutti i suoi elementi figlio hanno gli stessi nomi, tale oggetto non viene creato per impostazione predefinita.

 **Remarks:** 

Il valore predefinito è  false .

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Un flag che indica se una fonte dati generata conterrà sempre un oggetto per un elemento radice XML. |

