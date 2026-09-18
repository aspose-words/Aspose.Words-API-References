---
title: "Aspose::Words::ImportFormatOptions::get_ResolveThemeColors Methode"
linktitle: "get_ResolveThemeColors"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ImportFormatOptions::get_ResolveThemeColors Methode. Gibt einen booleschen Wert zurück oder setzt ihn, der angibt, ob die Themenfarben der Formen zwangsweise aufgelöst werden sollen. Der Standardwert ist false in C++."
type: docs
weight: 8500
url: /de/cpp/aspose.words/importformatoptions/get_resolvethemecolors/
---
## ImportFormatOptions::get_ResolveThemeColors method


Liest oder setzt einen booleschen Wert, der angibt, ob die Themenfarben der Formen zwingend aufgelöst werden sollen. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_ResolveThemeColors() const
```

## Hinweise


Bitte beachten Sie, dass diese Option nur für den [KeepSourceFormatting](../../importformatmode/) Modus relevant ist.

Normalerweise löst Aspose.Words die Quell‑Themenfarben nicht auf, wenn beim Importieren Stile erhalten werden können, ohne Formatierungsattribute in direkte zu expandieren. In diesem Fall können die tatsächlichen Farben der importierten Formen jedoch von denen im Originaldokument abweichen. Der Grund dafür sind unterschiedliche Themenfarben in den Quell‑ und Ziel‑Dokumenten. Das Setzen dieser Option auf **true** erzwingt das Auflösen der Themenfarben der Quellformen und damit das Beibehalten der tatsächlichen Farbe der Formen, die sie im Quelldokument haben.

## Beispiele



Zeigt, wie man einen Knoten importiert, wobei die Quellthemenfarben von Formen aufgelöst werden.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);

// Wechseln Sie zur primären Fußzeile und fügen Sie eine Form ein, die Themenfarben verwendet.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 50);
shape->get_Stroke()->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
// Importieren Sie die Quellfußzeile in das Zieldokument, wobei die Themenfarben aufgelöst werden,
// so dass die Form ihre tatsächliche Farbe aus dem Quelldokument beibehält.
System::SharedPtr<Aspose::Words::HeaderFooter> footer = srcDoc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ResolveThemeColors(true);
auto importedFooter = System::ExplicitCast<Aspose::Words::HeaderFooter>(dstDoc->ImportNode(footer, true, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options));

dstDoc->get_FirstSection()->get_HeadersFooters()->Add(importedFooter);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBase.ImportNodeWithResolveThemeColors.docx");
```

## Siehe auch

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
