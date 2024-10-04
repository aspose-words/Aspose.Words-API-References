---
title: JustificationMode Enum
linktitle: JustificationMode
articleTitle: JustificationMode
second_title: Aspose.Words for .NET
description: Aspose.Words.Settings.JustificationMode enum. Specifies the character spacing adjustment for a document. The default value is Expand in C#.
type: docs
weight: 6210
url: /net/aspose.words.settings/justificationmode/
---
## JustificationMode enumeration

Specifies the character spacing adjustment for a document. The default value is `Expand`.

```csharp
public enum JustificationMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Expand | `0` | Do not compress character spacing. |
| Compress | `1` | Compress character spacing. |
| CompressKana | `2` | Compress, using rules of the kana syllabaries, Hiragana and Katakana. |

## Examples

Shows how to manage character spacing control.

```csharp
Document doc = new Document(MyDir + "Document.docx");

JustificationMode justificationMode = doc.JustificationMode;
if (justificationMode == JustificationMode.Expand)
    doc.JustificationMode = JustificationMode.Compress;

doc.Save(ArtifactsDir + "Document.SetJustificationMode.docx");
```

### See Also

* namespace [Aspose.Words.Settings](../../aspose.words.settings/)
* assembly [Aspose.Words](../../)
