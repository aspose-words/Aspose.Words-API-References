---
title: StyleCollection.Count
second_title: Aspose.Words för .NET API Referens
description: StyleCollection fast egendom. Hämtar antalet stilar i samlingen.
type: docs
weight: 10
url: /sv/net/aspose.words/stylecollection/count/
---
## StyleCollection.Count property

Hämtar antalet stilar i samlingen.

```csharp
public int Count { get; }
```

### Exempel

Visar hur man lägger till en stil till ett dokuments stilsamling.

```csharp
Document doc = new Document();
StyleCollection styles = doc.Styles;

// Ställ in standardparametrar för nya stilar som vi senare kan lägga till i den här samlingen.
styles.DefaultFont.Name = "Courier New";

// Om vi lägger till en stil av "StyleType.Paragraph", kommer samlingen att tillämpa värdena för
// dess "DefaultParagraphFormat"-egenskap till stilens "ParagraphFormat"-egenskap.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;

// Lägg till en stil och kontrollera sedan att den har standardinställningarna.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### Se även

* class [StyleCollection](../)
* namnutrymme [Aspose.Words](../../stylecollection/)
* hopsättning [Aspose.Words](../../../)


