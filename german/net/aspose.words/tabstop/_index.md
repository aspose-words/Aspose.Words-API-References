---
title: Class TabStop
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.TabStop klas. Stellt einen einzelnen benutzerdefinierten Tabstopp dar. DerTabStopObjekt ist Mitglied von the TabStopCollection Sammlung.
type: docs
weight: 6200
url: /de/net/aspose.words/tabstop/
---
## TabStop class

Stellt einen einzelnen benutzerdefinierten Tabstopp dar. Der`TabStop`Objekt ist Mitglied von the [`TabStopCollection`](../tabstopcollection/) Sammlung.

Um mehr zu erfahren, besuchen Sie die[Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) Dokumentationsartikel.

```csharp
public sealed class TabStop
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [TabStop](tabstop/#constructor)(double) | Initialisiert eine neue Instanz dieser Klasse. |
| [TabStop](tabstop/#constructor_1)(double, TabAlignment, TabLeader) | Initialisiert eine neue Instanz dieser Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Alignment](../../aspose.words/tabstop/alignment/) { get; set; } | Ruft die Textausrichtung an diesem Tabstopp ab oder legt diese fest. |
| [IsClear](../../aspose.words/tabstop/isclear/) { get; } | Gibt zurück`WAHR` wenn dieser Tabstopp alle vorhandenen Tabstopps an dieser Position löscht. |
| [Leader](../../aspose.words/tabstop/leader/) { get; set; } | Ruft den Typ der Führungslinie ab, die unter dem Tabulatorzeichen angezeigt wird, oder legt diesen fest. |
| [Position](../../aspose.words/tabstop/position/) { get; } | Ermittelt die Position des Tabstopps in Punkten. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Equals](../../aspose.words/tabstop/equals/#equals)(TabStop) | Vergleicht mit dem angegebenen`TabStop` . |
| override [GetHashCode](../../aspose.words/tabstop/gethashcode/)() | Berechnet den Hash-Code für dieses Objekt. |

### Bemerkungen

Normalerweise gibt ein Tabstopp eine Position an, an der ein Tabstopp vorhanden ist. Da Tabstopps jedoch von übergeordneten Stilen geerbt werden können, muss das untergeordnete Objekt möglicherweise explizit definieren, dass an einer bestimmten Position kein Tabstopp vorhanden ist. Um einen geerbten Tabstopp an einer bestimmten Position zu löschen, erstellen Sie einen`TabStop` Objekt und set [`Alignment`](./alignment/) ZuClear.

Weitere Informationen finden Sie unter[`TabStopCollection`](../tabstopcollection/).

### Beispiele

Zeigt, wie die Position des rechten Tabstopps in Inhaltsverzeichnis-bezogenen Absätzen geändert wird.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// Alle Absätze mit TOC-ergebnisbasierten Stilen durchlaufen; Dies ist jeder Stil zwischen TOC und TOC9.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // Holen Sie sich den ersten Tab, der in diesem Absatz verwendet wird. Dies sollte der Tab sein, der zum Ausrichten der Seitenzahlen verwendet wird.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // Ersetzen Sie den ersten Standard-Tabstopp durch einen benutzerdefinierten Tabstopp.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


