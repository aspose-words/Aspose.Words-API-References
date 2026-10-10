---
title: "Metodo Aspose::Words::PageSetup::get_TextOrientation"
linktitle: "get_TextOrientation"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::PageSetup::get_TextOrientation. Consente di specificare TextOrientation per l'intera pagina. Il valore predefinito è Horizontal in C++."
type: docs
weight: 45000
url: /it/cpp/aspose.words/pagesetup/get_textorientation/
---
## PageSetup::get_TextOrientation method


Consente di specificare [TextOrientation](./) per l'intera pagina. Il valore predefinito è [Horizontal](../../textorientation/)

```cpp
Aspose::Words::TextOrientation Aspose::Words::PageSetup::get_TextOrientation()
```


## Esempi



Mostra come impostare l'orientamento del testo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Imposta la proprietà "TextOrientation" su "TextOrientation.Upward" per ruotare tutto il testo di 90 gradi
// verso destra in modo che tutto il testo da sinistra a destra ora vada dall'alto verso il basso.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_TextOrientation(Aspose::Words::TextOrientation::Upward);

doc->Save(get_ArtifactsDir() + u"PageSetup.SetTextOrientation.docx");
```

## Vedi anche

* Enum [TextOrientation](../../textorientation/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
