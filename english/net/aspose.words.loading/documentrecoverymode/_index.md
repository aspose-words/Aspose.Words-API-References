---
title: DocumentRecoveryMode Enum
linktitle: DocumentRecoveryMode
articleTitle: DocumentRecoveryMode
second_title: Aspose.Words for .NET
description: Aspose.Words.DocumentRecoveryMode enum specifies recovery modes for documents with errors during loading.
type: docs
weight: 4070
url: /net/aspose.words.loading/documentrecoverymode/
---
## DocumentRecoveryMode enumeration

Specifies the available recovery options when a document encounters errors during loading.

```csharp
public enum DocumentRecoveryMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | No recovery is attempted. If the document is invalid, loading will fail with an error. |
| TryRecover | `1` | Attempts to recover the document while preserving as much data as possible. |

## Examples

Shows how to try to recover a document if errors occurred during loading.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.RecoveryMode = DocumentRecoveryMode.TryRecover;

Document doc = new Document(MyDir + "Corrupted footnotes.docx", loadOptions);
```

### See Also

* namespace [Aspose.Words.Loading](../../aspose.words.loading/)
* assembly [Aspose.Words](../../)
