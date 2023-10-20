---
title: CleanupOptions.UnusedLists
linktitle: UnusedLists
articleTitle: UnusedLists
second_title: Aspose.Words för .NET
description: CleanupOptions UnusedLists fast egendom. Anger om oanvända list och listdefinitioner ska tas bort från dokumentet. Standardvärdet ärSann  i C#.
type: docs
weight: 40
url: /sv/net/aspose.words/cleanupoptions/unusedlists/
---
## CleanupOptions.UnusedLists property

Anger om oanvända list- och listdefinitioner ska tas bort från dokumentet. Standardvärdet är`Sann` .

```csharp
public bool UnusedLists { get; set; }
```

## Exempel

Visar hur man tar bort alla oanvända anpassade stilar från ett dokument.

```csharp
Document doc = new Document();

doc.Styles.Add(StyleType.List, "MyListStyle1");
doc.Styles.Add(StyleType.List, "MyListStyle2");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle1");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle2");

// I kombination med de inbyggda stilarna har dokumentet nu åtta stilar.
// En anpassad stil markeras som "använd" medan det finns någon text i dokumentet
// formaterad i den stilen. Det betyder att de 4 stilarna vi har lagt till för närvarande är oanvända.
Assert.AreEqual(8, doc.Styles.Count);

// Använd en anpassad teckenstil och sedan en anpassad liststil. Om du gör det kommer de att markeras som "använda".
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

// Nu finns det en oanvänd teckenstil och en oanvänd liststil.
// Cleanup()-metoden, när den är konfigurerad med ett CleanupOptions-objekt, kan rikta in sig på oanvända stilar och ta bort dem.
CleanupOptions cleanupOptions = new CleanupOptions
{
    UnusedLists = true, UnusedStyles = true, UnusedBuiltinStyles = true
};

doc.Cleanup(cleanupOptions);

Assert.AreEqual(4, doc.Styles.Count);

 // Om du tar bort varje nod som en anpassad stil tillämpas på markeras den som "oanvänd" igen.
// Kör rengöringsmetoden igen för att ta bort dem.
doc.FirstSection.Body.RemoveAllChildren();
doc.Cleanup(cleanupOptions);

Assert.AreEqual(2, doc.Styles.Count);
```

### Se även

* class [CleanupOptions](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
