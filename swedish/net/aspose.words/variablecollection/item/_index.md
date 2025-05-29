---
title: VariableCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: Hantera dokumentvariabler enkelt med VariableCollection Item. Ange eller hämta namn som inte är skiftlägeskänsliga – inga nullvärden är tillåtna, vilket säkerställer dataintegritet.
type: docs
weight: 20
url: /sv/net/aspose.words/variablecollection/item/
---
## VariableCollection indexer (1 of 2)

Hämtar eller anger en dokumentvariabel med det skiftlägeskänsliga namnet. `null`värden är inte tillåtna som höger sida av uppgiften och kommer att ersättas med en tom sträng.

```csharp
public string this[string name] { get; set; }
```

## Exempel

Visar hur man arbetar med ett dokuments variabelsamling.

```csharp
Document doc = new Document();
VariableCollection variables = doc.Variables;

// Varje dokument har en samling av nyckel/värde-parvariabler, som vi kan lägga till objekt till.
variables.Add("Home address", "123 Main St.");
variables.Add("City", "London");
variables.Add("Bedrooms", "3");

Assert.AreEqual(3, variables.Count);

// Vi kan visa värdena för variabler i dokumentets innehåll med hjälp av DOCVARIABLE-fält.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocVariable field = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
field.VariableName = "Home address";
field.Update();

Assert.AreEqual("123 Main St.", field.Result);

// Att tilldela värden till befintliga nycklar kommer att uppdatera dem.
variables.Add("Home address", "456 Queen St.");

// Vi måste sedan uppdatera DOCVARIABLE-fälten för att säkerställa att de visar ett aktuellt värde.
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

Assert.AreEqual("3", variables[0]);
Assert.AreEqual("London", variables["City"]);

// Räkna upp över samlingen av variabler.
using (IEnumerator<KeyValuePair<string, string>> enumerator = doc.Variables.GetEnumerator())
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: {enumerator.Current.Key}, Value: {enumerator.Current.Value}");

// Nedan följer tre sätt att ta bort dokumentvariabler från en samling.
// 1 - Efter namn:
variables.Remove("City");

Assert.False(variables.Contains("City"));

// 2 - Enligt index:
variables.RemoveAt(1);

Assert.False(variables.Contains("Home address"));

// 3 - Rensa hela samlingen på en gång:
variables.Clear();

Assert.AreEqual(0, variables.Count);
```

### Se även

* class [VariableCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## VariableCollection indexer (2 of 2)

Hämtar eller ställer in en dokumentvariabel vid det angivna indexet. `null`värden är inte tillåtna som höger sida av uppgiften och kommer att ersättas med en tom sträng.

```csharp
public string this[int index] { get; set; }
```

| Parameter | Beskrivning |
| --- | --- |
| index | Nollbaserat index för dokumentvariabeln. |

## Exempel

Visar hur man arbetar med ett dokuments variabelsamling.

```csharp
Document doc = new Document();
VariableCollection variables = doc.Variables;

// Varje dokument har en samling av nyckel/värde-parvariabler, som vi kan lägga till objekt till.
variables.Add("Home address", "123 Main St.");
variables.Add("City", "London");
variables.Add("Bedrooms", "3");

Assert.AreEqual(3, variables.Count);

// Vi kan visa värdena för variabler i dokumentets innehåll med hjälp av DOCVARIABLE-fält.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocVariable field = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
field.VariableName = "Home address";
field.Update();

Assert.AreEqual("123 Main St.", field.Result);

// Att tilldela värden till befintliga nycklar kommer att uppdatera dem.
variables.Add("Home address", "456 Queen St.");

// Vi måste sedan uppdatera DOCVARIABLE-fälten för att säkerställa att de visar ett aktuellt värde.
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

Assert.AreEqual("3", variables[0]);
Assert.AreEqual("London", variables["City"]);

// Räkna upp över samlingen av variabler.
using (IEnumerator<KeyValuePair<string, string>> enumerator = doc.Variables.GetEnumerator())
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: {enumerator.Current.Key}, Value: {enumerator.Current.Value}");

// Nedan följer tre sätt att ta bort dokumentvariabler från en samling.
// 1 - Efter namn:
variables.Remove("City");

Assert.False(variables.Contains("City"));

// 2 - Enligt index:
variables.RemoveAt(1);

Assert.False(variables.Contains("Home address"));

// 3 - Rensa hela samlingen på en gång:
variables.Clear();

Assert.AreEqual(0, variables.Count);
```

### Se även

* class [VariableCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
