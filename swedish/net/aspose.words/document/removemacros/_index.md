---
title: Document.RemoveMacros
linktitle: RemoveMacros
articleTitle: RemoveMacros
second_title: Aspose.Words för .NET
description: Document RemoveMacros metod. Tar bort alla makron VBAprojektet samt verktygsfält och kommandoanpassningar från dokumentet i C#.
type: docs
weight: 670
url: /sv/net/aspose.words/document/removemacros/
---
## Document.RemoveMacros method

Tar bort alla makron (VBA-projektet) samt verktygsfält och kommandoanpassningar från dokumentet.

```csharp
public void RemoveMacros()
```

## Anmärkningar

Genom att ta bort alla makron från ett dokument kan du säkerställa att dokumentet inte innehåller några makrovirus.

## Exempel

Visar hur man tar bort alla makron från ett dokument.

```csharp
Document doc = new Document(MyDir + "Macro.docm");

Assert.IsTrue(doc.HasMacros);
Assert.AreEqual("Project", doc.VbaProject.Name);

// Ta bort dokumentets VBA-projekt, tillsammans med alla dess makron.
doc.RemoveMacros();

Assert.IsFalse(doc.HasMacros);
Assert.Null(doc.VbaProject);
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
