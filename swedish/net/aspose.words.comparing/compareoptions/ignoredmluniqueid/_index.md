---
title: CompareOptions.IgnoreDmlUniqueId
second_title: Aspose.Words för .NET API Referens
description: CompareOptions fast egendom. Anger om skillnaden i DrawingML unika Id. ska ignoreras. Standardvärdet ärfalsk .
type: docs
weight: 60
url: /sv/net/aspose.words.comparing/compareoptions/ignoredmluniqueid/
---
## CompareOptions.IgnoreDmlUniqueId property

Anger om skillnaden i DrawingML unika Id. ska ignoreras. Standardvärdet är`falsk` .

```csharp
public bool IgnoreDmlUniqueId { get; set; }
```

### Exempel

Visar hur man jämför dokument som ignorerar DML unika ID.

```csharp
Document docA = new Document(MyDir + "DML unique ID original.docx");
Document docB = new Document(MyDir + "DML unique ID compare.docx");

// Som standard ignorerar inte Aspose.Words DML:s unika ID, och antalet revisioner var 2.
// Om vi ignorerar DML:s unika ID och antalet revisioner var 0.
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.IgnoreDmlUniqueId = isIgnoreDmlUniqueId;

docA.Compare(docB, "Aspose.Words", DateTime.Now, compareOptions);

Assert.AreEqual(isIgnoreDmlUniqueId ? 0 : 2, docA.Revisions.Count);
```

### Se även

* class [CompareOptions](../)
* namnutrymme [Aspose.Words.Comparing](../../compareoptions/)
* hopsättning [Aspose.Words](../../../)


