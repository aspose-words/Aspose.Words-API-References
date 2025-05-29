---
title: XmlDataSource
linktitle: XmlDataSource
articleTitle: XmlDataSource
second_title: Aspose.Words pour .NET
description: Créez une source de données puissante sans effort avec le constructeur XmlDataSource, en chargeant les données XML à l'aide d'options par défaut optimisées pour une intégration transparente.
type: docs
weight: 10
url: /fr/net/aspose.words.reporting/xmldatasource/xmldatasource/
---
## XmlDataSource(*string*) {#constructor_4}

Crée une nouvelle source de données avec des données provenant d'un fichier XML en utilisant les options par défaut pour le chargement de données XML.

```csharp
public XmlDataSource(string xmlPath)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| xmlPath | String | Le chemin vers le fichier XML à utiliser comme source de données. |

## Exemples

Montrez comment utiliser XML comme source de données (chaîne).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

XmlDataSource dataSource = new XmlDataSource(MyDir + "List of people.xml");
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataString.docx");
```

### Voir également

* class [XmlDataSource](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)

---

## XmlDataSource(*Stream*) {#constructor}

Crée une nouvelle source de données avec des données provenant d'un flux XML en utilisant les options par défaut pour le chargement des données XML.

```csharp
public XmlDataSource(Stream xmlStream)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| xmlStream | Stream | Le flux de données XML à utiliser comme source de données. |

## Exemples

Montrez comment utiliser XML comme source de données (flux).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

using (FileStream stream = File.OpenRead(MyDir + "List of people.xml"))
{
    XmlDataSource dataSource = new XmlDataSource(stream);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataStream.docx");
```

### Voir également

* class [XmlDataSource](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)

---

## XmlDataSource(*string, string*) {#constructor_6}

Crée une source de données à partir d'un fichier XML, à l'aide d'un fichier de définition de schéma XML. Les options par défaut sont utilisées pour le chargement des données XML.

```csharp
public XmlDataSource(string xmlPath, string xmlSchemaPath)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| xmlPath | String | Le chemin vers le fichier XML à utiliser comme source de données. |
| xmlSchemaPath | String | Le chemin d'accès au fichier de définition de schéma XML qui fournit le schéma pour le fichier XML . |

### Voir également

* class [XmlDataSource](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, Stream*) {#constructor_2}

Crée une source de données à partir d'un flux XML utilisant un flux de définition de schéma XML. Les options par défaut sont utilisées pour le chargement des données XML.

```csharp
public XmlDataSource(Stream xmlStream, Stream xmlSchemaStream)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| xmlStream | Stream | Le flux de données XML à utiliser comme source de données. |
| xmlSchemaStream | Stream | Le flux de définition de schéma XML qui fournit un schéma pour les données XML. |

### Voir également

* class [XmlDataSource](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)

---

## XmlDataSource(*string, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_5}

Crée une nouvelle source de données avec des données provenant d'un fichier XML en utilisant les options spécifiées pour le chargement de données XML.

```csharp
public XmlDataSource(string xmlPath, XmlDataLoadOptions options)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| xmlPath | String | Le chemin vers le fichier XML à utiliser comme source de données. |
| options | XmlDataLoadOptions | Options de chargement de données XML. |

### Voir également

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_1}

Crée une nouvelle source de données avec des données provenant d'un flux XML en utilisant les options spécifiées pour le chargement de données XML.

```csharp
public XmlDataSource(Stream xmlStream, XmlDataLoadOptions options)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| xmlStream | Stream | Le flux de données XML à utiliser comme source de données. |
| options | XmlDataLoadOptions | Options de chargement de données XML. |

### Voir également

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)

---

## XmlDataSource(*string, string, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_7}

Crée une source de données à partir des données d'un fichier XML, à l'aide d'un fichier de définition de schéma XML. Les options spécifiées sont utilisées pour le chargement des données XML.

```csharp
public XmlDataSource(string xmlPath, string xmlSchemaPath, XmlDataLoadOptions options)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| xmlPath | String | Le chemin vers le fichier XML à utiliser comme source de données. |
| xmlSchemaPath | String | Le chemin d'accès au fichier de définition de schéma XML qui fournit le schéma pour le fichier XML . |
| options | XmlDataLoadOptions | Options de chargement de données XML. |

### Voir également

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)

---

## XmlDataSource(*Stream, Stream, [XmlDataLoadOptions](../../xmldataloadoptions/)*) {#constructor_3}

Crée une source de données à partir d'un flux XML utilisant un flux de définition de schéma XML. Les options spécifiées sont utilisées pour le chargement des données XML.

```csharp
public XmlDataSource(Stream xmlStream, Stream xmlSchemaStream, XmlDataLoadOptions options)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| xmlStream | Stream | Le flux de données XML à utiliser comme source de données. |
| xmlSchemaStream | Stream | Le flux de définition de schéma XML qui fournit un schéma pour les données XML. |
| options | XmlDataLoadOptions | Options de chargement de données XML. |

### Voir également

* class [XmlDataLoadOptions](../../xmldataloadoptions/)
* class [XmlDataSource](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)
