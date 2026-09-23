---
title: "ReportBuilderOptions"
linktitle: "ReportBuilderOptions"
second_title: "Aspose.Words pour Java"
description: "Représente les options pour la fonctionnalité du moteur de génération de rapports LINQ en Java."
type: docs
weight: 573
url: /fr/java/com.aspose.words/reportbuilderoptions/
---

**Inheritance:**
java.lang.Object
```
public class ReportBuilderOptions
```

Représente les options pour la fonctionnalité de LINQ Reporting Engine.

 **Examples:** 

Montre comment remplir le document avec des données.

```

 public void buildReportData() throws Exception {
     // There is a several ways to populate document with data:
     String doc = getMyDir() + "Reporting engine template - If greedy (Java).docx";

     AsposeData obj = new AsposeData();
     {
         obj.setList(new ArrayList<>());
         {
             obj.getList().add("abc");
         }
     }

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.1.docx", obj);
     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.2.docx", obj, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.3.docx", SaveFormat.DOCX, obj);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.4.docx", SaveFormat.DOCX, obj, options);
 }

 public static class AsposeData {
     public ArrayList getList() {
         return mList;
     }

     ;

     public void setList(ArrayList value) {
         mList = value;
     }

     ;

     private ArrayList mList;
 }
 
```
## Constructors

| Constructor | Description |
| --- | --- |
| [ReportBuilderOptions()](#ReportBuilderOptions) | Initialise une nouvelle instance de cette classe. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [getKnownTypes()](#getKnownTypes) | Obtient un ensemble non ordonné (c’est‑à‑dire |
| [getMissingMemberMessage()](#getMissingMemberMessage) | Obtient une valeur chaîne imprimée à la place d’une expression de modèle qui représente une référence simple à un membre manquant d’un objet. |
| [getOptions()](#getOptions) | Obtient un ensemble de drapeaux contrôlant le comportement de cette instance de [ReportingEngine](../../com.aspose.words/reportingengine/) lors de la génération d’un rapport. |
| [setMissingMemberMessage(String value)](#setMissingMemberMessage-java.lang.String) | Définit une valeur chaîne imprimée à la place d’une expression de modèle qui représente une référence simple à un membre manquant d’un objet. |
| [setOptions(int value)](#setOptions-int) | Définit un ensemble de drapeaux contrôlant le comportement de cette instance de [ReportingEngine](../../com.aspose.words/reportingengine/) lors de la génération d’un rapport. |
### ReportBuilderOptions() {#ReportBuilderOptions}
```
public ReportBuilderOptions()
```


Initialise une nouvelle instance de cette classe.

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

**Returns:**
java.lang.String - Une valeur chaîne imprimée à la place d’une expression de modèle qui représente une référence simple à un membre manquant d’un objet.
### getOptions() {#getOptions}
```
public int getOptions()
```


Obtient un ensemble de drapeaux contrôlant le comportement de cette instance de [ReportingEngine](../../com.aspose.words/reportingengine/) lors de la génération d’un rapport.

 **Examples:** 

Montre comment remplir le document avec des données.

```

 public void buildReportData() throws Exception {
     // There is a several ways to populate document with data:
     String doc = getMyDir() + "Reporting engine template - If greedy (Java).docx";

     AsposeData obj = new AsposeData();
     {
         obj.setList(new ArrayList<>());
         {
             obj.getList().add("abc");
         }
     }

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.1.docx", obj);
     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.2.docx", obj, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.3.docx", SaveFormat.DOCX, obj);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.4.docx", SaveFormat.DOCX, obj, options);
 }

 public static class AsposeData {
     public ArrayList getList() {
         return mList;
     }

     ;

     public void setList(ArrayList value) {
         mList = value;
     }

     ;

     private ArrayList mList;
 }
 
```

**Returns:**
int - Un ensemble de drapeaux contrôlant le comportement de cette instance de [ReportingEngine](../../com.aspose.words/reportingengine/) lors de la génération d’un rapport. La valeur retournée est une combinaison binaire des constantes de [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/).
### setMissingMemberMessage(String value) {#setMissingMemberMessage-java.lang.String}
```
public void setMissingMemberMessage(String value)
```


Définit une valeur chaîne imprimée à la place d’une expression de modèle qui représente une référence simple à un membre manquant d’un objet. La valeur par défaut est une chaîne vide.

 **Remarks:** 

La propriété doit être utilisée en conjonction avec l’option [ReportBuildOptions.ALLOW\_MISSING\_MEMBERS](../../com.aspose.words/reportbuildoptions/\#ALLOW-MISSING-MEMBERS). Sinon, une exception est levée lorsqu’un membre manquant d’un objet est rencontré.

La propriété n’affecte que l’impression d’une expression de modèle représentant une référence simple à un membre d’objet manquant. Par exemple, l’impression d’un opérateur binaire dont l’un des opérandes fait référence à un membre d’objet manquant n’est pas affectée.

La valeur de cette propriété ne peut pas être définie sur null.

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

Montre comment remplir le document avec des données.

```

 public void buildReportData() throws Exception {
     // There is a several ways to populate document with data:
     String doc = getMyDir() + "Reporting engine template - If greedy (Java).docx";

     AsposeData obj = new AsposeData();
     {
         obj.setList(new ArrayList<>());
         {
             obj.getList().add("abc");
         }
     }

     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.1.docx", obj);
     ReportBuilderOptions options = new ReportBuilderOptions();
     options.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.2.docx", obj, options);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.3.docx", SaveFormat.DOCX, obj);
     ReportBuilder.buildReport(doc, getArtifactsDir() + "LowCode.BuildReportWithObject.4.docx", SaveFormat.DOCX, obj, options);
 }

 public static class AsposeData {
     public ArrayList getList() {
         return mList;
     }

     ;

     public void setList(ArrayList value) {
         mList = value;
     }

     ;

     private ArrayList mList;
 }
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | Un ensemble de drapeaux contrôlant le comportement de cette instance de [ReportingEngine](../../com.aspose.words/reportingengine/) lors de la génération d’un rapport. La valeur doit être une combinaison binaire des constantes de [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/). |

