---
title: Document.RemoveCustomizations
linktitle: RemoveCustomizations
articleTitle: RemoveCustomizations
second_title: Aspose.Words for .NET
description: Remove toolbar and keyboard customizations from Word documents to restore default settings and ensure a clean document experience.
type: docs
weight: 710
url: /net/aspose.words/document/removecustomizations/
---
## Document.RemoveCustomizations method

Removes toolbar and keyboard command customizations from the document.

```csharp
public void RemoveCustomizations()
```

## Examples

Shows how to remove toolbar and keyboard command customizations from the document.

```csharp
Document doc = new Document(MyDir + "Customized menu.docx");

// Remove all custom document UI customizations, including custom context menu entries.
doc.RemoveCustomizations();

doc.Save(ArtifactsDir + "Document.RemoveCustomizations.docx");
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
