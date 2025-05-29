---
title: ReportingEngine Class
linktitle: ReportingEngine
articleTitle: ReportingEngine
second_title: Aspose.Words für .NET
description: Nutzen Sie die leistungsstarke Dokumentenautomatisierung mit Aspose.Words.ReportingEngine. Füllen Sie Vorlagen einfach mit Daten und passen Sie die Einstellungen für nahtlose Berichte an.
type: docs
weight: 5470
url: /de/net/aspose.words.reporting/reportingengine/
---
## ReportingEngine class

Bietet Routinen zum Füllen von Vorlagendokumenten mit Daten und eine Reihe von Einstellungen zum Steuern dieser Routinen.

Um mehr zu erfahren, besuchen Sie die[LINQ-Berichtsmodul](https://docs.aspose.com/words/net/linq-reporting-engine/) Dokumentationsartikel.

```csharp
public class ReportingEngine
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [ReportingEngine](reportingengine/)() | Initialisiert eine neue Instanz dieser Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [KnownTypes](../../aspose.words.reporting/reportingengine/knowntypes/) { get; } | Ruft einen ungeordneten Satz (d. h. eine Sammlung eindeutiger Elemente) ab, der enthältType Objekte , deren vollständig oder teilweise qualifizierte Namen in Berichtsvorlagen verwendet werden können, die von dieser Engine -Instanz verarbeitet werden, um die statischen Mitglieder der entsprechenden Typen aufzurufen, Typumwandlungen durchzuführen usw. |
| [MissingMemberMessage](../../aspose.words.reporting/reportingengine/missingmembermessage/) { get; set; } | Ruft einen Zeichenfolgenwert ab oder legt ihn fest, der anstelle eines Vorlagenausdrucks ausgegeben wird und einen einfachen Verweis auf ein fehlendes Element eines Objekts darstellt. Der Standardwert ist eine leere Zeichenfolge. |
| [Options](../../aspose.words.reporting/reportingengine/options/) { get; set; } | Ruft eine Reihe von Flags ab oder setzt diese, die das Verhalten dieses`ReportingEngine` Instanz beim Erstellen eines Berichts. |
| static [UseReflectionOptimization](../../aspose.words.reporting/reportingengine/usereflectionoptimization/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der angibt, ob Aufrufe von benutzerdefinierten Typmembern über die Reflection-API mithilfe der dynamischen Klassengenerierung optimiert werden. Der Standardwert ist`WAHR` . |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport)(*[Document](../../aspose.words/document/), object*) | Füllt das angegebene Vorlagendokument mit Daten aus der angegebenen Quelle und macht daraus einen fertigen Bericht. |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport_1)(*[Document](../../aspose.words/document/), object, string*) | Füllt das angegebene Vorlagendokument mit Daten aus der angegebenen Quelle und macht daraus einen fertigen Bericht. |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport_2)(*[Document](../../aspose.words/document/), object[], string[]*) | Füllt das angegebene Vorlagendokument mit Daten aus den angegebenen Quellen und macht daraus einen fertigen Bericht. |
| static [GetRestrictedTypes](../../aspose.words.reporting/reportingengine/getrestrictedtypes/)() | Gibt Typen zurück, deren Mitglieder sowie Mitglieder abgeleiteter Typen für die Engine aufgrund der Vorlagensyntax unzugänglich sein sollten. |
| static [SetRestrictedTypes](../../aspose.words.reporting/reportingengine/setrestrictedtypes/)(*params Type[]*) | Gibt Typen an, deren Mitglieder sowie Mitglieder abgeleiteter Typen für die Engine über die Vorlagensyntax nicht zugänglich sein sollen. |

### Siehe auch

* namensraum [Aspose.Words.Reporting](../../aspose.words.reporting/)
* Montage [Aspose.Words](../../)
