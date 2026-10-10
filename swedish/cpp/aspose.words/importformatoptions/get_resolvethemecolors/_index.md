---
title: "Aspose::Words::ImportFormatOptions::get_ResolveThemeColors metod"
linktitle: "get_ResolveThemeColors"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ImportFormatOptions::get_ResolveThemeColors metod. Hämtar eller anger ett booleskt värde som specificerar om temafärger för formerna ska lösas tvångsmässigt. Standardvärdet är falskt i C++."
type: docs
weight: 8500
url: /sv/cpp/aspose.words/importformatoptions/get_resolvethemecolors/
---
## ImportFormatOptions::get_ResolveThemeColors method


Hämtar eller anger ett booleskt värde som specificerar om temafärger för former ska lösas tvångsmässigt. Standardvärdet är **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_ResolveThemeColors() const
```

## Anmärkningar


Observera att detta alternativ endast är relevant för läget [KeepSourceFormatting](../../importformatmode/).

Normalt löser inte Aspose.Words temafärger från källan när import av stilar kan bevaras utan att expandera formateringsattribut till direkta. Men i detta fall kan de faktiska färgerna på de importerade formerna skilja sig från de de hade i originaldokumentet. Anledningen är de olika temafärgerna i käll- och måldokumenten. Att sätta detta alternativ till **true** tvingar en lösning av källformens temafärger och därmed bevarar den faktiska färgen på formerna som de har i källdokumentet.

## Exempel



Visar hur man importerar en nod med upplösning av källans temafärger för former.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);

// Gå till den primära sidfoten och infoga en form som använder temafärger.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 50);
shape->get_Stroke()->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
// Importera källsidfoten till måldokumentet med temafärger upplösta,
// så att formen behåller sin faktiska färg från källdokumentet.
System::SharedPtr<Aspose::Words::HeaderFooter> footer = srcDoc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ResolveThemeColors(true);
auto importedFooter = System::ExplicitCast<Aspose::Words::HeaderFooter>(dstDoc->ImportNode(footer, true, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options));

dstDoc->get_FirstSection()->get_HeadersFooters()->Add(importedFooter);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBase.ImportNodeWithResolveThemeColors.docx");
```

## Se även

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
