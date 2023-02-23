---
title: Document.RemoveMacros
linktitle: RemoveMacros
second_title: Aspose.Words for .NET API Reference
description: Document method. Removes all macros the VBA project as well as toolbars and command customizations from the document in C#.
type: docs
weight: 670
url: /net/aspose.words/document/removemacros/
---
## Document.RemoveMacros method

Removes all macros (the VBA project) as well as toolbars and command customizations from the document.

```csharp
public void RemoveMacros()
```

## Remarks

By removing all macros from a document you can ensure the document contains no macro viruses.

## Examples

Shows how to remove all macros from a document.

```csharp
Document doc = new Document(MyDir + "Macro.docm");

Assert.IsTrue(doc.HasMacros);
Assert.AreEqual("Project", doc.VbaProject.Name);

// Remove the document's VBA project, along with all its macros.
doc.RemoveMacros();

Assert.IsFalse(doc.HasMacros);
Assert.Null(doc.VbaProject);
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../document/)
* assembly [Aspose.Words](../../../)
