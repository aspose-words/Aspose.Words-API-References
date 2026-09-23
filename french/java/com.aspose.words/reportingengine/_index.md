---
title: "ReportingEngine"
linktitle: "ReportingEngine"
second_title: "Aspose.Words pour Java"
description: "Fournit des routines pour remplir des documents modèle avec des données et un ensemble de paramètres pour contrôler ces routines en Java."
type: docs
weight: 574
url: /fr/java/com.aspose.words/reportingengine/
---

**Inheritance:**
java.lang.Object
```
public class ReportingEngine
```

Fournit des routines pour remplir les documents modèles avec des données ainsi qu'un ensemble de paramètres pour contrôler ces routines.

Pour en savoir plus, consultez l'article de documentation [ LINQ Reporting Engine ][LINQ Reporting Engine].


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Constructors

| Constructor | Description |
| --- | --- |
| [ReportingEngine()](#ReportingEngine) | Initialise une nouvelle instance de cette classe. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [buildReport(Document document, Object dataSource)](#buildReport-com.aspose.words.Document-java.lang.Object) | Remplit le document modèle spécifié avec des données provenant de la source spécifiée, le transformant en rapport prêt. |
| [buildReport(Document document, Object dataSource, String dataSourceName)](#buildReport-com.aspose.words.Document-java.lang.Object-java.lang.String) | Remplit le document modèle spécifié avec des données provenant de la source spécifiée, le transformant en rapport prêt. |
| [buildReport(Document document, Object[] dataSources, String[] dataSourceNames)](#buildReport-com.aspose.words.Document-java.lang.Object---java.lang.String) | Remplit le document modèle spécifié avec des données provenant des sources spécifiées, le transformant en rapport prêt. |
| [equals(Object obj)](#equals-java.lang.Object) |  |
| [getKnownTypes()](#getKnownTypes) | Obtient un ensemble non ordonné (c’est‑à‑dire |
| [getMissingMemberMessage()](#getMissingMemberMessage) | Obtient une valeur chaîne imprimée à la place d’une expression de modèle qui représente une référence simple à un membre manquant d’un objet. |
| [getOptions()](#getOptions) | Obtient un ensemble de drapeaux contrôlant le comportement de cette instance de [ReportingEngine](../../com.aspose.words/reportingengine/) lors de la génération d’un rapport. |
| [getRestrictedTypes()](#getRestrictedTypes) | Renvoie les types dont les membres ainsi que ceux des types dérivés doivent être inaccessibles au moteur via la syntaxe du modèle. |
| [getUseReflectionOptimization()](#getUseReflectionOptimization) | Obtient une valeur indiquant si les appels aux membres de types personnalisés effectués via l'API de réflexion sont optimisés à l'aide de la génération de classes dynamiques ou non. |
| [hashCode()](#hashCode) |  |
| [setMissingMemberMessage(String value)](#setMissingMemberMessage-java.lang.String) | Définit une valeur chaîne imprimée à la place d’une expression de modèle qui représente une référence simple à un membre manquant d’un objet. |
| [setOptions(int value)](#setOptions-int) | Définit un ensemble de drapeaux contrôlant le comportement de cette instance de [ReportingEngine](../../com.aspose.words/reportingengine/) lors de la génération d’un rapport. |
| [setRestrictedTypes(Class[] types)](#setRestrictedTypes-java.lang.Class...) | Spécifie les types dont les membres ainsi que ceux des types dérivés doivent être inaccessibles au moteur via la syntaxe du modèle. |
| [setUseReflectionOptimization(boolean value)](#setUseReflectionOptimization-boolean) | Définit une valeur indiquant si les appels aux membres de types personnalisés effectués via l'API de réflexion sont optimisés à l'aide de la génération de classes dynamiques ou non. |
### ReportingEngine() {#ReportingEngine}
```
public ReportingEngine()
```


Initialise une nouvelle instance de cette classe.

### buildReport(Document document, Object dataSource) {#buildReport-com.aspose.words.Document-java.lang.Object}
```
public boolean buildReport(Document document, Object dataSource)
```


Remplit le document modèle spécifié avec des données provenant de la source spécifiée, le transformant en rapport prêt.

 **Remarks:** 

En utilisant cette surcharge, vous pouvez référencer les membres de la source de données dans le document modèle, mais vous ne pouvez pas référencer l'objet source de données lui‑même. Vous devez utiliser la surcharge [buildReport(com.aspose.words.Document, java.lang.Object, java.lang.String)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object--java.lang.String) pour y parvenir.

Un objet source de données peut être de l'un des types suivants :

 *  [XmlDataSource](../../com.aspose.words/xmldatasource/)
 *  [JsonDataSource](../../com.aspose.words/jsondatasource/)
 *  [CsvDataSource](../../com.aspose.words/csvdatasource/)
 *  [DataSet](../../com.aspose.words.net.system.data/dataset/)
 *  [DataTable](../../com.aspose.words.net.system.data/datatable/)
 *  [DataRow](../../com.aspose.words.net.system.data/datarow/)
 *  [IDataReader](../../com.aspose.words.net.system.data/idatareader/)
 *  [IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
 *  [DataView](../../com.aspose.words.net.system.data/dataview/)
 *  [DataRowView](../../com.aspose.words.net.system.data/datarowview/)
 *  Any other arbitrary Java type

Pour obtenir des informations sur la façon de travailler avec des sources de données de différents types dans les documents modèle, consultez la référence de la syntaxe du modèle (https://docs.aspose.com/display/wordsjava/Template+Syntax).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | Un document modèle à remplir avec des données. |
| dataSource | java.lang.Object | Un objet source de données. |

**Returns:**
boolean - Un indicateur indiquant si l'analyse du document modèle a réussi. L'indicateur retourné n'a de sens que si la valeur de la propriété [getOptions()](../../com.aspose.words/reportingengine/\#getOptions) / [setOptions(int)](../../com.aspose.words/reportingengine/\#setOptions-int) inclut l'option [ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions/\#INLINE-ERROR-MESSAGES).
### buildReport(Document document, Object dataSource, String dataSourceName) {#buildReport-com.aspose.words.Document-java.lang.Object-java.lang.String}
```
public boolean buildReport(Document document, Object dataSource, String dataSourceName)
```


Remplit le document modèle spécifié avec des données provenant de la source spécifiée, le transformant en rapport prêt.

 **Remarks:** 

En utilisant cette surcharge, vous pouvez référencer les membres de la source de données ainsi que l'objet source de données lui‑même dans le modèle. Si vous ne prévoyez pas de référencer l'objet source de données, vous pouvez omettre dataSourceName en passant null ou utiliser la surcharge [buildReport(com.aspose.words.Document, java.lang.Object)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object).

Un objet source de données peut être de l'un des types suivants :

 *  [XmlDataSource](../../com.aspose.words/xmldatasource/)
 *  [JsonDataSource](../../com.aspose.words/jsondatasource/)
 *  [CsvDataSource](../../com.aspose.words/csvdatasource/)
 *  [DataSet](../../com.aspose.words.net.system.data/dataset/)
 *  [DataTable](../../com.aspose.words.net.system.data/datatable/)
 *  [DataRow](../../com.aspose.words.net.system.data/datarow/)
 *  [IDataReader](../../com.aspose.words.net.system.data/idatareader/)
 *  [IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
 *  [DataView](../../com.aspose.words.net.system.data/dataview/)
 *  [DataRowView](../../com.aspose.words.net.system.data/datarowview/)
 *  Any other arbitrary Java type

Pour obtenir des informations sur la façon de travailler avec des sources de données de différents types dans les documents modèle, consultez la référence de la syntaxe du modèle (https://docs.aspose.com/display/wordsjava/Template+Syntax).

 **Examples:** 

Montre comment autoriser les membres manquants.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

Montre comment afficher les valeurs sous forme de texte en dollars.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("<<[ds.getValue1()]:dollarText>>\r<<[ds.getValue2()]:dollarText>>");

 NumericTestClass testData = new NumericTestBuilder().withValues(1234, 5621718.589).build();

 ReportingEngine report = new ReportingEngine();
 report.getKnownTypes().add(NumericTestClass.class);
 report.buildReport(doc, testData, "ds");

 doc.save(getArtifactsDir() + "ReportingEngine.DollarTextFormat.docx");
 
```

Montre comment supprimer sélectivement des paragraphes.

```

 // Template contains tags with an exclamation mark. For such tags, empty paragraphs will be removed.
 Document doc = new Document(getMyDir() + "Reporting engine template - Selective remove paragraphs.docx");

 ReportingEngine engine = new ReportingEngine();
 engine.buildReport(doc, false, "value");

 doc.save(getArtifactsDir() + "ReportingEngine.SelectiveDeletionOfParagraphs.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | Un document modèle à remplir avec des données. |
| dataSource | java.lang.Object | Un objet source de données. |
| dataSourceName | java.lang.String | Un nom pour référencer l'objet source de données dans le modèle. |

**Returns:**
boolean - Un indicateur indiquant si l'analyse du document modèle a réussi. L'indicateur retourné n'a de sens que si la valeur de la propriété [getOptions()](../../com.aspose.words/reportingengine/\#getOptions) / [setOptions(int)](../../com.aspose.words/reportingengine/\#setOptions-int) inclut l'option [ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions/\#INLINE-ERROR-MESSAGES).
### buildReport(Document document, Object[] dataSources, String[] dataSourceNames) {#buildReport-com.aspose.words.Document-java.lang.Object---java.lang.String}
```
public boolean buildReport(Document document, Object[] dataSources, String[] dataSourceNames)
```


Remplit le document modèle spécifié avec des données provenant des sources spécifiées, le transformant en rapport prêt.

 **Remarks:** 

En utilisant cette surcharge, vous pouvez référencer plusieurs objets source de données et leurs membres dans le modèle. Le nom de la première source de données peut être omis (c’est‑à‑dire être une chaîne vide ou null) si vous ne comptez référencer que les membres de la source de données et non l'objet source lui‑même. Les noms des autres sources de données doivent être spécifiés et uniques.

Si vous prévoyez d'utiliser une seule source de données, envisagez d'utiliser les surcharges [buildReport(com.aspose.words.Document, java.lang.Object)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object) et [buildReport(com.aspose.words.Document, java.lang.Object, java.lang.String)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object--java.lang.String) à la place.

Un objet source de données peut être de l'un des types suivants :

 *  [XmlDataSource](../../com.aspose.words/xmldatasource/)
 *  [JsonDataSource](../../com.aspose.words/jsondatasource/)
 *  [CsvDataSource](../../com.aspose.words/csvdatasource/)
 *  [DataSet](../../com.aspose.words.net.system.data/dataset/)
 *  [DataTable](../../com.aspose.words.net.system.data/datatable/)
 *  [DataRow](../../com.aspose.words.net.system.data/datarow/)
 *  [IDataReader](../../com.aspose.words.net.system.data/idatareader/)
 *  [IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
 *  [DataView](../../com.aspose.words.net.system.data/dataview/)
 *  [DataRowView](../../com.aspose.words.net.system.data/datarowview/)
 *  Any other arbitrary Java type

Pour obtenir des informations sur la façon de travailler avec des sources de données de différents types dans les documents modèle, consultez la référence de la syntaxe du modèle (https://docs.aspose.com/display/wordsjava/Template+Syntax).

 **Examples:** 

Montre comment conserver la numérotation insérée telle quelle.

```

 // By default, numbered lists from a template document are continued when their identifiers match those from a document being inserted.
 // With "-sourceNumbering" numbering should be separated and kept as is.
 Document template = DocumentHelper.createSimpleDocument("<>" + System.lineSeparator() + "<>");

 DocumentTestClass doc = new DocumentTestBuilder()
         .withDocument(new Document(getMyDir() + "List item.docx")).build();

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.REMOVE_EMPTY_PARAGRAPHS); }
 engine.buildReport(template, new Object[] { doc }, new String[] { "src" });

 template.save(getArtifactsDir() + "ReportingEngine.SourseListNumbering.docx");
 
```

Montre comment travailler avec les graphiques de Word 2016.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Word 2016 Charts (Java).docx");

 ReportingEngine engine = new ReportingEngine();
 engine.buildReport(doc, new Object[] { Common.getShares(), Common.getShareQuotes() },
         new String[] { "shares", "quotes" });

 doc.save(getArtifactsDir() + "ReportingEngine.Word2016Charts.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | Un document modèle à remplir avec des données. |
| dataSources | java.lang.Object[] | Un tableau d'objets source de données. |
| dataSourceNames | java.lang.String[] | Un tableau de noms pour référencer les objets source de données dans le modèle. |

**Returns:**
boolean - Un indicateur indiquant si l'analyse du document modèle a réussi. L'indicateur retourné n'a de sens que si la valeur de la propriété [getOptions()](../../com.aspose.words/reportingengine/\#getOptions) / [setOptions(int)](../../com.aspose.words/reportingengine/\#setOptions-int) inclut l'option [ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions/\#INLINE-ERROR-MESSAGES).
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getKnownTypes() {#getKnownTypes}
```
public KnownTypeSet getKnownTypes()
```


Obtient un ensemble non ordonné (c’est‑à‑dire une collection d’éléments uniques) contenant des objets java.lang.Class dont les noms entièrement ou partiellement qualifiés peuvent être utilisés dans les modèles de rapport traités par cette instance du moteur pour invoquer les membres statiques des types correspondants, effectuer des conversions de type, etc.

**Returns:**
[KnownTypeSet](../../com.aspose.words/knowntypeset/) - An unordered set (i.e.
### getMissingMemberMessage() {#getMissingMemberMessage}
```
public String getMissingMemberMessage()
```


Obtient une valeur chaîne imprimée à la place d’une expression de modèle qui représente une référence simple à un membre manquant d’un objet. La valeur par défaut est une chaîne vide.

 **Remarks:** 

La propriété doit être utilisée en conjonction avec l’option [ReportBuildOptions.ALLOW\_MISSING\_MEMBERS](../../com.aspose.words/reportbuildoptions/\#ALLOW-MISSING-MEMBERS). Sinon, une exception est levée lorsqu’un membre manquant d’un objet est rencontré.

La propriété n’affecte que l’impression d’une expression de modèle représentant une référence simple à un membre d’objet manquant. Par exemple, l’impression d’un opérateur binaire dont l’un des opérandes fait référence à un membre d’objet manquant n’est pas affectée.

La valeur de cette propriété ne peut pas être définie sur null.

 **Examples:** 

Montre comment autoriser les membres manquants.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

**Returns:**
java.lang.String - Une valeur chaîne imprimée à la place d’une expression de modèle qui représente une référence simple à un membre manquant d’un objet.
### getOptions() {#getOptions}
```
public int getOptions()
```


Obtient un ensemble de drapeaux contrôlant le comportement de cette instance de [ReportingEngine](../../com.aspose.words/reportingengine/) lors de la génération d’un rapport.

 **Examples:** 

Montre comment autoriser les membres manquants.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

Montre comment définir les options pour le Reporting Engine

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Fields (Java).docx");

 // Note that enabling of the option makes the engine to update fields while building a report,
 // so there is no need to update fields separately after that.
 ReportingEngine engine = new ReportingEngine();
 engine.setOptions(ReportBuildOptions.UPDATE_FIELDS_SYNTAX_AWARE);
 engine.buildReport(doc, new String[] { "First topic", "Second topic", "Third topic" }, "topics");

 doc.save(getArtifactsDir() + "ReportingEngine.UpdateFieldsSyntaxAware.docx");
 
```

**Returns:**
int - Un ensemble de drapeaux contrôlant le comportement de cette instance de [ReportingEngine](../../com.aspose.words/reportingengine/) lors de la génération d’un rapport. La valeur retournée est une combinaison binaire des constantes de [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/).
### getRestrictedTypes() {#getRestrictedTypes}
```
public static Class[] getRestrictedTypes()
```


Renvoie les types dont les membres ainsi que ceux des types dérivés doivent être inaccessibles au moteur via la syntaxe du modèle.

 **Remarks:** 

Le tableau retourné contient les éléments précédemment définis en utilisant [setRestrictedTypes(java.lang.Class[])](../../com.aspose.words/reportingengine/\#setRestrictedTypes-java.lang.Class).

Modifier les éléments du tableau retourné n'a aucun effet sur les types restreints. Pour modifier les types restreints, utilisez [setRestrictedTypes(java.lang.Class[])](../../com.aspose.words/reportingengine/\#setRestrictedTypes-java.lang.Class) à la place.

**Returns:**
java.lang.Class[] - Types dont les membres ainsi que les membres des types dérivés doivent être inaccessibles pour le moteur via la syntaxe du modèle.
### getUseReflectionOptimization() {#getUseReflectionOptimization}
```
public static boolean getUseReflectionOptimization()
```


Obtient une valeur indiquant si les appels aux membres de types personnalisés effectués via l'API de réflexion sont optimisés à l'aide de la génération de classes dynamiques ou non. La valeur par défaut est  true .

 **Remarks:** 

Il existe certains scénarios où il est préférable de désactiver cette optimisation. Par exemple, si vous travaillez constamment avec de petites collections d'éléments de données, le coût de la génération de classes dynamiques peut être plus perceptible que celui des appels directs à l'API de réflexion. L'option n'a aucun effet lorsqu'elle est exécutée sur iOS et que l'optimisation de la réflexion n'est pas utilisée.

**Returns:**
boolean - Une valeur indiquant si les appels aux membres de types personnalisés effectués via l'API de réflexion sont optimisés à l'aide de la génération de classes dynamiques ou non.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### setMissingMemberMessage(String value) {#setMissingMemberMessage-java.lang.String}
```
public void setMissingMemberMessage(String value)
```


Définit une valeur chaîne imprimée à la place d’une expression de modèle qui représente une référence simple à un membre manquant d’un objet. La valeur par défaut est une chaîne vide.

 **Remarks:** 

La propriété doit être utilisée en conjonction avec l’option [ReportBuildOptions.ALLOW\_MISSING\_MEMBERS](../../com.aspose.words/reportbuildoptions/\#ALLOW-MISSING-MEMBERS). Sinon, une exception est levée lorsqu’un membre manquant d’un objet est rencontré.

La propriété n’affecte que l’impression d’une expression de modèle représentant une référence simple à un membre d’objet manquant. Par exemple, l’impression d’un opérateur binaire dont l’un des opérandes fait référence à un membre d’objet manquant n’est pas affectée.

La valeur de cette propriété ne peut pas être définie sur null.

 **Examples:** 

Montre comment autoriser les membres manquants.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Une valeur chaîne imprimée à la place d’une expression de modèle qui représente une référence simple à un membre manquant d’un objet. |

### setOptions(int value) {#setOptions-int}
```
public void setOptions(int value)
```


Définit un ensemble de drapeaux contrôlant le comportement de cette instance de [ReportingEngine](../../com.aspose.words/reportingengine/) lors de la génération d’un rapport.

 **Examples:** 

Montre comment autoriser les membres manquants.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

Montre comment définir les options pour le Reporting Engine

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Fields (Java).docx");

 // Note that enabling of the option makes the engine to update fields while building a report,
 // so there is no need to update fields separately after that.
 ReportingEngine engine = new ReportingEngine();
 engine.setOptions(ReportBuildOptions.UPDATE_FIELDS_SYNTAX_AWARE);
 engine.buildReport(doc, new String[] { "First topic", "Second topic", "Third topic" }, "topics");

 doc.save(getArtifactsDir() + "ReportingEngine.UpdateFieldsSyntaxAware.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | Un ensemble de drapeaux contrôlant le comportement de cette instance de [ReportingEngine](../../com.aspose.words/reportingengine/) lors de la génération d’un rapport. La valeur doit être une combinaison binaire des constantes de [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/). |

### setRestrictedTypes(Class[] types) {#setRestrictedTypes-java.lang.Class...}
```
public static void setRestrictedTypes(Class[] types)
```


Spécifie les types dont les membres ainsi que ceux des types dérivés doivent être inaccessibles au moteur via la syntaxe du modèle.

 **Remarks:** 

Les types restreints doivent être définis avant la toute première génération d'un rapport. Après l'invocation de  BuildReportbuildReport , les types restreints ne peuvent plus être modifiés et une exception est levée en cas de tentative. Le meilleur endroit pour définir les types restreints est le démarrage de l'application.

Notez qu'un grand nombre de types restreints peut affecter les performances, il est donc préférable de restreindre uniquement les types dont l'accès aux membres est réellement sensible.

Lance java.lang.IllegalArgumentException dans les cas suivants :

\-  types  est nul.

\- Un des éléments de  types  est  nul .

\- Un des éléments de  types  représente un type invisible, c.-à-d. un type non public ou un type imbriqué public dont le type externe est non public.

\- Un des éléments de  types  représente un type tableau.

\-  types  contiennent des entrées en double.

 **Examples:** 

Montre comment refuser l'accès aux membres de types considérés comme non sécurisés.

```

 Document doc =
         DocumentHelper.createSimpleDocument(
                 "<><<[typeVar]>>");

 // Note, that you can't set restricted types during or after building a report.
 ReportingEngine.setRestrictedTypes(Class.class);
 // We set "AllowMissingMembers" option to avoid exceptions during building a report.
 ReportingEngine engine = new ReportingEngine();
 engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
 engine.buildReport(doc, new Object());

 // We get an empty string because we can't access the GetType() method.
 Assert.assertEquals(doc.getText().trim(), "");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| types | java.lang.Class[] | Types à restreindre. |

### setUseReflectionOptimization(boolean value) {#setUseReflectionOptimization-boolean}
```
public static void setUseReflectionOptimization(boolean value)
```


Définit une valeur indiquant si les appels aux membres de types personnalisés effectués via l'API de réflexion sont optimisés à l'aide de la génération de classes dynamiques ou non. La valeur par défaut est  true .

 **Remarks:** 

Il existe certains scénarios où il est préférable de désactiver cette optimisation. Par exemple, si vous travaillez constamment avec de petites collections d'éléments de données, le coût de la génération de classes dynamiques peut être plus perceptible que celui des appels directs à l'API de réflexion. L'option n'a aucun effet lorsqu'elle est exécutée sur iOS et que l'optimisation de la réflexion n'est pas utilisée.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Une valeur indiquant si les appels aux membres de types personnalisés effectués via l'API de réflexion sont optimisés à l'aide de la génération de classes dynamiques ou non. |

