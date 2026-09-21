---
title: "Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream metod"
linktitle: "get_DocumentPartStream"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream metod. Tillåter att ange strömmen där dokumentdelen ska sparas i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.saving/documentpartsavingargs/get_documentpartstream/
---
## DocumentPartSavingArgs::get_DocumentPartStream method


Tillåter att ange strömmen där dokumentdelen ska sparas.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::DocumentPartSavingArgs::get_DocumentPartStream() const
```

## Anmärkningar


Denna egenskap låter dig spara dokumentdelar till strömmar istället för filer vid HTML‑export.

Standardvärdet är **null**. När denna egenskap är **null** kommer dokumentdelen att sparas till en fil som anges i egenskapen [DocumentPartFileName](../get_documentpartfilename/).

När sparning till en ström i HTML‑format begärs av [Save()](../) eller [Save()](../) och den första dokumentdelen håller på att sparas, föreslår Aspose.Words här huvudutdata‑strömmen som ursprungligen skickades av anroparen.

När sparning till EPUB‑format, som är ett containerformat baserat på HTML, [DocumentPartStream](./) inte kan specificeras eftersom alla underliggande delar kommer att kapslas in i ett enda utdata‑paket.

## Se även

* Class [DocumentPartSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
