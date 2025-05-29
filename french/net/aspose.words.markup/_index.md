---
title: Aspose.Words.Markup
linktitle: Aspose.Words.Markup
articleTitle: Aspose.Words.Markup
second_title: Aspose.Words pour .NET
description: Découvrez l'espace de noms Aspose.Words.Markup, comprenant des classes personnalisables pour les balises intelligentes, XML et les contrôles de contenu pour améliorer la gestion de vos documents.
type: docs
weight: 180
url: /fr/net/aspose.words.markup/
---
Le**Aspose.Words.Markup** L'espace de noms contient des classes qui représentent la sémantique définie par le client dans un document : balises intelligentes, XML personnalisé et balises de document structurées (contrôles de contenu).

## Des classes

| Classer | La description |
| --- | --- |
| [CustomPart](./custompart/) | Représente une partie personnalisée (contenu arbitraire), qui n'est pas définie par la norme ISO/IEC 29500. |
| [CustomPartCollection](./custompartcollection/) | Représente une collection de[`CustomPart`](../aspose.words.markup/custompart/) objets. |
| [CustomXmlPart](./customxmlpart/) | Représente une partie de stockage de données XML personnalisée (données XML personnalisées dans un package). |
| [CustomXmlPartCollection](./customxmlpartcollection/) | représente une collection de composants XML personnalisés. Les éléments sont[`CustomXmlPart`](../aspose.words.markup/customxmlpart/) objets. |
| [CustomXmlProperty](./customxmlproperty/) | Représente un seul attribut XML personnalisé ou une propriété de balise intelligente. |
| [CustomXmlPropertyCollection](./customxmlpropertycollection/) | Représente une collection d'attributs XML personnalisés ou de propriétés de balises intelligentes. |
| [CustomXmlSchemaCollection](./customxmlschemacollection/) | Une collection de chaînes qui représentent des schémas XML associés à une partie XML personnalisée. |
| [SdtListItem](./sdtlistitem/) | Cet élément spécifie un seul élément de liste dans un parentComboBox ouDropDownList balise de document structuré. |
| [SdtListItemCollection](./sdtlistitemcollection/) | Donne accès à[`SdtListItem`](../aspose.words.markup/sdtlistitem/) éléments d'une balise de document structuré. |
| [SmartTag](./smarttag/) | Cet élément spécifie la présence d'une balise intelligente autour d'une ou plusieurs structures en ligne (exécutions, images, champs, etc.) dans un paragraphe. |
| [StructuredDocumentTag](./structureddocumenttag/) | Représente une balise de document structurée (SDT ou contrôle de contenu) dans un document. |
| [StructuredDocumentTagCollection](./structureddocumenttagcollection/) | Une collection de[`IStructuredDocumentTag`](../aspose.words.markup/istructureddocumenttag/) instances qui représentent les balises de document structurées dans la plage spécifiée. |
| [StructuredDocumentTagRangeEnd](./structureddocumenttagrangeend/) | Représente une fin de**à distance** balise de document structurée qui accepte un contenu multi-sections. Voir aussi[`StructuredDocumentTagRangeStart`](../aspose.words.markup/structureddocumenttagrangestart/) nœud. |
| [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/) | Représente un début de**à distance** balise de document structurée qui accepte un contenu multi-sections. Voir aussi[`StructuredDocumentTagRangeEnd`](../aspose.words.markup/structureddocumenttagrangeend/) . |
| [XmlMapping](./xmlmapping/) | Spécifie les informations utilisées pour établir un mappage entre la balise de document structurée parent et un élément XML stocké dans une partie de données XML personnalisée du document. |
## Interfaces

| Interface | La description |
| --- | --- |
| [IStructuredDocumentTag](./istructureddocumenttag/) | Interface pour définir une donnée commune pour[`StructuredDocumentTag`](../aspose.words.markup/structureddocumenttag/) et[`StructuredDocumentTagRangeStart`](../aspose.words.markup/structureddocumenttagrangestart/) . |
## Énumération

| Énumération | La description |
| --- | --- |
| [MarkupLevel](./markuplevel/) | Spécifie le niveau dans l'arborescence du document où un[`StructuredDocumentTag`](../aspose.words.markup/structureddocumenttag/) peut se produire. |
| [SdtAppearance](./sdtappearance/) | Spécifie l'apparence d'une balise de document structuré. |
| [SdtCalendarType](./sdtcalendartype/) | Spécifie les types possibles de calendriers qui peuvent être utilisés pour spécifier[`CalendarType`](../aspose.words.markup/structureddocumenttag/calendartype/) dans un document Office Open XML. |
| [SdtDateStorageFormat](./sdtdatestorageformat/) | Spécifie comment la date d'un SDT de date est stockée/récupérée lorsque le SDT est lié à un nœud XML dans le magasin de données du document. |
| [SdtType](./sdttype/) | Spécifie le type d'un nœud de balise de document structuré (SDT). |
