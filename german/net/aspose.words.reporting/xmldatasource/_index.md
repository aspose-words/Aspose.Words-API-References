---
title: XmlDataSource Class
linktitle: XmlDataSource
articleTitle: XmlDataSource
second_title: Aspose.Words für .NET
description: Nutzen Sie leistungsstarke Berichte mit Aspose.Words.XmlDataSource. Greifen Sie einfach auf XML-Daten zu, um sie nahtlos in Ihre Berichte zu integrieren und die Datenvisualisierung zu verbessern.
type: docs
weight: 5490
url: /de/net/aspose.words.reporting/xmldatasource/
---
## XmlDataSource class

Bietet Zugriff auf Daten einer XML-Datei oder eines XML-Streams zur Verwendung in einem Bericht.

Um mehr zu erfahren, besuchen Sie die[LINQ-Berichtsmodul](https://docs.aspose.com/words/net/linq-reporting-engine/) Dokumentationsartikel.

```csharp
public class XmlDataSource
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [XmlDataSource](xmldatasource/#constructor)(*Stream*) | Erstellt eine neue Datenquelle mit Daten aus einem XML-Stream unter Verwendung der Standardoptionen zum Laden von XML-Daten. |
| [XmlDataSource](xmldatasource/#constructor_4)(*string*) | Erstellt eine neue Datenquelle mit Daten aus einer XML-Datei unter Verwendung der Standardoptionen zum Laden von XML-Daten. |
| [XmlDataSource](xmldatasource/#constructor_2)(*Stream, Stream*) | Erstellt eine neue Datenquelle mit Daten aus einem XML-Stream unter Verwendung eines XML-Schemadefinitionsstreams. Zum Laden der XML-Daten werden die Standardoptionen verwendet. |
| [XmlDataSource](xmldatasource/#constructor_1)(*Stream, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Erstellt eine neue Datenquelle mit Daten aus einem XML-Stream unter Verwendung der angegebenen Optionen zum Laden von XML-Daten. |
| [XmlDataSource](xmldatasource/#constructor_6)(*string, string*) | Erstellt eine neue Datenquelle mit Daten aus einer XML-Datei unter Verwendung einer XML-Schemadefinitionsdatei. Zum Laden von XML-Daten werden die Standardoptionen verwendet. |
| [XmlDataSource](xmldatasource/#constructor_5)(*string, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Erstellt eine neue Datenquelle mit Daten aus einer XML-Datei unter Verwendung der angegebenen Optionen zum Laden von XML-Daten. |
| [XmlDataSource](xmldatasource/#constructor_3)(*Stream, Stream, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Erstellt eine neue Datenquelle mit Daten aus einem XML-Stream unter Verwendung eines XML-Schemadefinitionsstreams. Die angegebenen Optionen werden zum Laden der XML-Daten verwendet. |
| [XmlDataSource](xmldatasource/#constructor_7)(*string, string, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Erstellt eine neue Datenquelle mit Daten aus einer XML-Datei unter Verwendung einer XML-Schemadefinitionsdatei. Die angegebenen Optionen werden zum Laden der XML-Daten verwendet. |

## Bemerkungen

Um beim Generieren eines Berichts auf die Daten der entsprechenden Datei oder des Streams zuzugreifen, übergeben Sie eine Instanz dieser Klasse als eine Datenquelle an einen der[`ReportingEngine`](../reportingengine/) .BuildReport-Überladungen.

Wenn in Vorlagendokumenten ein XML-Element der obersten Ebene nur eine Liste von Elementen desselben Typs enthält, ein`XmlDataSource` Instanz sollte genauso behandelt werden, als wäre sie aDataTable -Instanz. Andernfalls wird eine`XmlDataSource` Instanz sollte genauso behandelt werden, als wäre sie aDataRow -Instanz. Weitere Informationen finden Sie in der Vorlagensyntaxreferenz (https://docs.aspose.com/display/wordsnet/Template+Syntax).

Wenn die XML-Schemadefinition an einen Konstruktor dieser Klasse übergeben wird, werden die Datentypen der Werte einfacher XML-Elemente und Attribute entsprechend dem Schema bestimmt. So können Sie in Vorlagendokumenten mit typisierten Werten statt nur mit Zeichenfolgen arbeiten.

Wenn die XML-Schemadefinition nicht an einen Konstruktor dieser Klasse übergeben wird, werden die Datentypen der Werte einfacher XML-Elemente und Attribute automatisch anhand ihrer String-Darstellungen bestimmt. Daher können Sie in Vorlagendokumenten auch in diesem Fall mit typisierten Werten arbeiten. Die Engine kann Werte der folgenden Typen automatisch erkennen:

* Nullable
* Nullable
* Nullable
* Nullable
* String

Beachten Sie, dass für eine funktionierende automatische Erkennung von Datentypen die Zeichenfolgendarstellungen der Werte einfacher XML-Elemente und Attribute unter Verwendung invarianter Kultureinstellungen erstellt werden sollten.

Um das Standardverhalten des XML-Datenladens zu überschreiben, initialisieren und übergeben Sie ein[`XmlDataLoadOptions`](../xmldataloadoptions/) Instanz an einen Konstruktor dieser Klasse.

## Beispiele

Zeigen Sie, wie XML als Datenquelle (Zeichenfolge) verwendet wird.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

XmlDataSource dataSource = new XmlDataSource(MyDir + "List of people.xml");
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataString.docx");
```

Zeigen Sie, wie XML als Datenquelle (Stream) verwendet wird.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

using (FileStream stream = File.OpenRead(MyDir + "List of people.xml"))
{
    XmlDataSource dataSource = new XmlDataSource(stream);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataStream.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Reporting](../../aspose.words.reporting/)
* Montage [Aspose.Words](../../)
