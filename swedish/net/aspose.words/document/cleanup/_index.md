---
title: Document.Cleanup
linktitle: Cleanup
articleTitle: Cleanup
second_title: Aspose.Words för .NET
description: Optimera dina dokument med vår rensningsmetod – ta bort oanvända format och listor för ett renare och effektivare arbetsflöde. Förbättra läsbarheten idag!
type: docs
weight: 580
url: /sv/net/aspose.words/document/cleanup/
---
## Cleanup() {#cleanup}

Rensar oanvända format och listor från dokumentet.

```csharp
public void Cleanup()
```

## Exempel

Visar hur man tar bort oanvända anpassade format från ett dokument.

```csharp
Document doc = new Document();

doc.Styles.Add(StyleType.List, "MyListStyle1");
doc.Styles.Add(StyleType.List, "MyListStyle2");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle1");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle2");

// Tillsammans med de inbyggda stilarna har dokumentet nu åtta stilar.
// En anpassad stil räknas som "använd" när den tillämpas på någon del av dokumentet,
// vilket betyder att de fyra stilarna vi lade till för närvarande inte används.
Assert.AreEqual(8, doc.Styles.Count);

// Använd ett anpassat teckenformat och sedan ett anpassat listformat. Om du gör det markeras formaten som "använda".
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

doc.Cleanup();

Assert.AreEqual(6, doc.Styles.Count);

// Om du tar bort varje nod som en anpassad stil tillämpas på markeras den som "oanvänd" igen.
// Kör rensningsmetoden igen för att ta bort dem.
doc.FirstSection.Body.RemoveAllChildren();
doc.Cleanup();

Assert.AreEqual(4, doc.Styles.Count);
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## Cleanup(*[CleanupOptions](../../cleanupoptions/)*) {#cleanup_1}

Rensar oanvända stilar och listor från dokumentet beroende på angivet[`CleanupOptions`](../../cleanupoptions/) .

```csharp
public void Cleanup(CleanupOptions options)
```

## Exempel

Visar hur man tar bort alla oanvända anpassade format från ett dokument.

```csharp
Document doc = new Document();

doc.Styles.Add(StyleType.List, "MyListStyle1");
doc.Styles.Add(StyleType.List, "MyListStyle2");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle1");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle2");

// Tillsammans med de inbyggda stilarna har dokumentet nu åtta stilar.
// En anpassad stil markeras som "använd" så länge det finns text i dokumentet
// formaterad i den stilen. Det betyder att de fyra stilarna vi lade till för närvarande inte används.
Assert.AreEqual(8, doc.Styles.Count);

// Använd ett anpassat teckenformat och sedan ett anpassat listformat. Om du gör det markeras de som "använda".
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

// Nu finns det ett oanvänt teckenformat och ett oanvänt listformat.
// Metoden Cleanup(), när den konfigureras med ett CleanupOptions-objekt, kan rikta in sig på oanvända stilar och ta bort dem.
CleanupOptions cleanupOptions = new CleanupOptions
{
    UnusedLists = true, UnusedStyles = true, UnusedBuiltinStyles = true
};

doc.Cleanup(cleanupOptions);

Assert.AreEqual(4, doc.Styles.Count);

 // Om du tar bort varje nod som en anpassad stil tillämpas på markeras den som "oanvänd" igen.
// Kör rensningsmetoden igen för att ta bort dem.
doc.FirstSection.Body.RemoveAllChildren();
doc.Cleanup(cleanupOptions);

Assert.AreEqual(2, doc.Styles.Count);
```

### Se även

* class [CleanupOptions](../../cleanupoptions/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
