---
title: Class XmlDataSource
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Reporting.XmlDataSource klas. Bietet Zugriff auf Daten einer XMLDatei oder eines XMLStreams zur Verwendung in einem Bericht.
type: docs
weight: 4750
url: /de/net/aspose.words.reporting/xmldatasource/
---
## XmlDataSource class

Bietet Zugriff auf Daten einer XML-Datei oder eines XML-Streams zur Verwendung in einem Bericht.

Um mehr zu erfahren, besuchen Sie die[LINQ-Reporting-Engine](https://docs.aspose.com/words/net/linq-reporting-engine/) Dokumentationsartikel.

```csharp
public class XmlDataSource
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [XmlDataSource](xmldatasource/#constructor)(Stream) | Erstellt eine neue Datenquelle mit Daten aus einem XML-Stream unter Verwendung der Standardoptionen für das Laden von XML-Daten. |
| [XmlDataSource](xmldatasource/#constructor_4)(string) | Erstellt eine neue Datenquelle mit Daten aus einer XML-Datei unter Verwendung der Standardoptionen für das Laden von XML-Daten. |
| [XmlDataSource](xmldatasource/#constructor_2)(Stream, Stream) | Erstellt eine neue Datenquelle mit Daten aus einem XML-Stream unter Verwendung eines XML-Schemadefinitions-Streams. Standardoptionen werden für das Laden von XML-Daten verwendet. |
| [XmlDataSource](xmldatasource/#constructor_1)(Stream, XmlDataLoadOptions) | Erstellt eine neue Datenquelle mit Daten aus einem XML-Stream unter Verwendung der angegebenen Optionen für das Laden von XML-Daten. |
| [XmlDataSource](xmldatasource/#constructor_6)(string, string) | Erstellt eine neue Datenquelle mit Daten aus einer XML-Datei mithilfe einer XML-Schemadefinitionsdatei. Standardoptionen werden für das Laden von XML-Daten verwendet. |
| [XmlDataSource](xmldatasource/#constructor_5)(string, XmlDataLoadOptions) | Erstellt eine neue Datenquelle mit Daten aus einer XML-Datei unter Verwendung der angegebenen Optionen für das Laden von XML-Daten. |
| [XmlDataSource](xmldatasource/#constructor_3)(Stream, Stream, XmlDataLoadOptions) | Erstellt eine neue Datenquelle mit Daten aus einem XML-Stream unter Verwendung eines XML-Schemadefinitions-Streams. Die angegebenen -Optionen werden zum Laden von XML-Daten verwendet. |
| [XmlDataSource](xmldatasource/#constructor_7)(string, string, XmlDataLoadOptions) | Erstellt eine neue Datenquelle mit Daten aus einer XML-Datei mithilfe einer XML-Schemadefinitionsdatei. Die angegebenen -Optionen werden zum Laden von XML-Daten verwendet. |

### Bemerkungen

Um beim Erstellen eines Berichts auf Daten der entsprechenden Datei oder des entsprechenden Streams zuzugreifen, übergeben Sie eine Instanz dieser Klasse als eine Datenquelle an eine von[`ReportingEngine`](../reportingengine/) .BuildReport-Überladungen.

Wenn in Vorlagendokumenten ein XML-Element der obersten Ebene nur eine Liste von Elementen desselben Typs enthält, an`XmlDataSource` Die Instanz sollte genauso behandelt werden, als wäre sie aDataTable Instanz. Ansonsten ein`XmlDataSource` Die Instanz sollte genauso behandelt werden, als wäre sie aDataRow Instanz. Weitere Informationen finden Sie in der Vorlagensyntaxreferenz (https://docs.aspose.com/display/wordsnet/Template+Syntax).

Wenn die XML-Schemadefinition an einen Konstruktor dieser Klasse übergeben wird, werden Datentypen von Werten einfacher XML-Elemente und Attribute gemäß dem Schema bestimmt. In Vorlagendokumenten können Sie also mit typisierten Werten und nicht nur mit Zeichenfolgen arbeiten.

Wenn die XML-Schemadefinition nicht an einen Konstruktor dieser Klasse übergeben wird, werden Datentypen von Werten einfacher XML-Elemente und Attribute automatisch anhand ihrer Zeichenfolgendarstellungen bestimmt. In Vorlagendokumenten können Sie also auch in diesem Fall mit typisierten Werten arbeiten. Die Engine ist in der Lage, Werte der folgenden Typen automatisch zu erkennen:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Beachten Sie, dass für eine funktionierende automatische Erkennung von Datentypen Zeichenfolgendarstellungen von Werten einfacher XML-Elemente und Attribute mithilfe invarianter Kultureinstellungen gebildet werden sollten.

Um das Standardverhalten beim Laden von XML-Daten zu überschreiben, initialisieren und übergeben Sie a[`XmlDataLoadOptions`](../xmldataloadoptions/) Instanz zu einem Konstruktor dieser Klasse.

### Siehe auch

* namensraum [Aspose.Words.Reporting](../../aspose.words.reporting/)
* Montage [Aspose.Words](../../)


