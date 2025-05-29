---
title: VariableCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words für .NET
description: Verwalten Sie Dokumentvariablen mühelos mit VariableCollection Item. Legen Sie Namen ohne Berücksichtigung der Groß- und Kleinschreibung fest oder rufen Sie sie ab. Nullwerte sind nicht zulässig, um die Datenintegrität zu gewährleisten.
type: docs
weight: 20
url: /de/net/aspose.words/variablecollection/item/
---
## VariableCollection indexer (1 of 2)

Ruft eine Dokumentvariable über den Namen ab oder legt sie fest (ohne Berücksichtigung der Groß-/Kleinschreibung). `null`Werte sind auf der rechten Seite der Zuweisung nicht zulässig und werden durch einen leeren String ersetzt.

```csharp
public string this[string name] { get; set; }
```

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

* class [VariableCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## VariableCollection indexer (2 of 2)

Ruft eine Dokumentvariable am angegebenen Index ab oder legt sie fest. `null`Werte sind auf der rechten Seite der Zuweisung nicht zulässig und werden durch einen leeren String ersetzt.

```csharp
public string this[int index] { get; set; }
```

| Parameter | Beschreibung |
| --- | --- |
| index | Nullbasierter Index der Dokumentvariable. |

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

* class [VariableCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
