---
title: VariableCollection Class
linktitle: VariableCollection
articleTitle: VariableCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.VariableCollection, verwalten und passen Sie Dokumentvariablen effizient an, um die Dokumentautomatisierung und Flexibilität zu verbessern.
type: docs
weight: 7380
url: /de/net/aspose.words/variablecollection/
---
## VariableCollection class

Eine Sammlung von Dokumentvariablen.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Dokumenteigenschaften](https://docs.aspose.com/words/net/work-with-document-properties/) Dokumentationsartikel.

```csharp
public class VariableCollection : IEnumerable<KeyValuePair<string, string>>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words/variablecollection/count/) { get; } | Ruft die Anzahl der in der Sammlung enthaltenen Elemente ab. |
| [Item](../../aspose.words/variablecollection/item/) { get; set; } | Ruft eine Dokumentvariable über den Namen ab oder legt sie fest (ohne Berücksichtigung der Groß-/Kleinschreibung). `null`Werte sind auf der rechten Seite der Zuweisung nicht zulässig und werden durch einen leeren String ersetzt. (2 indexers) |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words/variablecollection/add/)(*string, string*) | Fügt der Sammlung eine Dokumentvariable hinzu. |
| [Clear](../../aspose.words/variablecollection/clear/)() | Entfernt alle Elemente aus der Sammlung. |
| [Contains](../../aspose.words/variablecollection/contains/)(*string*) | Bestimmt, ob die Sammlung eine Dokumentvariable mit dem angegebenen Namen enthält. |
| [GetEnumerator](../../aspose.words/variablecollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück, mit dem alle Variablen in der Sammlung durchlaufen werden können. |
| [IndexOfKey](../../aspose.words/variablecollection/indexofkey/)(*string*) | Gibt den nullbasierten Index der angegebenen Dokumentvariable in der Sammlung zurück. |
| [Remove](../../aspose.words/variablecollection/remove/)(*string*) | Entfernt eine Dokumentvariable mit dem angegebenen Namen aus der Sammlung. |
| [RemoveAt](../../aspose.words/variablecollection/removeat/)(*int*) | Entfernt eine Dokumentvariable am angegebenen Index. |

## Bemerkungen

Variablennamen und -werte sind Zeichenfolgen.

Bei Variablennamen wird die Groß- und Kleinschreibung nicht berücksichtigt.

## Beispiele

Zeigt, wie mit der Variablensammlung eines Dokuments gearbeitet wird.

```csharp
Document doc = new Document();
VariableCollection variables = doc.Variables;

// Jedes Dokument verfügt über eine Sammlung von Schlüssel-/Wertpaarvariablen, denen wir Elemente hinzufügen können.
variables.Add("Home address", "123 Main St.");
variables.Add("City", "London");
variables.Add("Bedrooms", "3");

Assert.AreEqual(3, variables.Count);

// Wir können die Werte von Variablen im Dokumenttext mithilfe von DOCVARIABLE-Feldern anzeigen.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocVariable field = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
field.VariableName = "Home address";
field.Update();

Assert.AreEqual("123 Main St.", field.Result);

// Durch die Zuweisung von Werten zu vorhandenen Schlüsseln werden diese aktualisiert.
variables.Add("Home address", "456 Queen St.");

// Wir müssen dann die DOCVARIABLE-Felder aktualisieren, um sicherzustellen, dass sie einen aktuellen Wert anzeigen.
Assert.AreEqual("123 Main St.", field.Result);

field.Update();

Assert.AreEqual("456 Queen St.", field.Result);

// Überprüfen Sie, ob die Dokumentvariablen mit einem bestimmten Namen oder Wert vorhanden sind.
Assert.True(variables.Contains("City"));
Assert.True(variables.Any(v => v.Value == "London"));

// Die Variablensammlung sortiert Variablen automatisch alphabetisch nach Namen.
Assert.AreEqual(0, variables.IndexOfKey("Bedrooms"));
Assert.AreEqual(1, variables.IndexOfKey("City"));
Assert.AreEqual(2, variables.IndexOfKey("Home address"));

Assert.AreEqual("3", variables[0]);
Assert.AreEqual("London", variables["City"]);

// Aufzählung der Variablensammlung.
using (IEnumerator<KeyValuePair<string, string>> enumerator = doc.Variables.GetEnumerator())
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: {enumerator.Current.Key}, Value: {enumerator.Current.Value}");

// Unten sind drei Möglichkeiten zum Entfernen von Dokumentvariablen aus einer Sammlung aufgeführt.
// 1 - Nach Namen:
variables.Remove("City");

Assert.False(variables.Contains("City"));

// 2 - Nach Index:
variables.RemoveAt(1);

Assert.False(variables.Contains("Home address"));

// 3 - Die gesamte Sammlung auf einmal löschen:
variables.Clear();

Assert.AreEqual(0, variables.Count);
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
