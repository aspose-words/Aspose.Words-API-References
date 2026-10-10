---
title: "Metodo Aspose::Words::Font::get_Emboss"
linktitle: "get_Emboss"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Font::get_Emboss. Vero se il carattere è formattato come embossato in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words/font/get_emboss/
---
## Font::get_Emboss method


Vero se il carattere è formattato in rilievo.

```cpp
bool Aspose::Words::Font::get_Emboss()
```


## Esempi



Mostra come applicare effetti di incisione/embossing al testo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_Color(System::Drawing::Color::get_LightBlue());

// Di seguito sono riportati due modi per utilizzare le ombre per applicare un effetto simile a 3D al testo.
// 1 -  Incidi il testo per far sembrare le lettere incassate nella pagina:
builder->get_Font()->set_Engrave(true);

builder->Writeln(u"This text is engraved.");

// 2 -  Embossa il testo per far sembrare le lettere sporgenti dalla pagina:
builder->get_Font()->set_Engrave(false);
builder->get_Font()->set_Emboss(true);

builder->Writeln(u"This text is embossed.");

doc->Save(get_ArtifactsDir() + u"Font.EngraveEmboss.docx");
```

## Vedi anche

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
