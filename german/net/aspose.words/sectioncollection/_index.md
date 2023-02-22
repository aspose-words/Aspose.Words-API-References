---
title: Class SectionCollection
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.SectionCollection klas. Eine Sammlung von Abschnitt Objekte im Dokument.
type: docs
weight: 5450
url: /de/net/aspose.words/sectioncollection/
---
## SectionCollection class

Eine Sammlung von **Abschnitt** Objekte im Dokument.

```csharp
public class SectionCollection : NodeCollection
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Ruft die Anzahl der Knoten in der Sammlung ab. |
| [Item](../../aspose.words/sectioncollection/item/) { get; } | Ruft einen Abschnitt am angegebenen Index ab. (2 indexers) |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(Node) | Fügt am Ende der Sammlung einen Knoten hinzu. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Entfernt alle Knoten aus dieser Sammlung und aus dem Dokument. |
| [Contains](../../aspose.words/nodecollection/contains/)(Node) | Bestimmt, ob sich ein Knoten in der Sammlung befindet. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Bietet eine einfache Iteration im "foreach"-Stil über die Sammlung von Knoten. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(Node) | Gibt den nullbasierten Index des angegebenen Knotens zurück. |
| [Insert](../../aspose.words/nodecollection/insert/)(int, Node) | Fügt am angegebenen Index einen Knoten in die Sammlung ein. |
| [Remove](../../aspose.words/nodecollection/remove/)(Node) | Entfernt den Knoten aus der Sammlung und aus dem Dokument. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int) | Entfernt den Knoten am angegebenen Index aus der Sammlung und aus dem Dokument. |
| [ToArray](../../aspose.words/sectioncollection/toarray/#toarray_1)() | Kopiert alle Abschnitte aus der Sammlung in ein neues Array von Abschnitten. (2 methods) |

### Bemerkungen

Ein Microsoft Word-Dokument kann mehrere Abschnitte enthalten. Um einen Abschnitt in Microsoft Word zu erstellen, wählen Sie den Befehl Einfügen/Umbruch und wählen Sie einen Umbruchtyp aus. Der Umbruch gibt an, ob section auf einer neuen Seite oder auf derselben Seite beginnt.

Das programmgesteuerte Einfügen und Entfernen von Abschnitten kann verwendet werden, um während des Seriendrucks produzierte Dokumente anzupassen. Wenn ein Dokument je nach bestimmten Kriterien einen anderen Inhalt oder Teile des -Inhalts haben muss, können Sie ein „Master“-Dokument erstellen, das mehrere Abschnitte enthält, und einige der Abschnitte vor oder nach dem Seriendruck löschen.

### Beispiele

Zeigt, wie Abschnitte in einem Dokument hinzugefügt und entfernt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

// Den ersten Abschnitt aus dem Dokument löschen.
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// Eine Kopie des jetzt ersten Abschnitts an das Ende des Dokuments anhängen.
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

### Siehe auch

* class [NodeCollection](../nodecollection/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


