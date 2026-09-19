---
title: "metodo Aspose::Words::ImportFormatOptions::get_ResolveThemeColors"
linktitle: "get_ResolveThemeColors"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::ImportFormatOptions::get_ResolveThemeColors. Ottiene o imposta un valore booleano che specifica se risolvere forzatamente i colori tematici delle forme. Il valore predefinito è false in C++."
type: docs
weight: 8500
url: /it/cpp/aspose.words/importformatoptions/get_resolvethemecolors/
---
## ImportFormatOptions::get_ResolveThemeColors method


Ottiene o imposta un valore booleano che specifica se risolvere forzatamente i colori tema delle forme. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_ResolveThemeColors() const
```

## Note


Si prega di notare che questa opzione è rilevante solo per la modalità [KeepSourceFormatting](../../importformatmode/).

Normalmente, Aspose.Words non risolve i colori tematici di origine quando l'importazione degli stili può essere preservata senza espandere gli attributi di formattazione in quelli diretti. Tuttavia, in questo caso i colori effettivi delle forme importate possono differire da quelli presenti nel documento originale. Il motivo è la differenza dei colori tematici nei documenti di origine e di destinazione. Impostare questa opzione su **true** forza la risoluzione dei colori tematici delle forme di origine e quindi preserva il colore reale delle forme nel documento di origine.

## Esempi



Mostra come importare un nodo risolvendo i colori del tema sorgente delle forme.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);

// Sposta al piè di pagina principale e inserisci una forma che utilizza i colori del tema.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 50);
shape->get_Stroke()->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);

auto dstDoc = System::MakeObject<Aspose::Words::Document>();
// Importa il piè di pagina di origine nel documento di destinazione con i colori del tema risolti,
// in modo che la forma conservi il suo colore reale dal documento di origine.
System::SharedPtr<Aspose::Words::HeaderFooter> footer = srcDoc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ResolveThemeColors(true);
auto importedFooter = System::ExplicitCast<Aspose::Words::HeaderFooter>(dstDoc->ImportNode(footer, true, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options));

dstDoc->get_FirstSection()->get_HeadersFooters()->Add(importedFooter);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBase.ImportNodeWithResolveThemeColors.docx");
```

## Vedi anche

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
