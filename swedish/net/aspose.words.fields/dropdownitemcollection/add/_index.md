---
title: DropDownItemCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words för .NET
description: Förbättra enkelt din DropDownItemCollection med Add-metoden. Lägg direkt till strängar för att utöka din samling och förbättra användarupplevelsen.
type: docs
weight: 30
url: /sv/net/aspose.words.fields/dropdownitemcollection/add/
---
## DropDownItemCollection.Add method

Lägger till en sträng i slutet av samlingen.

```csharp
public int Add(string value)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| value | String | Strängen som ska läggas till i slutet av samlingen. |

### Returvärde

Det nollbaserade indexet där det nya elementet infogas.

## Exempel

Visar hur man infogar ett kombinationsrutefält och redigerar elementen i dess objektsamling.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en kombinationsruta och verifiera sedan dess samling av listrutealternativ.
// I Microsoft Word klickar användaren på kombinationsrutan,
// och välj sedan ett av textelementen i samlingen som ska visas.
string[] items = { "One", "Two", "Three" };
FormField comboBoxField = builder.InsertComboBox("DropDown", items, 0);
DropDownItemCollection dropDownItems = comboBoxField.DropDownItems;

Assert.AreEqual(3, dropDownItems.Count);
Assert.AreEqual("One", dropDownItems[0]);
Assert.AreEqual(1, dropDownItems.IndexOf("Two"));
Assert.IsTrue(dropDownItems.Contains("Three"));

// Det finns två sätt att lägga till ett nytt objekt i en befintlig samling av listruteobjekt.
// 1 - Lägg till ett objekt i slutet av samlingen:
dropDownItems.Add("Four");

// 2 - Infoga ett objekt före ett annat objekt vid ett angivet index:
dropDownItems.Insert(3, "Three and a half");

Assert.AreEqual(5, dropDownItems.Count);

// Iterera över samlingen och skriv ut varje element.
using (IEnumerator<string> dropDownCollectionEnumerator = dropDownItems.GetEnumerator())
    while (dropDownCollectionEnumerator.MoveNext())
        Console.WriteLine(dropDownCollectionEnumerator.Current);

// Det finns två sätt att ta bort element från en samling av listrutor.
// 1 - Ta bort ett objekt med innehåll som är lika med den skickade strängen:
dropDownItems.Remove("Four");

// 2 - Ta bort ett objekt i ett index:
dropDownItems.RemoveAt(3);

Assert.AreEqual(3, dropDownItems.Count);
Assert.IsFalse(dropDownItems.Contains("Three and a half"));
Assert.IsFalse(dropDownItems.Contains("Four"));

doc.Save(ArtifactsDir + "FormFields.DropDownItemCollection.html");

// Töm hela samlingen av listruteobjekt.
dropDownItems.Clear();
```

### Se även

* class [DropDownItemCollection](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
