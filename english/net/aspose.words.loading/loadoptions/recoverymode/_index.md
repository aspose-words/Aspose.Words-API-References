---
title: LoadOptions.RecoveryMode
linktitle: RecoveryMode
articleTitle: RecoveryMode
second_title: Aspose.Words for .NET
description: LoadOptions.RecoveryMode property sets how Aspose.Words handles document errors by recovery or strict loading.
type: docs
weight: 140
url: /net/aspose.words.loading/loadoptions/recoverymode/
---
## LoadOptions.RecoveryMode property

Defines how the document should be handled if errors occur during loading. Use this property to specify whether the system should attempt to recover the document or follow another defined behavior. The default value is TryRecover.

```csharp
public DocumentRecoveryMode RecoveryMode { get; set; }
```

## Examples

Shows how to try to recover a document if errors occurred during loading.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.RecoveryMode = DocumentRecoveryMode.TryRecover;

Document doc = new Document(MyDir + "Corrupted footnotes.docx", loadOptions);
```

### See Also

* enum [DocumentRecoveryMode](../../documentrecoverymode/)
* class [LoadOptions](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
