---
title: "Aspose::Words::ImportFormatOptions::get_ForceCopyStyles Methode"
linktitle: "get_ForceCopyStyles"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ImportFormatOptions::get_ForceCopyStyles Methode. Gibt einen booleschen Wert zurück oder legt ihn fest, der angibt, ob widersprüchliche Stile im KeepSourceFormatting‑Modus kopiert werden sollen. Der Standardwert ist false in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words/importformatoptions/get_forcecopystyles/
---
## ImportFormatOptions::get_ForceCopyStyles method


Gibt einen booleschen Wert zurück oder legt ihn fest, der angibt, ob widersprüchliche Stile im [KeepSourceFormatting](../../importformatmode/) Modus kopiert werden sollen. Der Standardwert ist **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_ForceCopyStyles() const
```

## Hinweise


Standardmäßig, wenn ein passender Stil bereits in einem Zieldokument existiert, wird die Formatierung des Quellstils in direkte Knoteneigenschaften expandiert und der Stil dieses Knotens wird auf den Standard zurückgesetzt.

Wenn diese Option auf **true** gesetzt ist, wird der Quellstil zwangsweise mit einem eindeutigen Namen in das Zieldokument kopiert und auf den importierten Knoten angewendet.

Hinweis: In diesem Fall ist nicht garantiert, dass die Formatierung des importierten Knotens im Zieldokument erhalten bleibt.

## Beispiele



Zeigt, wie Quellstile mit eindeutigen Namen zwangsweise kopiert werden.
```cpp
// Beide Dokumente enthalten MyStyle1 und MyStyle2, MyStyle3 existiert nur im Quelldokument.
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Styles source.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Styles destination.docx");

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ForceCopyStyles(true);
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

System::SharedPtr<Aspose::Words::ParagraphCollection> paras = dstDoc->get_Sections()->idx_get(1)->get_Body()->get_Paragraphs();

ASSERT_EQ(paras->idx_get(0)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle1_0");
ASSERT_EQ(paras->idx_get(1)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle2_0");
ASSERT_EQ(paras->idx_get(2)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle3");
```

## Siehe auch

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
