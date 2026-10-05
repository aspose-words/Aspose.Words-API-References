---
title: Aspose::Words::Saving::PdfPermissions enum
linktitle: PdfPermissions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfPermissions enum. Specifies the operations that are allowed to a user on an encrypted PDF document in C++.'
type: docs
weight: 80000
url: /cpp/aspose.words.saving/pdfpermissions/
---
## PdfPermissions enum


Specifies the operations that are allowed to a user on an encrypted PDF document.

```cpp
enum class PdfPermissions
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| DisallowAll | 0 | Disallows all operations on the PDF document. This is the default value. |
| AllowAll | 65535 | Allows all operations on the PDF document. |
| ContentCopy | 16 | Copy or otherwise extract text and graphics from the document by operations other than that controlled by [ContentCopyForAccessibility](./). |
| ContentCopyForAccessibility | 512 | Extract text and graphics (in support of accessibility to users with disabilities or for other purposes). |
| ModifyContents | 8 | Modify the contents of the document by operations other than those controlled by [ModifyAnnotations](./), [FillIn](./), and [DocumentAssembly](./). |
| ModifyAnnotations | 32 | Add or modify text annotations, fill in interactive form fields, and, if [ModifyContents](./) is also set, create or modify interactive form fields (including signature fields). |
| FillIn | 256 | Fill in existing interactive form fields (including signature fields), even if [ModifyContents](./) is clear. |
| DocumentAssembly | 1024 | Assemble the document (insert, rotate, or delete pages and create document outline items or thumbnail images), even if [ModifyContents](./) is clear. |
| Printing | 4 | Print the document (possibly not at the highest quality level, depending on whether [HighResolutionPrinting](./) is also set). |
| HighResolutionPrinting | 2052 | Print the document to a representation from which a faithful digital copy of the PDF content could be generated, based on an implementation-dependent algorithm. When this flag is clear (and [Printing](./) is set), printing shall be limited to a low-level representation of the appearance, possibly of degraded quality. |

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
