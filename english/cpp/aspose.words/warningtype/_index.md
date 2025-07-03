---
title: Aspose::Words::WarningType enum
linktitle: WarningType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::WarningType enum. Specifies the type of a warning that is issued by Aspose.Words during document loading or saving in C++.'
type: docs
weight: 129000
url: /cpp/aspose.words/warningtype/
---
## WarningType enum


Specifies the type of a warning that is issued by Aspose.Words during document loading or saving.

```cpp
enum class WarningType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| DataLossCategory | 255 | Some text/char/image or other data will be missing from either the document tree following load, or from the created document following save. |
| DataLoss | 1 | Generic data loss, no specific code. |
| MajorFormattingLossCategory | 65280 | The resulting document or a particular location in it might look substantially different compared to the original document. |
| MajorFormattingLoss | 256 | Generic major formatting loss, no specific code. |
| MinorFormattingLossCategory | 16711680 | The resulting document or a particular location in it might look somewhat different compared to the original document. |
| MinorFormattingLoss | 65536 | Generic minor formatting loss, no specific code. |
| FontSubstitution | 131072 | [Font](../font/) has been substituted. |
| FontEmbedding | 262144 | Loss of embedded font information during document saving. |
| UnexpectedContentCategory | 251658240 | Some content in the source document could not be recognized (i.e. is unsupported), this may or may not cause issues or result in data/formatting loss. |
| UnexpectedContent | 16777216 | Generic unexpected content, no specific code. |
| Hint | 268435456 | Advises of a potential problem or suggests an improvement. |

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
