---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel Methode"
linktitle: "get_NavigationMapLevel"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel Methode. Gibt die maximale Ebene von Überschriften an, die in die Navigationskarte übernommen werden, wenn in die Formate EPUB, MOBI oder AZW3 exportiert wird. Der Standardwert ist %3 in C++."
type: docs
weight: 40500
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_navigationmaplevel/
---
## HtmlSaveOptions::get_NavigationMapLevel method


Gibt die maximale Ebene von Überschriften an, die in die Navigationskarte beim Exportieren in die Formate EPUB, MOBI oder AZW3 übernommen wird. Standardwert ist **%3**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel() const
```

## Hinweise


Die Navigationskarte ermöglicht es Benutzeragenten, eine einfache Navigation durch die Dokumentstruktur bereitzustellen. Normalerweise entsprechen Navigationspunkte den Überschriften im Dokument. Um Überschriften bis zur Ebene **N** zu übernehmen, weisen Sie diesen Wert [NavigationMapLevel](./) zu.

Standardmäßig werden drei Ebenen von Überschriften übernommen: Absätze mit den Stilen **Heading 1**, **Heading 2** und **Heading 3**. Sie können diese Eigenschaft auf einen Wert von 1 bis 9 setzen, um die entsprechende maximale Ebene anzufordern. Wird sie auf null gesetzt, reduziert sich die Navigationskarte auf nur die Dokumentwurzel oder die Wurzeln der Dokumentteile.

## Beispiele



Zeigt, wie ein Inhaltsverzeichnis für Azw3-Dokumente erstellt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Azw3);
options->set_NavigationMapLevel(2);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.CreateAZW3Toc.azw3", options);
```


Zeigt, wie ein Inhaltsverzeichnis für Mobi-Dokumente erstellt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Mobi);
options->set_NavigationMapLevel(5);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.CreateMobiToc.mobi", options);
```

## Siehe auch

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
