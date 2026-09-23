---
title: "XmlDataSource"
linktitle: "XmlDataSource"
second_title: "Aspose.Words pour Java"
description: "Fournit l'accès aux données d'un fichier ou d'un flux XML à utiliser dans un rapport en Java."
type: docs
weight: 746
url: /fr/java/com.aspose.words/xmldatasource/
---

**Inheritance:**
java.lang.Object
```
public class XmlDataSource
```

Fournit l'accès aux données d'un fichier XML ou d'un flux à utiliser dans un rapport.

Pour en savoir plus, consultez l'article de documentation [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

Pour accéder aux données du fichier ou du flux correspondant lors de la génération d'un rapport, transmettez une instance de cette classe en tant que source de données à l'une des surcharges de [ReportingEngine](../../com.aspose.words/reportingengine/). buildReport.

Dans les documents modèles, si un élément XML de niveau supérieur ne contient qu'une liste d'éléments du même type, une instance de [XmlDataSource](../../com.aspose.words/xmldatasource/) doit être traitée de la même manière qu'une instance de [DataTable](../../com.aspose.words.net.system.data/datatable/). Sinon, une instance de [XmlDataSource](../../com.aspose.words/xmldatasource/) doit être traitée de la même manière qu'une instance de [DataRow](../../com.aspose.words.net.system.data/datarow/). Pour plus d'informations, voir la référence de la syntaxe des modèles(https://docs.aspose.com/display/wordsjava/Template+Syntax).

Lorsque la définition du schéma XML est passée au constructeur de cette classe, les types de données des valeurs des éléments XML simples et des attributs sont déterminés selon le schéma. Ainsi, dans les documents modèles, vous pouvez travailler avec des valeurs typées plutôt qu'avec de simples chaînes.

Lorsque la définition du schéma XML n'est pas passée au constructeur de cette classe, les types de données des valeurs des éléments XML simples et des attributs sont déterminés automatiquement à partir de leurs représentations sous forme de chaînes. Ainsi, dans les documents modèles, vous pouvez également travailler avec des valeurs typées dans ce cas. Le moteur est capable de reconnaître automatiquement les valeurs des types suivants :

 *  long
 *  double
 *  boolean
 *  java.util.Date
 *  java.lang.String

Notez que, pour que la reconnaissance automatique des types de données fonctionne, les représentations sous forme de chaînes des valeurs des éléments XML simples et des attributs doivent être générées en utilisant des paramètres culturels invariants.

Pour remplacer le comportement par défaut du chargement des données XML, initialisez et transmettez une instance de [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) au constructeur de cette classe.

 **Examples:** 

Montrez comment utiliser XML comme source de données (chaîne).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - XML data destination (Java).docx");

 XmlDataSource dataSource = new XmlDataSource(getMyDir() + "List of people.xml");
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.XmlDataString.docx");
 
```

Montrez comment utiliser XML comme source de données (flux).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - XML data destination (Java).docx");

 InputStream stream = new FileInputStream(getMyDir() + "List of people.xml");
 try {
     XmlDataSource dataSource = new XmlDataSource(stream);
     buildReport(doc, dataSource, "persons");
 } finally {
     stream.close();
 }

 doc.save(getArtifactsDir() + "ReportingEngine.XmlDataStream.docx");
 
```


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Constructors

