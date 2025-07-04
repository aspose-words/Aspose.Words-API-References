---
title: Document.RemoveMacros
linktitle: RemoveMacros
articleTitle: RemoveMacros
second_title: Aspose.Words for .NET
description: Effortlessly remove all macros, toolbars, and custom command settings from your VBA project with the Document RemoveMacros method for a cleaner document.
type: docs
weight: 720
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

Assert.That(doc.HasMacros, Is.True);
Assert.That(doc.VbaProject.Name, Is.EqualTo("Project"));

// Remove the document's VBA project, along with all its macros.
doc.RemoveMacros();

Assert.That(doc.HasMacros, Is.False);
Assert.That(doc.VbaProject, Is.Null);
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
