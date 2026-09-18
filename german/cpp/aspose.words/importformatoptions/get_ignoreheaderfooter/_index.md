---
title: "Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter Methode"
linktitle: "get_IgnoreHeaderFooter"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter Methode. Gibt einen booleschen Wert zurück oder legt ihn fest, der angibt, dass die Quellformatierung des Kopf-/Fußzeileninhalts ignoriert wird, wenn der KeepSourceFormatting‑Modus verwendet wird. Der Standardwert ist true in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words/importformatoptions/get_ignoreheaderfooter/
---
## ImportFormatOptions::get_IgnoreHeaderFooter method


Gibt einen booleschen Wert zurück oder legt ihn fest, der angibt, dass die Quellformatierung des Kopf‑/Fußzeileninhalts ignoriert wird, wenn der [KeepSourceFormatting](../../importformatmode/)-Modus verwendet wird. Der Standardwert ist **true**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter() const
```


## Beispiele



Zeigt, wie das Ignorieren oder Nicht‑Ignorieren der Quellformatierung von Kopf‑/Fußzeileninhalten angegeben wird.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Wenn 'IgnoreHeaderFooter' false ist, dann wird die ursprüngliche Formatierung für Kopf‑/Fußzeileninhalte
// aus "Header and footer types.docx" verwendet.
// Wenn 'IgnoreHeaderFooter' true ist, dann wird die Formatierung für Kopf‑/Fußzeileninhalte
// aus "Document.docx" verwendet.
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_IgnoreHeaderFooter(false);

dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, importFormatOptions);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

## Siehe auch

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
