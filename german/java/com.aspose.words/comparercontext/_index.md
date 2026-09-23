---
title: "ComparerContext"
linktitle: "ComparerContext"
second_title: "Aspose.Words für Java"
description: "Dokumentenvergleichskontext in Java."
type: docs
weight: 115
url: /de/java/com.aspose.words/comparercontext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.ProcessorContext](../../com.aspose.words/processorcontext/)
```
public class ComparerContext extends ProcessorContext
```

Dokumentvergleichskontext

 **Examples:** 

Zeigt, wie man Dokumente einfach mithilfe von Kontext vergleicht.

```

 // There is a several ways to compare documents:
 String firstDoc = getMyDir() + "Table column bookmarks.docx";
 String secondDoc = getMyDir() + "Table column bookmarks.doc";

 ComparerContext comparerContext = new ComparerContext();
 comparerContext.getCompareOptions().setIgnoreCaseChanges(true);
 comparerContext.setAuthor("Author");
 comparerContext.setDateTime(new Date());

 Comparer.create(comparerContext)
         .from(firstDoc)
         .from(secondDoc)
         .to(getArtifactsDir() + "LowCode.CompareContextDocuments.docx")
         .execute();
 
```

Zeigt, wie man Dokumente aus dem Stream mithilfe von Kontext vergleicht.

