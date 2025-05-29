---
title: Document.Variables
linktitle: Variables
articleTitle: Variables
second_title: Aspose.Words för .NET
description: Upptäck dokumentvariabler. Få tillgång till en kraftfull samling anpassningsbara variabler för dina dokument och mallar, vilket förbättrar effektiviteten och flexibiliteten.
type: docs
weight: 460
url: /sv/net/aspose.words/document/variables/
---
## Document.Variables property

Returnerar samlingen av variabler som lagts till i ett dokument eller en mall.

```csharp
public VariableCollection Variables { get; }
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

* class [VariableCollection](../../variablecollection/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
