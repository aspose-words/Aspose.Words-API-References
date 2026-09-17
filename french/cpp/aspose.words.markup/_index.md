---
title: "Espace de noms Aspose::Words::Markup"
linktitle: "Aspose::Words::Markup"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Espace de noms Aspose::Words::Markup. L'espace de noms Aspose.Words.Markup contient des classes qui représentent des sémantiques définies par le client dans un document : balises intelligentes, XML personnalisé et balises de document structurées (contrôles de contenu) en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words.markup/
---

L'espace de noms **Aspose.Words.Markup** contient des classes qui représentent la sémantique définie par le client dans un document : les balises intelligentes, le XML personnalisé et les balises de document structuré (contrôles de contenu).

## Classes

| Classe | Description |
| --- | --- |
| [CustomPart](./custompart/) | Représente une partie personnalisée (contenu arbitraire) qui n'est pas définie par la norme ISO/IEC 29500. Pour en savoir plus, consultez l'article de documentation [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [CustomPartCollection](./custompartcollection/) | Représente une collection d'objets [CustomPart](./custompart/). Pour en savoir plus, consultez l'article de documentation [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [CustomXmlPart](./customxmlpart/) | Représente une partie de stockage de données XML personnalisées (données XML personnalisées dans un package). Pour en savoir plus, consultez l'article de documentation [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [CustomXmlPartCollection](./customxmlpartcollection/) | Représente une collection de parties XML personnalisées. Les éléments sont des objets [CustomXmlPart](./customxmlpart/). Pour en savoir plus, consultez l'article de documentation [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [CustomXmlProperty](./customxmlproperty/) | Représente un attribut XML personnalisé unique ou une propriété de smart tag. Pour en savoir plus, consultez l'article de documentation [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [CustomXmlPropertyCollection](./customxmlpropertycollection/) | Représente une collection d'attributs XML personnalisés ou de propriétés de smart tag. Pour en savoir plus, consultez l'article de documentation [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [CustomXmlSchemaCollection](./customxmlschemacollection/) | Une collection de chaînes qui représentent des schémas XML associés à une partie XML personnalisée. Pour en savoir plus, consultez l'article de documentation [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [SdtListItem](./sdtlistitem/) | Cet élément spécifie un seul élément de liste au sein d'un [ComboBox](./sdttype/) ou [DropDownList](./sdttype/) balise de document structuré parent. Pour en savoir plus, consultez l'article de documentation [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [SdtListItemCollection](./sdtlistitemcollection/) | Fournit l'accès aux éléments [SdtListItem](./sdtlistitem/) d'une balise de document structuré. Pour en savoir plus, consultez l'article de documentation [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [SmartTag](./smarttag/) | Cet élément spécifie la présence d'un smart tag autour d'une ou plusieurs structures en ligne (exécutions, images, champs, etc.) dans un paragraphe. Pour en savoir plus, consultez l'article de documentation [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [StructuredDocumentTag](./structureddocumenttag/) | Représente une balise de document structuré (SDT ou contrôle de contenu) dans un document. Pour en savoir plus, consultez l'article de documentation [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [StructuredDocumentTagCollection](./structureddocumenttagcollection/) | Une collection d'instances [IStructuredDocumentTag](./istructureddocumenttag/) qui représentent les balises de document structuré dans la plage spécifiée. Pour en savoir plus, consultez l'article de documentation [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [StructuredDocumentTagRangeEnd](./structureddocumenttagrangeend/) | Représente la fin d'une balise de document structuré **ranged** qui accepte du contenu multi-sections. Voir également le nœud [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/). Pour en savoir plus, consultez l'article de documentation [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/) | Représente le début d'une balise de document structuré **ranged** qui accepte du contenu multi-sections. Voir également le nœud [StructuredDocumentTagRangeEnd](./structureddocumenttagrangeend/). Pour en savoir plus, consultez l'article de documentation [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
| [XmlMapping](./xmlmapping/) | Spécifie les informations utilisées pour établir une correspondance entre la balise de document structuré parent et un élément XML stocké dans une partie de données XML personnalisée du document. Pour en savoir plus, consultez l'article de documentation [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/). |
## Interfaces

| Interface | Description |
| --- | --- |
| [IStructuredDocumentTag](./istructureddocumenttag/) | Interface pour définir des données communes pour [StructuredDocumentTag](./structureddocumenttag/) et [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/). |
## Enums

| Enum | Description |
| --- | --- |
| [MarkupLevel](./markuplevel/) | Spécifie le niveau dans l'arborescence du document où un [StructuredDocumentTag](./structureddocumenttag/) particulier peut apparaître. |
| [SdtAppearance](./sdtappearance/) | Spécifie l'apparence d'une balise de document structuré. |
| [SdtCalendarType](./sdtcalendartype/) | Spécifie les types de calendriers possibles qui peuvent être utilisés pour spécifier [CalendarType](./structureddocumenttag/get_calendartype/) dans un document Office Open XML. |
| [SdtDateStorageFormat](./sdtdatestorageformat/) | Spécifie comment la date d'un SDT de type date est stockée/récupérée lorsque le SDT est lié à un nœud XML dans le magasin de données du document. |
| [SdtType](./sdttype/) | Spécifie le type d'un nœud de balise de document structuré (SDT). |
