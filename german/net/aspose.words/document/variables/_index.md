---
title: Document.Variables
linktitle: Variables
articleTitle: Variables
second_title: Aspose.Words für .NET
description: Entdecken Sie Dokumentvariablen. Greifen Sie auf eine leistungsstarke Sammlung anpassbarer Variablen für Ihre Dokumente und Vorlagen zu und steigern Sie so Effizienz und Flexibilität.
type: docs
weight: 460
url: /de/net/aspose.words/document/variables/
---
## Document.Variables property

Gibt die Sammlung der Variablen zurück, die einem Dokument oder einer Vorlage hinzugefügt wurden.

```csharp
public VariableCollection Variables { get; }
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

* class [VariableCollection](../../variablecollection/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
