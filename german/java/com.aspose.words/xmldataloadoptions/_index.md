---
title: "XmlDataLoadOptions"
linktitle: "XmlDataLoadOptions"
second_title: "Aspose.Words für Java"
description: "Stellt Optionen für das Laden von XML-Daten in Java dar."
type: docs
weight: 745
url: /de/java/com.aspose.words/xmldataloadoptions/
---

**Inheritance:**
java.lang.Object
```
public class XmlDataLoadOptions
```

Stellt Optionen für das Laden von XML-Daten dar.

Weitere Informationen finden Sie im Dokumentationsartikel zum [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

Eine Instanz dieser Klasse kann an die Konstruktoren von [XmlDataSource](../../com.aspose.words/xmldatasource/) übergeben werden.


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [XmlDataLoadOptions()](#XmlDataLoadOptions) | Initialisiert eine neue Instanz dieser Klasse mit Standardoptionen. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getAlwaysGenerateRootObject()](#getAlwaysGenerateRootObject) | Liefert ein Flag, das angibt, ob eine erzeugte Datenquelle stets ein Objekt für ein XML-Stammelement enthält. |
| [setAlwaysGenerateRootObject(boolean value)](#setAlwaysGenerateRootObject-boolean) | Setzt ein Flag, das angibt, ob eine erzeugte Datenquelle stets ein Objekt für ein XML-Stammelement enthält. |
### XmlDataLoadOptions() {#XmlDataLoadOptions}
```
public XmlDataLoadOptions()
```


Initialisiert eine neue Instanz dieser Klasse mit Standardoptionen.

### getAlwaysGenerateRootObject() {#getAlwaysGenerateRootObject}
```
public boolean getAlwaysGenerateRootObject()
```


Liefert ein Flag, das angibt, ob eine erzeugte Datenquelle stets ein Objekt für ein XML-Stammelement enthält. Wenn ein XML-Stammelement keine Attribute hat und alle seine Kind-Elemente denselben Namen besitzen, wird ein solches Objekt standardmäßig nicht erstellt.

 **Remarks:** 

Der Standardwert ist  false .

**Returns:**
boolean - Ein Flag, das angibt, ob eine erzeugte Datenquelle stets ein Objekt für ein XML-Stammelement enthält.
### setAlwaysGenerateRootObject(boolean value) {#setAlwaysGenerateRootObject-boolean}
```
public void setAlwaysGenerateRootObject(boolean value)
```


Setzt ein Flag, das angibt, ob eine erzeugte Datenquelle stets ein Objekt für ein XML-Stammelement enthält. Wenn ein XML-Stammelement keine Attribute hat und alle seine Kind-Elemente denselben Namen besitzen, wird ein solches Objekt standardmäßig nicht erstellt.

 **Remarks:** 

Der Standardwert ist  false .

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein Flag, das angibt, ob eine erzeugte Datenquelle stets ein Objekt für ein XML-Stammelement enthält. |

