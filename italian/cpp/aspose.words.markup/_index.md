---
title: "Spazio dei nomi Aspose::Words::Markup"
linktitle: "Aspose::Words::Markup"
second_title: "Riferimento API Aspose.Words per C++"
description: "Spazio dei nomi Aspose::Words::Markup. Lo spazio dei nomi Aspose.Words.Markup contiene classi che rappresentano semantiche definite dal cliente in un documento: smart tag, XML personalizzato e tag di documento strutturati (controlli di contenuto) in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words.markup/
---

Il namespace **Aspose.Words.Markup** contiene classi che rappresentano semantiche definite dal cliente in un documento: smart tag, XML personalizzato e tag di documento strutturato (controlli di contenuto).

## Classi

| Classe | Descrizione |
| --- | --- |
| [CustomPart](./custompart/) | Rappresenta una parte personalizzata (contenuto arbitrario) che non è definita dallo standard ISO/IEC 29500. Per saperne di più, visita l'articolo di documentazione [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [CustomPartCollection](./custompartcollection/) | Rappresenta una raccolta di oggetti [CustomPart](./custompart/). Per saperne di più, visita l'articolo di documentazione [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [CustomXmlPart](./customxmlpart/) | Rappresenta una parte di archiviazione dati XML personalizzata (dati XML personalizzati all'interno di un pacchetto). Per saperne di più, visita l'articolo di documentazione [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [CustomXmlPartCollection](./customxmlpartcollection/) | Rappresenta una raccolta di parti XML personalizzate. Gli elementi sono oggetti [CustomXmlPart](./customxmlpart/). Per saperne di più, visita l'articolo di documentazione [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [CustomXmlProperty](./customxmlproperty/) | Rappresenta un singolo attributo XML personalizzato o una proprietà di smart tag. Per saperne di più, visita l'articolo di documentazione [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [CustomXmlPropertyCollection](./customxmlpropertycollection/) | Rappresenta una raccolta di attributi XML personalizzati o proprietà di smart tag. Per saperne di più, visita l'articolo di documentazione [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [CustomXmlSchemaCollection](./customxmlschemacollection/) | Una raccolta di stringhe che rappresentano gli schemi XML associati a una parte XML personalizzata. Per saperne di più, visita l'articolo di documentazione [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [SdtListItem](./sdtlistitem/) | Questo elemento specifica un singolo elemento di elenco all'interno di un [ComboBox](./sdttype/) o [DropDownList](./sdttype/) tag di documento strutturato padre. Per saperne di più, visita l'articolo di documentazione [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [SdtListItemCollection](./sdtlistitemcollection/) | Fornisce l'accesso agli elementi [SdtListItem](./sdtlistitem/) di un tag di documento strutturato. Per saperne di più, visita l'articolo di documentazione [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [SmartTag](./smarttag/) | Questo elemento specifica la presenza di uno smart tag attorno a una o più strutture in linea (run, immagini, campi, ecc.) all'interno di un paragrafo. Per saperne di più, visita l'articolo di documentazione [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [StructuredDocumentTag](./structureddocumenttag/) | Rappresenta un tag di documento strutturato (SDT o controllo del contenuto) in un documento. Per saperne di più, visita l'articolo di documentazione [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [StructuredDocumentTagCollection](./structureddocumenttagcollection/) | Una raccolta di istanze [IStructuredDocumentTag](./istructureddocumenttag/) che rappresentano i tag di documento strutturato nell'intervallo specificato. Per saperne di più, visita l'articolo di documentazione [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [StructuredDocumentTagRangeEnd](./structureddocumenttagrangeend/) | Rappresenta la fine di un tag di documento strutturato **ranged** che accetta contenuti multi-sezione. Vedi anche il nodo [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/). Per saperne di più, visita l'articolo di documentazione [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/) | Rappresenta l'inizio di un tag di documento strutturato **ranged** che accetta contenuti multi-sezione. Vedi anche il nodo [StructuredDocumentTagRangeEnd](./structureddocumenttagrangeend/). Per saperne di più, visita l'articolo di documentazione [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [XmlMapping](./xmlmapping/) | Specifica le informazioni utilizzate per stabilire una mappatura tra il tag di documento strutturato padre e un elemento XML memorizzato all'interno di una parte di dati XML personalizzata nel documento. Per saperne di più, visita l'articolo di documentazione [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
## Interfacce

| Interfaccia | Descrizione |
| --- | --- |
| [IStructuredDocumentTag](./istructureddocumenttag/) | Interfaccia per definire dati comuni per [StructuredDocumentTag](./structureddocumenttag/) e [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/). |
## Enums

| Enum | Descrizione |
| --- | --- |
| [MarkupLevel](./markuplevel/) | Specifica il livello nell'albero del documento in cui può comparire un determinato [StructuredDocumentTag](./structureddocumenttag/). |
| [SdtAppearance](./sdtappearance/) | Specifica l'aspetto di un tag di documento strutturato. |
| [SdtCalendarType](./sdtcalendartype/) | Specifica i possibili tipi di calendari che possono essere usati per specificare [CalendarType](./structureddocumenttag/get_calendartype/) in un documento Office Open XML. |
| [SdtDateStorageFormat](./sdtdatestorageformat/) | Specifica come la data per un SDT di tipo data viene memorizzata/recuperata quando l'SDT è collegato a un nodo XML nell'archivio dati del documento. |
| [SdtType](./sdttype/) | Specifica il tipo di nodo di un tag di documento strutturato (SDT). |
