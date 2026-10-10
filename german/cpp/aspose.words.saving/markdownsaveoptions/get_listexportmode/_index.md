---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode Methode"
linktitle: "get_ListExportMode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode Methode. Gibt an, wie Listenelemente in die Ausgabedatei geschrieben werden. Standardwert ist MarkdownSyntax in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words.saving/markdownsaveoptions/get_listexportmode/
---
## MarkdownSaveOptions::get_ListExportMode method


Gibt an, wie Listenelemente in die Ausgabedatei geschrieben werden. Standardwert ist [MarkdownSyntax](../../markdownlistexportmode/).

```cpp
Aspose::Words::Saving::MarkdownListExportMode Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode() const
```

## Hinweise


Wenn diese Eigenschaft auf [PlainText](../../markdownlistexportmode/) gesetzt wird, werden alle Listenkennzeichnungen mit [UpdateListLabels](../../../aspose.words/document/updatelistlabels/) aktualisiert und mit ihren tatsächlichen Werten exportiert. Solche Listen können mit dem Markdown‑Format nicht kompatibel sein und werden beim Import in diesem Fall als Klartext erkannt.

Wenn diese Eigenschaft auf [MarkdownSyntax](../../markdownlistexportmode/) gesetzt wird, versucht der Writer, Listenelemente so zu exportieren, dass sie von Markdown automatisch nummeriert werden können.

## Beispiele



Zeigt, wie Listenelemente in das Markdown-Dokument geschrieben werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");

// Verwenden Sie MarkdownListExportMode.PlainText oder MarkdownListExportMode.MarkdownSyntax, um die Liste zu exportieren.
auto options = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
options->set_ListExportMode(markdownListExportMode);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ListExportMode.md", options);
```

## Siehe auch

* Enum [MarkdownListExportMode](../../markdownlistexportmode/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
