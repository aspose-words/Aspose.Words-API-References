---
title: Class DropDownItemCollection
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Fields.DropDownItemCollection klass. En samling strängar som representerar alla objekt i ett rullgardinsfält.
type: docs
weight: 1350
url: /sv/net/aspose.words.fields/dropdownitemcollection/
---
## DropDownItemCollection class

En samling strängar som representerar alla objekt i ett rullgardinsfält.

```csharp
public class DropDownItemCollection : IEnumerable<string>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.fields/dropdownitemcollection/count/) { get; } | Hämtar antalet element som finns i samlingen. |
| [Item](../../aspose.words.fields/dropdownitemcollection/item/) { get; set; } | Hämtar eller ställer in elementet vid angivet index. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Add](../../aspose.words.fields/dropdownitemcollection/add/)(string) | Lägger till en sträng i slutet av samlingen. |
| [Clear](../../aspose.words.fields/dropdownitemcollection/clear/)() | Tar bort alla element från samlingen. |
| [Contains](../../aspose.words.fields/dropdownitemcollection/contains/)(string) | Bestämmer om samlingen innehåller det angivna värdet. |
| [GetEnumerator](../../aspose.words.fields/dropdownitemcollection/getenumerator/)() | Returnerar ett uppräkningsobjekt som kan användas för att iterera över alla objekt i samlingen. |
| [IndexOf](../../aspose.words.fields/dropdownitemcollection/indexof/)(string) | Returnerar det nollbaserade indexet för det angivna värdet i samlingen. |
| [Insert](../../aspose.words.fields/dropdownitemcollection/insert/)(int, string) | Infogar en sträng i samlingen vid det angivna indexet. |
| [Remove](../../aspose.words.fields/dropdownitemcollection/remove/)(string) | Tar bort det angivna värdet från samlingen. |
| [RemoveAt](../../aspose.words.fields/dropdownitemcollection/removeat/)(int) | Tar bort ett värde vid det angivna indexet. |

### Exempel

Visar hur man infogar ett kombinationsrutafält och redigerar elementen i dess objektsamling.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en kombinationsruta och verifiera sedan dess samling av listruta.
// I Microsoft Word klickar användaren på kombinationsrutan,
// och välj sedan ett av textobjekten i samlingen att visa.
string[] items = { "One", "Two", "Three" };
FormField comboBoxField = builder.InsertComboBox("DropDown", items, 0);
DropDownItemCollection dropDownItems = comboBoxField.DropDownItems;

Assert.AreEqual(3, dropDownItems.Count);
Assert.AreEqual("One", dropDownItems[0]);
Assert.AreEqual(1, dropDownItems.IndexOf("Two"));
Assert.IsTrue(dropDownItems.Contains("Three"));

// Det finns två sätt att lägga till ett nytt objekt till en befintlig samling av rullgardinsobjekt.
// 1 - Lägg till ett föremål i slutet av samlingen:
dropDownItems.Add("Four");

// 2 - Infoga ett objekt före ett annat objekt vid ett specificerat index:
dropDownItems.Insert(3, "Three and a half");

Assert.AreEqual(5, dropDownItems.Count);

// Iterera över samlingen och skriv ut varje element.
using (IEnumerator<string> dropDownCollectionEnumerator = dropDownItems.GetEnumerator())
    while (dropDownCollectionEnumerator.MoveNext())
        Console.WriteLine(dropDownCollectionEnumerator.Current);

// Det finns två sätt att ta bort element från en samling rullgardinsobjekt.
// 1 - Ta bort ett objekt med innehåll lika med den skickade strängen:
dropDownItems.Remove("Four");

// 2 - Ta bort ett objekt i ett index:
dropDownItems.RemoveAt(3);

Assert.AreEqual(3, dropDownItems.Count);
Assert.IsFalse(dropDownItems.Contains("Three and a half"));
Assert.IsFalse(dropDownItems.Contains("Four"));

doc.Save(ArtifactsDir + "FormFields.DropDownItemCollection.html");

// Töm hela samlingen av rullgardinsobjekt.
dropDownItems.Clear();
```

### Se även

* class [FormField](../formfield/)
* property [DropDownItems](../formfield/dropdownitems/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)