```

 // There is a several ways to compare documents from the stream:
 try (FileInputStream firstStreamIn = new FileInputStream(getMyDir() + "Table column bookmarks.docx")) {
     try (FileInputStream secondStreamIn = new FileInputStream(getMyDir() + "Table column bookmarks.doc")) {
         ComparerContext comparerContext = new ComparerContext();
         comparerContext.getCompareOptions().setIgnoreCaseChanges(true);
         comparerContext.setAuthor("Author");
         comparerContext.setDateTime(new Date());

         try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.CompareContextStreamDocuments.docx")) {
             Comparer.create(comparerContext)
                     .from(firstStreamIn)
                     .from(secondStreamIn)
                     .to(streamOut, SaveFormat.DOCX)
                     .execute();
         }
     }
 }
 
```
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [ComparerContext()](#ComparerContext) | Initialisiert eine neue Instanz dieser Klasse. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getAcceptRevisions()](#getAcceptRevisions) | Gibt an, ob Revisionen in den Dokumenten vor dem Vergleich akzeptiert werden sollen. |
| [getAuthor()](#getAuthor) | Der Autor, der den während des Dokumentvergleichs erstellten Revisionen zugewiesen wird. |
| [getCompareOptions()](#getCompareOptions) | Optionen, die beim Vergleich von Dokumenten verwendet werden. |
| [getDateTime()](#getDateTime) | Das Datum und die Uhrzeit, die den während des Dokumentvergleichs erstellten Revisionen zugewiesen werden. |
| [getFontSettings()](#getFontSettings) | Schrifteinstellungen, die vom Prozessor verwendet werden. |
| [getLayoutOptions()](#getLayoutOptions) | Dokumentenlayout‑Optionen, die vom Prozessor verwendet werden. |
| [getWarningCallback()](#getWarningCallback) | Warn‑Callback, das vom Prozessor verwendet wird. |
| [setAcceptRevisions(boolean value)](#setAcceptRevisions-boolean) | Gibt an, ob Revisionen in den Dokumenten vor dem Vergleich akzeptiert werden sollen. |
| [setAuthor(String value)](#setAuthor-java.lang.String) | Der Autor, der den während des Dokumentvergleichs erstellten Revisionen zugewiesen wird. |
| [setDateTime(Date value)](#setDateTime-java.util.Date) | Das Datum und die Uhrzeit, die den während des Dokumentvergleichs erstellten Revisionen zugewiesen werden. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Schrifteinstellungen, die vom Prozessor verwendet werden. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Warn‑Callback, das vom Prozessor verwendet wird. |
### ComparerContext() {#ComparerContext}
```
public ComparerContext()
```


Initialisiert eine neue Instanz dieser Klasse.

### getAcceptRevisions() {#getAcceptRevisions}
```
public boolean getAcceptRevisions()
```


Gibt an, ob Revisionen in den Dokumenten vor dem Vergleich akzeptiert werden sollen. Wenn die zu vergleichenden Dokumente Revisionen enthalten und dieses Flag auf false gesetzt ist, wird der Prozessor die Revisionen ablehnen. Standard ist  true .

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getAuthor() {#getAuthor}
```
public String getAuthor()
```


Der Autor, der den während des Dokumentvergleichs erstellten Revisionen zugewiesen wird.

**Returns:**
java.lang.String - Der entsprechende java.lang.String-Wert.
### getCompareOptions() {#getCompareOptions}
```
public CompareOptions getCompareOptions()
```


Optionen, die beim Vergleich von Dokumenten verwendet werden.

 **Examples:** 

Zeigt, wie man Dokumente einfach mithilfe von Kontext vergleicht.

```

 // There is a several ways to compare documents:
 String firstDoc = getMyDir() + "Table column bookmarks.docx";
 String secondDoc = getMyDir() + "Table column bookmarks.doc";

 ComparerContext comparerContext = new ComparerContext();
 comparerContext.getCompareOptions().setIgnoreCaseChanges(true);
 comparerContext.setAuthor("Author");
 comparerContext.setDateTime(new Date());

 Comparer.create(comparerContext)
         .from(firstDoc)
         .from(secondDoc)
         .to(getArtifactsDir() + "LowCode.CompareContextDocuments.docx")
         .execute();
 
```

Zeigt, wie man Dokumente aus dem Stream mithilfe von Kontext vergleicht.

```

 // There is a several ways to compare documents from the stream:
 try (FileInputStream firstStreamIn = new FileInputStream(getMyDir() + "Table column bookmarks.docx")) {
     try (FileInputStream secondStreamIn = new FileInputStream(getMyDir() + "Table column bookmarks.doc")) {
         ComparerContext comparerContext = new ComparerContext();
         comparerContext.getCompareOptions().setIgnoreCaseChanges(true);
         comparerContext.setAuthor("Author");
         comparerContext.setDateTime(new Date());

         try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.CompareContextStreamDocuments.docx")) {
             Comparer.create(comparerContext)
                     .from(firstStreamIn)
                     .from(secondStreamIn)
                     .to(streamOut, SaveFormat.DOCX)
                     .execute();
         }
     }
 }
 
```

**Returns:**
[CompareOptions](../../com.aspose.words/compareoptions/) - The corresponding [CompareOptions](../../com.aspose.words/compareoptions/) value.
### getDateTime() {#getDateTime}
```
public Date getDateTime()
```


Das Datum und die Uhrzeit, die den während des Dokumentvergleichs erstellten Revisionen zugewiesen werden.

**Returns:**
java.util.Date - Der entsprechende java.util.Date‑Wert.
### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


Schrifteinstellungen, die vom Prozessor verwendet werden.

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getLayoutOptions() {#getLayoutOptions}
```
public LayoutOptions getLayoutOptions()
```


Dokumentenlayout‑Optionen, die vom Prozessor verwendet werden.

**Returns:**
[LayoutOptions](../../com.aspose.words/layoutoptions/) - The corresponding [LayoutOptions](../../com.aspose.words/layoutoptions/) value.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Warn‑Callback, das vom Prozessor verwendet wird.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setAcceptRevisions(boolean value) {#setAcceptRevisions-boolean}
```
public void setAcceptRevisions(boolean value)
```


Gibt an, ob Revisionen in den Dokumenten vor dem Vergleich akzeptiert werden sollen. Wenn die zu vergleichenden Dokumente Revisionen enthalten und dieses Flag auf false gesetzt ist, wird der Prozessor die Revisionen ablehnen. Standard ist  true .

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setAuthor(String value) {#setAuthor-java.lang.String}
```
public void setAuthor(String value)
```


Der Autor, der den während des Dokumentvergleichs erstellten Revisionen zugewiesen wird.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setDateTime(Date value) {#setDateTime-java.util.Date}
```
public void setDateTime(Date value)
```


Das Datum und die Uhrzeit, die den während des Dokumentvergleichs erstellten Revisionen zugewiesen werden.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.util.Date | Der entsprechende java.util.Date-Wert. |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


Schrifteinstellungen, die vom Prozessor verwendet werden.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | Der entsprechende [FontSettings](../../com.aspose.words/fontsettings/) Wert. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Warn‑Callback, das vom Prozessor verwendet wird.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | Der entsprechende [IWarningCallback](../../com.aspose.words/iwarningcallback/) Wert. |

