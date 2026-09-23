---
title: "MailMergeSettings"
linktitle: "MailMergeSettings"
second_title: "Aspose.Words pour Java"
description: "Spécifie toutes les informations de mail merge pour un document en Java."
type: docs
weight: 445
url: /fr/java/com.aspose.words/mailmergesettings/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class MailMergeSettings implements Cloneable
```

Spécifie toutes les informations de fusion de courrier pour un document.

Pour en savoir plus, consultez l’article de documentation [ Mail Merge and Reporting ][Mail Merge and Reporting].

 **Remarks:** 

Vous pouvez utiliser cet objet pour spécifier une source de données de mail merge pour un document et ces informations (ainsi que les champs de données disponibles) apparaîtront dans Microsoft Word lorsque l'utilisateur ouvrira ce document. Vous pouvez également utiliser cet objet pour interroger les paramètres de mail merge que l'utilisateur a spécifiés dans Microsoft Word pour ce document.

Vous n'avez généralement pas besoin de créer des objets de cette classe directement car les paramètres de mail merge d'un document sont toujours accessibles via la propriété [Document.getMailMergeSettings()](../../com.aspose.words/document/\#getMailMergeSettings) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document/\#setMailMergeSettings-com.aspose.words.MailMergeSettings).

Pour détecter si ce document est le document principal de mail merge, vérifiez la valeur de la propriété [getMainDocumentType()](../../com.aspose.words/mailmergesettings/\#getMainDocumentType) / [setMainDocumentType(int)](../../com.aspose.words/mailmergesettings/\#setMainDocumentType-int).

Pour supprimer les paramètres de mail merge et les informations de source de données d'un document, vous pouvez utiliser la méthode [clear()](../../com.aspose.words/mailmergesettings/\#clear). Aspose.Words n'écrira pas les paramètres de mail merge dans un document si la propriété [getMainDocumentType()](../../com.aspose.words/mailmergesettings/\#getMainDocumentType) / [setMainDocumentType(int)](../../com.aspose.words/mailmergesettings/\#setMainDocumentType-int) est définie sur [MailMergeMainDocumentType.NOT_A_MERGE_DOCUMENT](../../com.aspose.words/mailmergemaindocumenttype/\#NOT-A-MERGE-DOCUMENT) ou si la propriété [getDataType()](../../com.aspose.words/mailmergesettings/\#getDataType) / [setDataType(int)](../../com.aspose.words/mailmergesettings/\#setDataType-int) est définie sur [MailMergeDataType.NONE](../../com.aspose.words/mailmergedatatype/\#NONE).

La meilleure façon d'apprendre à utiliser les propriétés de cet objet est de créer manuellement un document avec la source de données souhaitée dans Microsoft Word, puis d'ouvrir ce document avec Aspose.Words et d'examiner les propriétés des objets [Document.getMailMergeSettings()](../../com.aspose.words/document/\#getMailMergeSettings) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document/\#setMailMergeSettings-com.aspose.words.MailMergeSettings) et [getOdso()](../../com.aspose.words/mailmergesettings/\#getOdso) / [setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings/\#setOdso-com.aspose.words.Odso). C'est une bonne approche si vous souhaitez apprendre à configurer une source de données de façon programmatique, par exemple.

Aspose.Words conserve les informations de mail merge lors du chargement, de l'enregistrement et de la conversion de documents entre différents formats, mais n'utilise pas ces informations lors de l'exécution de son propre mail merge à l'aide de l'objet [MailMerge](../../com.aspose.words/mailmerge/).


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Méthodes

| Méthode | Description |
| --- | --- |
| [clear()](#clear) | Efface les paramètres de mail merge de manière à ce que, lors de l'enregistrement du document, aucun paramètre de mail merge ne soit sauvegardé et le document devienne un document normal. |
| [deepClone()](#deepClone) | Renvoie un clone profond de cet objet. |
| [getActiveRecord()](#getActiveRecord) | Spécifie l'index basé sur 1 de l'enregistrement de la source de données qui doit être affiché dans Microsoft Word. |
| [getAddressFieldName()](#getAddressFieldName) | Spécifie la colonne de la source de données contenant les adresses e-mail. |
| [getCheckErrors()](#getCheckErrors) | Spécifie le type de rapport d'erreur qui sera effectué par Microsoft Word lors d'un mail merge. |
| [getConnectString()](#getConnectString) | Spécifie la chaîne de connexion utilisée pour se connecter à une source de données externe. |
| [getDataSource()](#getDataSource) | Spécifie le chemin vers la source de données de mail-merge. |
| [getDataType()](#getDataType) | Spécifie le type de la source de données de mail-merge et la méthode d'accès aux données. |
| [getDestination()](#getDestination) | Spécifie comment Microsoft Word affichera les résultats d'une fusion de courrier. |
| [getDoNotSupressBlankLines()](#getDoNotSupressBlankLines) | Spécifie comment une application effectuant la fusion de courrier doit gérer les lignes vides dans les documents fusionnés résultant de la fusion de courrier. |
| [getHeaderSource()](#getHeaderSource) | Spécifie le chemin vers la source d'en-tête de fusion de courrier. |
| [getLinkToQuery()](#getLinkToQuery) | Pas sûr de celui-ci. |
| [getMailAsAttachment()](#getMailAsAttachment) | Spécifie que les documents produits lors d'une opération de fusion de courrier doivent être envoyés par e‑mail en tant que pièce jointe plutôt que dans le corps du courriel réel. |
| [getMailSubject()](#getMailSubject) | Spécifie le texte qui doit apparaître dans la ligne d'objet des e‑mails ou fax produits lors de la fusion de courrier. |
| [getMainDocumentType()](#getMainDocumentType) | Spécifie le type de document principal de la fusion de courrier. |
| [getOdso()](#getOdso) | Obtient l'objet qui spécifie les paramètres de l'Office Data Source Object (ODSO). |
| [getQuery()](#getQuery) | Contient la chaîne Structured Query Language qui doit être exécutée contre la source de données externe spécifiée afin de renvoyer l'ensemble des enregistrements qui seront importés dans le document lors de l'exécution de la fusion de courrier. |
| [getViewMergedData()](#getViewMergedData) | Spécifie que Microsoft Word doit afficher les données de la source de données externe spécifiée là où des champs de fusion ont été insérés (par ex. |
| [setActiveRecord(int value)](#setActiveRecord-int) | Spécifie l'index basé sur 1 de l'enregistrement de la source de données qui doit être affiché dans Microsoft Word. |
| [setAddressFieldName(String value)](#setAddressFieldName-java.lang.String) | Spécifie la colonne de la source de données contenant les adresses e-mail. |
| [setCheckErrors(int value)](#setCheckErrors-int) | Spécifie le type de rapport d'erreur qui sera effectué par Microsoft Word lors d'un mail merge. |
| [setConnectString(String value)](#setConnectString-java.lang.String) | Spécifie la chaîne de connexion utilisée pour se connecter à une source de données externe. |
| [setDataSource(String value)](#setDataSource-java.lang.String) | Spécifie le chemin vers la source de données de mail-merge. |
| [setDataType(int value)](#setDataType-int) | Spécifie le type de la source de données de mail-merge et la méthode d'accès aux données. |
| [setDestination(int value)](#setDestination-int) | Spécifie comment Microsoft Word affichera les résultats d'une fusion de courrier. |
| [setDoNotSupressBlankLines(boolean value)](#setDoNotSupressBlankLines-boolean) | Spécifie comment une application effectuant la fusion de courrier doit gérer les lignes vides dans les documents fusionnés résultant de la fusion de courrier. |
| [setHeaderSource(String value)](#setHeaderSource-java.lang.String) | Spécifie le chemin vers la source d'en-tête de fusion de courrier. |
| [setLinkToQuery(boolean value)](#setLinkToQuery-boolean) | Pas sûr de celui-ci. |
| [setMailAsAttachment(boolean value)](#setMailAsAttachment-boolean) | Spécifie que les documents produits lors d'une opération de fusion de courrier doivent être envoyés par e‑mail en tant que pièce jointe plutôt que dans le corps du courriel réel. |
| [setMailSubject(String value)](#setMailSubject-java.lang.String) | Spécifie le texte qui doit apparaître dans la ligne d'objet des e‑mails ou fax produits lors de la fusion de courrier. |
| [setMainDocumentType(int value)](#setMainDocumentType-int) | Spécifie le type de document principal de la fusion de courrier. |
| [setOdso(Odso value)](#setOdso-com.aspose.words.Odso) | Définit l'objet qui spécifie les paramètres de l'Office Data Source Object (ODSO). |
| [setQuery(String value)](#setQuery-java.lang.String) | Contient la chaîne Structured Query Language qui doit être exécutée contre la source de données externe spécifiée afin de renvoyer l'ensemble des enregistrements qui seront importés dans le document lors de l'exécution de la fusion de courrier. |
| [setViewMergedData(boolean value)](#setViewMergedData-boolean) | Spécifie que Microsoft Word doit afficher les données de la source de données externe spécifiée là où des champs de fusion ont été insérés (par ex. |
### clear() {#clear}
```
public void clear()
```


Efface les paramètres de mail merge de manière à ce que, lors de l'enregistrement du document, aucun paramètre de mail merge ne soit sauvegardé et le document devienne un document normal.

### deepClone() {#deepClone}
```
public MailMergeSettings deepClone()
```


Renvoie un clone profond de cet objet.

**Returns:**
[MailMergeSettings](../../com.aspose.words/mailmergesettings/)
### getActiveRecord() {#getActiveRecord}
```
public int getActiveRecord()
```


Spécifie l'index basé sur 1 de l'enregistrement de la source de données qui doit être affiché dans Microsoft Word. La valeur par défaut est 1.

**Returns:**
int - La valeur int correspondante.
### getAddressFieldName() {#getAddressFieldName}
```
public String getAddressFieldName()
```


Spécifie la colonne de la source de données contenant les adresses e‑mail. La valeur par défaut est une chaîne vide.

**Returns:**
java.lang.String - La valeur java.lang.String correspondante.
### getCheckErrors() {#getCheckErrors}
```
public int getCheckErrors()
```


Spécifie le type de rapport d'erreur qui doit être effectué par Microsoft Word lors d'une fusion de courrier. La valeur par défaut est [MailMergeCheckErrors.DEFAULT](../../com.aspose.words/mailmergecheckerrors/\#DEFAULT).

**Returns:**
int - La valeur int correspondante. La valeur renvoyée est l'une des constantes [MailMergeCheckErrors](../../com.aspose.words/mailmergecheckerrors/).
### getConnectString() {#getConnectString}
```
public String getConnectString()
```


Spécifie la chaîne de connexion utilisée pour se connecter à une source de données externe. La valeur par défaut est une chaîne vide.

**Returns:**
java.lang.String - La valeur java.lang.String correspondante.
### getDataSource() {#getDataSource}
```
public String getDataSource()
```


Spécifie le chemin vers la source de données de fusion de courrier. La valeur par défaut est une chaîne vide.

**Returns:**
java.lang.String - La valeur java.lang.String correspondante.
### getDataType() {#getDataType}
```
public int getDataType()
```


Spécifie le type de la source de données de fusion de courrier et la méthode d'accès aux données. La valeur par défaut est [MailMergeDataType.DEFAULT](../../com.aspose.words/mailmergedatatype/\#DEFAULT).

**Returns:**
int - La valeur int correspondante. La valeur renvoyée est l'une des constantes [MailMergeDataType](../../com.aspose.words/mailmergedatatype/).
### getDestination() {#getDestination}
```
public int getDestination()
```


Spécifie comment Microsoft Word affichera les résultats d'une fusion de courrier. La valeur par défaut est [MailMergeDestination.DEFAULT](../../com.aspose.words/mailmergedestination/\#DEFAULT).

**Returns:**
int - La valeur int correspondante. La valeur renvoyée est l'une des constantes [MailMergeDestination](../../com.aspose.words/mailmergedestination/).
### getDoNotSupressBlankLines() {#getDoNotSupressBlankLines}
```
public boolean getDoNotSupressBlankLines()
```


Spécifie comment une application effectuant la fusion de courrier doit gérer les lignes vides dans les documents fusionnés résultant de la fusion de courrier. La valeur par défaut est false.

**Returns:**
boolean - La valeur  boolean  correspondante.
### getHeaderSource() {#getHeaderSource}
```
public String getHeaderSource()
```


Spécifie le chemin vers la source d'en-tête de fusion de courrier. La valeur par défaut est une chaîne vide.

**Returns:**
java.lang.String - La valeur java.lang.String correspondante.
### getLinkToQuery() {#getLinkToQuery}
```
public boolean getLinkToQuery()
```


Pas sûr de celui-ci. La référence d'automatisation Microsoft Word indique que cela spécifie que la requête est exécutée chaque fois que le document est ouvert dans Microsoft Word. Mais la spécification OOXML indique que cela spécifie que la requête contient une référence à un fichier de requête externe contenant la requête réelle. La valeur par défaut est false.

**Returns:**
boolean - La valeur  boolean  correspondante.
### getMailAsAttachment() {#getMailAsAttachment}
```
public boolean getMailAsAttachment()
```


Spécifie que les documents produits lors d'une opération de fusion de courrier doivent être envoyés par e‑mail en tant que pièce jointe plutôt que dans le corps du courriel réel. La valeur par défaut est false.

**Returns:**
boolean - La valeur  boolean  correspondante.
### getMailSubject() {#getMailSubject}
```
public String getMailSubject()
```


Spécifie le texte qui doit apparaître dans la ligne d'objet des e‑mails ou fax générés lors de la fusion de courrier. La valeur par défaut est une chaîne vide.

**Returns:**
java.lang.String - La valeur java.lang.String correspondante.
### getMainDocumentType() {#getMainDocumentType}
```
public int getMainDocumentType()
```


Spécifie le type de document principal de la fusion de courrier. La valeur par défaut est [MailMergeMainDocumentType.DEFAULT](../../com.aspose.words/mailmergemaindocumenttype/\#DEFAULT).

 **Remarks:** 

Le document principal est le document qui contient les informations identiques pour chaque version du document fusionné.

**Returns:**
int - La valeur  int  correspondante. La valeur renvoyée est l'une des constantes [MailMergeMainDocumentType](../../com.aspose.words/mailmergemaindocumenttype/).
### getOdso() {#getOdso}
```
public Odso getOdso()
```


Obtient l'objet qui spécifie les paramètres de l'Office Data Source Object (ODSO).

 **Remarks:** 

Cet objet n'est jamais  null .

**Returns:**
[Odso](../../com.aspose.words/odso/) - The object that specifies the Office Data Source Object (ODSO) settings.
### getQuery() {#getQuery}
```
public String getQuery()
```


Contient la chaîne Structured Query Language qui doit être exécutée contre la source de données externe spécifiée afin de renvoyer l'ensemble des enregistrements qui seront importés dans le document lors de l'exécution de la fusion de courrier. La valeur par défaut est une chaîne vide.

**Returns:**
java.lang.String - La valeur java.lang.String correspondante.
### getViewMergedData() {#getViewMergedData}
```
public boolean getViewMergedData()
```


Spécifie que Microsoft Word doit afficher les données de la source de données externe spécifiée là où des champs de fusion ont été insérés (par ex. aperçu des données fusionnées). La valeur par défaut est  false .

**Returns:**
boolean - La valeur  boolean  correspondante.
### setActiveRecord(int value) {#setActiveRecord-int}
```
public void setActiveRecord(int value)
```


Spécifie l'index basé sur 1 de l'enregistrement de la source de données qui doit être affiché dans Microsoft Word. La valeur par défaut est 1.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | La valeur  int  correspondante. |

### setAddressFieldName(String value) {#setAddressFieldName-java.lang.String}
```
public void setAddressFieldName(String value)
```


Spécifie la colonne de la source de données contenant les adresses e‑mail. La valeur par défaut est une chaîne vide.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La valeur java.lang.String correspondante. |

### setCheckErrors(int value) {#setCheckErrors-int}
```
public void setCheckErrors(int value)
```


Spécifie le type de rapport d'erreur qui doit être effectué par Microsoft Word lors d'une fusion de courrier. La valeur par défaut est [MailMergeCheckErrors.DEFAULT](../../com.aspose.words/mailmergecheckerrors/\#DEFAULT).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur  int  correspondante. La valeur doit être l'une des constantes [MailMergeCheckErrors](../../com.aspose.words/mailmergecheckerrors/). |

### setConnectString(String value) {#setConnectString-java.lang.String}
```
public void setConnectString(String value)
```


Spécifie la chaîne de connexion utilisée pour se connecter à une source de données externe. La valeur par défaut est une chaîne vide.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La valeur java.lang.String correspondante. |

### setDataSource(String value) {#setDataSource-java.lang.String}
```
public void setDataSource(String value)
```


Spécifie le chemin vers la source de données de fusion de courrier. La valeur par défaut est une chaîne vide.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La valeur java.lang.String correspondante. |

### setDataType(int value) {#setDataType-int}
```
public void setDataType(int value)
```


Spécifie le type de la source de données de fusion de courrier et la méthode d'accès aux données. La valeur par défaut est [MailMergeDataType.DEFAULT](../../com.aspose.words/mailmergedatatype/\#DEFAULT).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur  int  correspondante. La valeur doit être l'une des constantes [MailMergeDataType](../../com.aspose.words/mailmergedatatype/). |

### setDestination(int value) {#setDestination-int}
```
public void setDestination(int value)
```


Spécifie comment Microsoft Word affichera les résultats d'une fusion de courrier. La valeur par défaut est [MailMergeDestination.DEFAULT](../../com.aspose.words/mailmergedestination/\#DEFAULT).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur  int  correspondante. La valeur doit être l'une des constantes [MailMergeDestination](../../com.aspose.words/mailmergedestination/). |

### setDoNotSupressBlankLines(boolean value) {#setDoNotSupressBlankLines-boolean}
```
public void setDoNotSupressBlankLines(boolean value)
```


Spécifie comment une application effectuant la fusion de courrier doit gérer les lignes vides dans les documents fusionnés résultant de la fusion de courrier. La valeur par défaut est false.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setHeaderSource(String value) {#setHeaderSource-java.lang.String}
```
public void setHeaderSource(String value)
```


Spécifie le chemin vers la source d'en-tête de fusion de courrier. La valeur par défaut est une chaîne vide.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La valeur java.lang.String correspondante. |

### setLinkToQuery(boolean value) {#setLinkToQuery-boolean}
```
public void setLinkToQuery(boolean value)
```


Pas sûr de celui-ci. La référence d'automatisation Microsoft Word indique que cela spécifie que la requête est exécutée chaque fois que le document est ouvert dans Microsoft Word. Mais la spécification OOXML indique que cela spécifie que la requête contient une référence à un fichier de requête externe contenant la requête réelle. La valeur par défaut est false.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setMailAsAttachment(boolean value) {#setMailAsAttachment-boolean}
```
public void setMailAsAttachment(boolean value)
```


Spécifie que les documents produits lors d'une opération de fusion de courrier doivent être envoyés par e‑mail en tant que pièce jointe plutôt que dans le corps du courriel réel. La valeur par défaut est false.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setMailSubject(String value) {#setMailSubject-java.lang.String}
```
public void setMailSubject(String value)
```


Spécifie le texte qui doit apparaître dans la ligne d'objet des e‑mails ou fax générés lors de la fusion de courrier. La valeur par défaut est une chaîne vide.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La valeur java.lang.String correspondante. |

### setMainDocumentType(int value) {#setMainDocumentType-int}
```
public void setMainDocumentType(int value)
```


Spécifie le type de document principal de la fusion de courrier. La valeur par défaut est [MailMergeMainDocumentType.DEFAULT](../../com.aspose.words/mailmergemaindocumenttype/\#DEFAULT).

 **Remarks:** 

Le document principal est le document qui contient les informations identiques pour chaque version du document fusionné.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur  int  correspondante. La valeur doit être l'une des constantes [MailMergeMainDocumentType](../../com.aspose.words/mailmergemaindocumenttype/). |

### setOdso(Odso value) {#setOdso-com.aspose.words.Odso}
```
public void setOdso(Odso value)
```


Définit l'objet qui spécifie les paramètres de l'Office Data Source Object (ODSO).

 **Remarks:** 

Cet objet n'est jamais  null .

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | [Odso](../../com.aspose.words/odso/) | L'objet qui spécifie les paramètres de l'Office Data Source Object (ODSO). |

### setQuery(String value) {#setQuery-java.lang.String}
```
public void setQuery(String value)
```


Contient la chaîne Structured Query Language qui doit être exécutée contre la source de données externe spécifiée afin de renvoyer l'ensemble des enregistrements qui seront importés dans le document lors de l'exécution de la fusion de courrier. La valeur par défaut est une chaîne vide.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La valeur java.lang.String correspondante. |

### setViewMergedData(boolean value) {#setViewMergedData-boolean}
```
public void setViewMergedData(boolean value)
```


Spécifie que Microsoft Word doit afficher les données de la source de données externe spécifiée là où des champs de fusion ont été insérés (par ex. aperçu des données fusionnées). La valeur par défaut est  false .

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