| Constructor | Description |
| --- | --- |
| [XmlDataSource(String xmlPath)](#XmlDataSource-java.lang.String) | Crée une nouvelle source de données avec les données d'un fichier XML en utilisant les options par défaut pour le chargement des données XML. |
| [XmlDataSource(InputStream xmlStream)](#XmlDataSource-java.io.InputStream) | Initialise une nouvelle instance de cette classe. |
| [XmlDataSource(String xmlPath, String xmlSchemaPath)](#XmlDataSource-java.lang.String-java.lang.String) | Crée une nouvelle source de données avec les données d'un fichier XML en utilisant un fichier de définition de schéma XML. |
| [XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream)](#XmlDataSource-java.io.InputStream-java.io.InputStream) | Initialise une nouvelle instance de cette classe. |
| [XmlDataSource(String xmlPath, XmlDataLoadOptions options)](#XmlDataSource-java.lang.String-com.aspose.words.XmlDataLoadOptions) | Crée une nouvelle source de données avec les données d'un fichier XML en utilisant les options spécifiées pour le chargement des données XML. |
| [XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options)](#XmlDataSource-java.io.InputStream-com.aspose.words.XmlDataLoadOptions) | Initialise une nouvelle instance de cette classe. |
| [XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options)](#XmlDataSource-java.lang.String-java.lang.String-com.aspose.words.XmlDataLoadOptions) | Crée une nouvelle source de données avec les données d'un fichier XML en utilisant un fichier de définition de schéma XML. |
| [XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options)](#XmlDataSource-java.io.InputStream-java.io.InputStream-com.aspose.words.XmlDataLoadOptions) | Initialise une nouvelle instance de cette classe. |
### XmlDataSource(String xmlPath) {#XmlDataSource-java.lang.String}
```
public XmlDataSource(String xmlPath)
```


Crée une nouvelle source de données avec les données d'un fichier XML en utilisant les options par défaut pour le chargement des données XML.

 **Examples:** 

Montrez comment utiliser XML comme source de données (chaîne).

```

 Document doc = new Document(getMyDir() + "Reporting engine template - XML data destination (Java).docx");

 XmlDataSource dataSource = new XmlDataSource(getMyDir() + "List of people.xml");
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.XmlDataString.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| xmlPath | java.lang.String | Le chemin du fichier XML à utiliser comme source de données. |

### XmlDataSource(InputStream xmlStream) {#XmlDataSource-java.io.InputStream}
```
public XmlDataSource(InputStream xmlStream)
```


Initialise une nouvelle instance de cette classe.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |

### XmlDataSource(String xmlPath, String xmlSchemaPath) {#XmlDataSource-java.lang.String-java.lang.String}
```
public XmlDataSource(String xmlPath, String xmlSchemaPath)
```


Crée une nouvelle source de données avec les données d'un fichier XML en utilisant un fichier de définition de schéma XML. Les options par défaut sont utilisées pour le chargement des données XML.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| xmlPath | java.lang.String | Le chemin du fichier XML à utiliser comme source de données. |
| xmlSchemaPath | java.lang.String | Le chemin du fichier de définition de schéma XML qui fournit le schéma pour le fichier XML. |

### XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream) {#XmlDataSource-java.io.InputStream-java.io.InputStream}
```
public XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream)
```


Initialise une nouvelle instance de cette classe.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| xmlSchemaStream | java.io.InputStream |  |

### XmlDataSource(String xmlPath, XmlDataLoadOptions options) {#XmlDataSource-java.lang.String-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(String xmlPath, XmlDataLoadOptions options)
```


Crée une nouvelle source de données avec les données d'un fichier XML en utilisant les options spécifiées pour le chargement des données XML.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| xmlPath | java.lang.String | Le chemin du fichier XML à utiliser comme source de données. |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) | Options pour le chargement des données XML. |

### XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options) {#XmlDataSource-java.io.InputStream-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options)
```


Initialise une nouvelle instance de cette classe.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) |  |

### XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options) {#XmlDataSource-java.lang.String-java.lang.String-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options)
```


Crée une nouvelle source de données avec les données d'un fichier XML en utilisant un fichier de définition de schéma XML. Les options spécifiées sont utilisées pour le chargement des données XML.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| xmlPath | java.lang.String | Le chemin du fichier XML à utiliser comme source de données. |
| xmlSchemaPath | java.lang.String | Le chemin du fichier de définition de schéma XML qui fournit le schéma pour le fichier XML. |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) | Options pour le chargement des données XML. |

### XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options) {#XmlDataSource-java.io.InputStream-java.io.InputStream-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options)
```


Initialise une nouvelle instance de cette classe.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| xmlSchemaStream | java.io.InputStream |  |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) |  |

