---
title: VariableCollection.Contains
second_title: Aspose.Words für .NET-API-Referenz
description: VariableCollection methode. Ermittelt ob die Sammlung eine Dokumentvariable mit dem angegebenen Namen enthält.
type: docs
weight: 50
url: /de/net/aspose.words/variablecollection/contains/
---
## VariableCollection.Contains method

Ermittelt, ob die Sammlung eine Dokumentvariable mit dem angegebenen Namen enthält.

```csharp
public bool Contains(string name)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | String | Der Name der zu suchenden Dokumentvariablen unterscheidet nicht zwischen Groß- und Kleinschreibung. |

### Rückgabewert

`WAHR` wenn Artikel in der Sammlung gefunden wird; ansonsten,`FALSCH`.

### Beispiele

Zeigt, wie mit der Variablensammlung eines Dokuments gearbeitet wird.

```csharp
Document doc = new Document();
VariableCollection variables = doc.Variables;

// Jedes Dokument verfügt über eine Sammlung von Schlüssel/Wert-Paarvariablen, zu denen wir Elemente hinzufügen können.
variables.Add("Home address", "123 Main St.");
variables.Add("City", "London");
variables.Add("Bedrooms", "3");

Assert.AreEqual(3, variables.Count);

// Wir können die Werte von Variablen im Dokumentkörper mithilfe von DOCVARIABLE-Feldern anzeigen.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocVariable field = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
field.VariableName = "Home address";
field.Update();

Assert.AreEqual("123 Main St.", field.Result);

// Durch Zuweisen von Werten zu vorhandenen Schlüsseln werden diese aktualisiert.
variables.Add("Home address", "456 Queen St.");

// Wir müssen dann die DOCVARIABLE-Felder aktualisieren, um sicherzustellen, dass sie einen aktuellen Wert anzeigen.
Assert.AreEqual("123 Main St.", field.Result);

field.Update();

Assert.AreEqual("456 Queen St.", field.Result);

// Überprüfen Sie, ob die Dokumentvariablen mit einem bestimmten Namen oder Wert vorhanden sind.
Assert.True(variables.Contains("City"));
Assert.True(variables.Any(v => v.Value == "London"));

// Die Sammlung von Variablen sortiert Variablen automatisch alphabetisch nach Namen.
Assert.AreEqual(0, variables.IndexOfKey("Bedrooms"));
Assert.AreEqual(1, variables.IndexOfKey("City"));
Assert.AreEqual(2, variables.IndexOfKey("Home address"));

// Über die Sammlung von Variablen aufzählen.
using (IEnumerator<KeyValuePair<string, string>> enumerator = doc.Variables.GetEnumerator())
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: {enumerator.Current.Key}, Value: {enumerator.Current.Value}");

// Im Folgenden finden Sie drei Möglichkeiten zum Entfernen von Dokumentvariablen aus einer Sammlung.
// 1 - Nach Namen:
variables.Remove("City");

Assert.False(variables.Contains("City"));

// 2 - Nach Index:
variables.RemoveAt(1);

Assert.False(variables.Contains("Home address"));

// 3 – Die gesamte Sammlung auf einmal löschen:
variables.Clear();

Assert.That(variables, Is.Empty);
```

### Siehe auch

* class [VariableCollection](../)
* namensraum [Aspose.Words](../../variablecollection/)
* Montage [Aspose.Words](../../../)


