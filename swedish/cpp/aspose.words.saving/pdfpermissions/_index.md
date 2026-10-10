---
title: "Aspose::Words::Saving::PdfPermissions enum"
linktitle: "PdfPermissions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::PdfPermissions enum. Anger vilka operationer som är tillåtna för en användare på ett krypterat PDF-dokument i C++."
type: docs
weight: 80000
url: /sv/cpp/aspose.words.saving/pdfpermissions/
---
## PdfPermissions enum


Anger vilka operationer som är tillåtna för en användare på ett krypterat PDF-dokument.

```cpp
enum class PdfPermissions
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| DisallowAll | 0 | Tillåter inga operationer på PDF-dokumentet. Detta är standardvärdet. |
| AllowAll | 65535 | Tillåter alla operationer på PDF-dokumentet. |
| ContentCopy | n/a | Kopiera eller på annat sätt extrahera text och grafik från dokumentet genom operationer som inte styrs av [ContentCopyForAccessibility](./). |
| ContentCopyForAccessibility | n/a | Extrahera text och grafik (för att stödja tillgänglighet för användare med funktionsnedsättningar eller för andra ändamål). |
| ModifyContents | n/a | Modifiera dokumentets innehåll genom operationer som inte styrs av [ModifyAnnotations](./), [FillIn](./) och [DocumentAssembly](./). |
| ModifyAnnotations | n/a | Lägg till eller ändra textanteckningar, fyll i interaktiva formulärfält och, om [ModifyContents](./) också är aktiverat, skapa eller ändra interaktiva formulärfält (inklusive signaturfält). |
| FillIn | n/a | Fyll i befintliga interaktiva formulärfält (inklusive signaturfält), även om [ModifyContents](./) är avmarkerat. |
| DocumentAssembly | n/a | Sätt ihop dokumentet (infoga, rotera eller ta bort sidor och skapa dokumentöversiktsobjekt eller miniatyrbilder), även om [ModifyContents](./) är avmarkerat. |
| Printing | n/a | Skriv ut dokumentet (möjligen inte på högsta kvalitet, beroende på om [HighResolutionPrinting](./) också är aktiverat). |
| HighResolutionPrinting | n/a | Skriv ut dokumentet till en representation från vilken en trogen digital kopia av PDF-innehållet kan genereras, baserat på en implementationsberoende algoritm. När denna flagga är avklarad (och [Printing](./) är aktiverad) ska utskrift begränsas till en låg nivå-representation av utseendet, eventuellt med försämrad kvalitet. |

## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
