---
title: Aspose.Words.Markup
linktitle: Aspose.Words.Markup
articleTitle: Aspose.Words.Markup
second_title: Aspose.Words per .NET
description: Scopri lo spazio dei nomi Aspose.Words.Markup, con classi personalizzabili per smart tag, XML e controlli dei contenuti per migliorare la gestione dei documenti.
type: docs
weight: 180
url: /it/net/aspose.words.markup/
---
IL**Aspose.Words.Markup** Lo spazio dei nomi contiene classi che rappresentano la semantica definita dal cliente in un documento: tag intelligenti, XML personalizzati e tag di documenti strutturati (controlli del contenuto).

## Classi

| Classe | Descrizione |
| --- | --- |
| [CustomPart](./custompart/) | Rappresenta una parte personalizzata (contenuto arbitrario), non definita dallo standard ISO/IEC 29500. |
| [CustomPartCollection](./custompartcollection/) | Rappresenta una raccolta di[`CustomPart`](../aspose.words.markup/custompart/) oggetti. |
| [CustomXmlPart](./customxmlpart/) | Rappresenta una parte di archiviazione dati XML personalizzata (dati XML personalizzati all'interno di un pacchetto). |
| [CustomXmlPartCollection](./customxmlpartcollection/) | Rappresenta una raccolta di parti XML personalizzate. Gli elementi sono[`CustomXmlPart`](../aspose.words.markup/customxmlpart/) oggetti. |
| [CustomXmlProperty](./customxmlproperty/) | Rappresenta un singolo attributo XML personalizzato o una proprietà di tag intelligente. |
| [CustomXmlPropertyCollection](./customxmlpropertycollection/) | Rappresenta una raccolta di attributi XML personalizzati o proprietà di tag intelligenti. |
| [CustomXmlSchemaCollection](./customxmlschemacollection/) | Una raccolta di stringhe che rappresentano schemi XML associati a una parte XML personalizzata. |
| [SdtListItem](./sdtlistitem/) | Questo elemento specifica un singolo elemento di elenco all'interno di un elemento padreComboBox ODropDownList tag documento strutturato. |
| [SdtListItemCollection](./sdtlistitemcollection/) | Fornisce l'accesso a[`SdtListItem`](../aspose.words.markup/sdtlistitem/) elementi di un tag di documento strutturato. |
| [SmartTag](./smarttag/) | Questo elemento specifica la presenza di uno smart tag attorno a una o più strutture inline (esercitazioni, immagini, campi, ecc.) all'interno di un paragrafo. |
| [StructuredDocumentTag](./structureddocumenttag/) | Rappresenta un tag di documento strutturato (SDT o controllo del contenuto) in un documento. |
| [StructuredDocumentTagCollection](./structureddocumenttagcollection/) | Una raccolta di[`IStructuredDocumentTag`](../aspose.words.markup/istructureddocumenttag/) istanze che rappresentano i tag del documento strutturato nell'intervallo specificato. |
| [StructuredDocumentTagRangeEnd](./structureddocumenttagrangeend/) | Rappresenta la fine di**a distanza** tag di documento strutturato che accetta contenuti multi-sezione. Vedi anche[`StructuredDocumentTagRangeStart`](../aspose.words.markup/structureddocumenttagrangestart/) nodo. |
| [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/) | Rappresenta un inizio di**a distanza** tag di documento strutturato che accetta contenuti multi-sezione. Vedi anche[`StructuredDocumentTagRangeEnd`](../aspose.words.markup/structureddocumenttagrangeend/) . |
| [XmlMapping](./xmlmapping/) | Specifica le informazioni utilizzate per stabilire una mappatura tra il tag del documento strutturato parent e un elemento XML memorizzato all'interno di una parte di dati XML personalizzata nel documento. |
## Interfacce

| Interfaccia | Descrizione |
| --- | --- |
| [IStructuredDocumentTag](./istructureddocumenttag/) | Interfaccia per definire un dato comune per[`StructuredDocumentTag`](../aspose.words.markup/structureddocumenttag/) E[`StructuredDocumentTagRangeStart`](../aspose.words.markup/structureddocumenttagrangestart/) . |
## Enumerazione

| Enumerazione | Descrizione |
| --- | --- |
| [MarkupLevel](./markuplevel/) | Specifica il livello nell'albero del documento in cui si trova un particolare[`StructuredDocumentTag`](../aspose.words.markup/structureddocumenttag/) può verificarsi. |
| [SdtAppearance](./sdtappearance/) | Specifica l'aspetto di un tag di documento strutturato. |
| [SdtCalendarType](./sdtcalendartype/) | Specifica i possibili tipi di calendari che possono essere utilizzati per specificare[`CalendarType`](../aspose.words.markup/structureddocumenttag/calendartype/) in un documento Office Open XML. |
| [SdtDateStorageFormat](./sdtdatestorageformat/) | Specifica come la data per un SDT di data viene archiviata/recuperata quando l'SDT è associato a un nodo XML nell'archivio dati del documento. |
| [SdtType](./sdttype/) | Specifica il tipo di nodo tag di documento strutturato (SDT). |
