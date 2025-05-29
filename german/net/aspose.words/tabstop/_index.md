---
title: TabStop Class
linktitle: TabStop
articleTitle: TabStop
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.TabStop, Ihre Lösung für benutzerdefinierte Tabstopps in der Dokumentformatierung. Optimieren Sie Ihre Dokumente präzise und einfach!
type: docs
weight: 7050
url: /de/net/aspose.words/tabstop/
---
## TabStop class

Stellt einen einzelnen benutzerdefinierten Tabstopp dar. Der`TabStop` Objekt ist ein Mitglied von the [`TabStopCollection`](../tabstopcollection/) Sammlung.

Um mehr zu erfahren, besuchen Sie die[Aspose.Words Dokumentobjektmodell (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) Dokumentationsartikel.

```csharp
public sealed class TabStop
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [TabStop](tabstop/#constructor)(*double*) | Initialisiert eine neue Instanz dieser Klasse. |
| [TabStop](tabstop/#constructor_1)(*double, [TabAlignment](../tabalignment/), [TabLeader](../tableader/)*) | Initialisiert eine neue Instanz dieser Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Alignment](../../aspose.words/tabstop/alignment/) { get; set; } | Ruft die Textausrichtung an diesem Tabstopp ab oder legt sie fest. |
| [IsClear](../../aspose.words/tabstop/isclear/) { get; } | Rückgaben`WAHR` wenn dieser Tabstopp alle vorhandenen Tabstopps an dieser Position löscht. |
| [Leader](../../aspose.words/tabstop/leader/) { get; set; } | Ruft den Typ der unter dem Tabulatorzeichen angezeigten Führungslinie ab oder legt ihn fest. |
| [Position](../../aspose.words/tabstop/position/) { get; } | Ruft die Position des Tabulatorstopps in Punkten ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Equals](../../aspose.words/tabstop/equals/#equals)(*TabStop*) | Vergleicht mit dem angegebenen`TabStop` . |
| override [GetHashCode](../../aspose.words/tabstop/gethashcode/)() | Berechnet den Hashcode für dieses Objekt. |

## Bemerkungen

Normalerweise gibt ein Tabstopp die Position an, an der ein Tabstopp vorhanden ist. Da Tabstopps jedoch von übergeordneten Stilen übernommen werden können, muss das untergeordnete Objekt möglicherweise explizit angeben, dass an einer bestimmten Position kein Tabstopp vorhanden ist. Um einen übernommenen Tabstopp an einer bestimmten Position zu löschen, erstellen Sie ein`TabStop` Objekt und set [`Alignment`](./alignment/) ZuClear.

Weitere Informationen finden Sie unter[`TabStopCollection`](../tabstopcollection/).

## Beispiele

Zeigt, wie die Position des rechten Tabstopps in Inhaltsverzeichnis-bezogenen Absätzen geändert wird.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// Durchlaufe alle Absätze mit auf dem Inhaltsverzeichnisergebnis basierenden Stilen. Dies ist jeder Stil zwischen Inhaltsverzeichnis und Inhaltsverzeichnis9.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // Holen Sie sich den ersten Tabulator, der in diesem Absatz verwendet wird. Dies sollte der Tabulator sein, der zum Ausrichten der Seitenzahlen verwendet wird.
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
