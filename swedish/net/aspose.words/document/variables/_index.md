---
title: Document.Variables
second_title: Aspose.Words för .NET API Referens
description: Document fast egendom. Returnerar samlingen av variabler som lagts till i ett dokument eller mall.
type: docs
weight: 420
url: /sv/net/aspose.words/document/variables/
---
## Document.Variables property

Returnerar samlingen av variabler som lagts till i ett dokument eller mall.

```csharp
public VariableCollection Variables { get; }
```

### Exempel

Visar hur man arbetar med ett dokuments variabelsamling.

```csharp
Document doc = new Document();
VariableCollection variables = doc.Variables;

// Varje dokument har en samling nyckel-/värdeparvariabler som vi kan lägga till objekt till.
variables.Add("Home address", "123 Main St.");
variables.Add("City", "London");
variables.Add("Bedrooms", "3");

Assert.AreEqual(3, variables.Count);

// Vi kan visa värdena för variabler i dokumentets brödtext med hjälp av DOCVARIABLE-fält.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocVariable field = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
field.VariableName = "Home address";
field.Update();

Assert.AreEqual("123 Main St.", field.Result);

// Att tilldela värden till befintliga nycklar kommer att uppdatera dem.
variables.Add("Home address", "456 Queen St.");

// Vi måste då uppdatera DOCVARIABLE-fält för att säkerställa att de visar ett aktuellt värde.
Assert.AreEqual("123 Main St.", field.Result);

field.Update();

Assert.AreEqual("456 Queen St.", field.Result);

// Verifiera att dokumentvariablerna med ett visst namn eller värde finns.
Assert.True(variables.Contains("City"));
Assert.True(variables.Any(v => v.Value == "London"));

// Samlingen av variabler sorterar automatiskt variabler alfabetiskt efter namn.
Assert.AreEqual(0, variables.IndexOfKey("Bedrooms"));
Assert.AreEqual(1, variables.IndexOfKey("City"));
Assert.AreEqual(2, variables.IndexOfKey("Home address"));

// Räkna upp över samlingen av variabler.
using (IEnumerator<KeyValuePair<string, string>> enumerator = doc.Variables.GetEnumerator())
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: {enumerator.Current.Key}, Value: {enumerator.Current.Value}");

// Nedan finns tre sätt att ta bort dokumentvariabler från en samling.
// 1 - Efter namn:
variables.Remove("City");

Assert.False(variables.Contains("City"));

// 2 - Efter index:
variables.RemoveAt(1);

Assert.False(variables.Contains("Home address"));

// 3 - Rensa hela samlingen på en gång:
variables.Clear();

Assert.That(variables, Is.Empty);
```

### Se även

* class [VariableCollection](../../variablecollection/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../document/)
* hopsättning [Aspose.Words](../../../)


