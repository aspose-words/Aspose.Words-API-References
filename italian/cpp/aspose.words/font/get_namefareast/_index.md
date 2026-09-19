---
title: "Metodo Aspose::Words::Font::get_NameFarEast"
linktitle: "get_NameFarEast"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Font::get_NameFarEast. Restituisce o imposta un nome di carattere dell'Est asiatico in C++."
type: docs
weight: 28000
url: /it/cpp/aspose.words/font/get_namefareast/
---
## Font::get_NameFarEast method


Restituisce o imposta un nome di carattere dell'Est asiatico.

```cpp
System::String Aspose::Words::Font::get_NameFarEast()
```


## Esempi



Mostra come inserire e formattare testo in una lingua dell'Estremo Oriente.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Specifica le impostazioni del carattere che il costruttore di documenti applicherà a qualsiasi testo inserito.
builder->get_Font()->set_Name(u"Courier New");
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());

// Denomina le equivalenze "FarEast" per il nostro carattere e locale.
// Se il costruttore inserisce caratteri asiatici con questa configurazione del carattere, allora ogni run che contiene
// questi caratteri li visualizzeranno usando il carattere/locale "FarEast" invece di quello predefinito.
// Ciò potrebbe essere utile quando un carattere occidentale non ha rappresentazioni ideali per i caratteri asiatici.
builder->get_Font()->set_NameFarEast(u"SimSun");
builder->get_Font()->set_LocaleIdFarEast(System::MakeObject<System::Globalization::CultureInfo>(u"zh-CN", false)->get_LCID());

// Questo testo verrà visualizzato nel carattere/locale predefinito.
builder->Writeln(u"Hello world!");

// Poiché questi sono caratteri asiatici, questo run applicherà le nostre equivalenze di carattere/locale "FarEast".
builder->Writeln(u"你好世界");

doc->Save(get_ArtifactsDir() + u"Font.FarEast.docx");
```

## Vedi anche

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
