---
title: "ReportBuilderOptions"
linktitle: "ReportBuilderOptions"
second_title: "Aspose.Words für Java"
description: "Stellt Optionen für die LINQ Reporting Engine-Funktionalität in Java dar."
type: docs
weight: 573
url: /de/java/com.aspose.words/reportbuilderoptions/
---

**Inheritance:**
java.lang.Object
```
public class ReportBuilderOptions
```

Stellt Optionen für die Funktionalität der LINQ Reporting Engine dar.

 **Examples:** 

Zeigt, wie ein Dokument mit Daten gefüllt wird.

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
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [ReportBuilderOptions()](#ReportBuilderOptions) | Initialisiert eine neue Instanz dieser Klasse. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getKnownTypes()](#getKnownTypes) | Liefert ein ungeordnetes Set (d.h. |
| [getMissingMemberMessage()](#getMissingMemberMessage) | Liefert einen Zeichenkettenwert, der anstelle eines Template-Ausdrucks ausgegeben wird, der eine einfache Referenz auf ein fehlendes Mitglied eines Objekts darstellt. |
| [getOptions()](#getOptions) | Liefert ein Satz von Flags, die das Verhalten dieser [ReportingEngine](../../com.aspose.words/reportingengine/)‑Instanz beim Erstellen eines Berichts steuern. |
| [setMissingMemberMessage(String value)](#setMissingMemberMessage-java.lang.String) | Setzt einen Zeichenkettenwert, der anstelle eines Template-Ausdrucks ausgegeben wird, der eine einfache Referenz auf ein fehlendes Mitglied eines Objekts darstellt. |
| [setOptions(int value)](#setOptions-int) | Setzt einen Satz von Flags, die das Verhalten dieser [ReportingEngine](../../com.aspose.words/reportingengine/)‑Instanz beim Erstellen eines Berichts steuern. |
### ReportBuilderOptions() {#ReportBuilderOptions}
```
public ReportBuilderOptions()
```


Initialisiert eine neue Instanz dieser Klasse.

### getKnownTypes() {#getKnownTypes}
```
public KnownTypeSet getKnownTypes()
```


Liefert ein ungeordnetes Set (d.h. eine Sammlung eindeutiger Elemente), das java.lang.Class-Objekte enthält, deren vollständig oder teilweise qualifizierte Namen innerhalb von Berichtsvorlagen, die von dieser Engine-Instanz verarbeitet werden, verwendet werden können, um die statischen Mitglieder der entsprechenden Typen aufzurufen, Typumwandlungen durchzuführen usw.

**Returns:**
[KnownTypeSet](../../com.aspose.words/knowntypeset/) - An unordered set (i.e.
### getMissingMemberMessage() {#getMissingMemberMessage}
```
public String getMissingMemberMessage()
```


Liefert einen Zeichenkettenwert, der anstelle eines Template-Ausdrucks ausgegeben wird, der eine einfache Referenz auf ein fehlendes Mitglied eines Objekts darstellt. Der Standardwert ist eine leere Zeichenkette.

 **Remarks:** 

Die Eigenschaft sollte zusammen mit der Option [ReportBuildOptions.ALLOW\_MISSING\_MEMBERS](../../com.aspose.words/reportbuildoptions/\#ALLOW-MISSING-MEMBERS) verwendet werden. Andernfalls wird eine Ausnahme ausgelöst, wenn ein fehlendes Mitglied eines Objekts gefunden wird.

Die Eigenschaft wirkt sich nur auf die Ausgabe eines Template-Ausdrucks aus, der eine einfache Referenz auf ein fehlendes Objektmitglied darstellt. Zum Beispiel wird die Ausgabe eines binären Operators, bei dem einer der Operanden auf ein fehlendes Objektmitglied verweist, nicht beeinflusst.

Der Wert dieser Eigenschaft kann nicht auf null gesetzt werden.

**Returns:**
java.lang.String – Ein Zeichenkettenwert, der anstelle eines Template-Ausdrucks ausgegeben wird, der eine einfache Referenz auf ein fehlendes Mitglied eines Objekts darstellt.
### getOptions() {#getOptions}
```
public int getOptions()
```


Liefert ein Satz von Flags, die das Verhalten dieser [ReportingEngine](../../com.aspose.words/reportingengine/)‑Instanz beim Erstellen eines Berichts steuern.

 **Examples:** 

Zeigt, wie ein Dokument mit Daten gefüllt wird.

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
int – Ein Satz von Flags, die das Verhalten dieser [ReportingEngine](../../com.aspose.words/reportingengine/)‑Instanz beim Erstellen eines Berichts steuern. Der zurückgegebene Wert ist eine bitweise Kombination von [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/)‑Konstanten.
### setMissingMemberMessage(String value) {#setMissingMemberMessage-java.lang.String}
```
public void setMissingMemberMessage(String value)
```


Setzt einen Zeichenkettenwert, der anstelle eines Template-Ausdrucks ausgegeben wird, der eine einfache Referenz auf ein fehlendes Mitglied eines Objekts darstellt. Der Standardwert ist eine leere Zeichenkette.

 **Remarks:** 

Die Eigenschaft sollte zusammen mit der Option [ReportBuildOptions.ALLOW\_MISSING\_MEMBERS](../../com.aspose.words/reportbuildoptions/\#ALLOW-MISSING-MEMBERS) verwendet werden. Andernfalls wird eine Ausnahme ausgelöst, wenn ein fehlendes Mitglied eines Objekts gefunden wird.

Die Eigenschaft wirkt sich nur auf die Ausgabe eines Template-Ausdrucks aus, der eine einfache Referenz auf ein fehlendes Objektmitglied darstellt. Zum Beispiel wird die Ausgabe eines binären Operators, bei dem einer der Operanden auf ein fehlendes Objektmitglied verweist, nicht beeinflusst.

Der Wert dieser Eigenschaft kann nicht auf null gesetzt werden.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Ein Zeichenkettenwert, der anstelle eines Template-Ausdrucks ausgegeben wird, der eine einfache Referenz auf ein fehlendes Mitglied eines Objekts darstellt. |

### setOptions(int value) {#setOptions-int}
```
public void setOptions(int value)
```


Setzt einen Satz von Flags, die das Verhalten dieser [ReportingEngine](../../com.aspose.words/reportingengine/)‑Instanz beim Erstellen eines Berichts steuern.

 **Examples:** 

Zeigt, wie ein Dokument mit Daten gefüllt wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Ein Satz von Flags, die das Verhalten dieser [ReportingEngine](../../com.aspose.words/reportingengine/)‑Instanz beim Erstellen eines Berichts steuern. Der Wert muss eine bitweise Kombination von [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/)‑Konstanten sein. |

