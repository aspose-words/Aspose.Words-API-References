---
title: "Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix metodo"
linktitle: "get_IdPrefix"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix metodo. Specifica un prefisso che viene anteposto a tutti gli ID degli elementi generati nel documento di output. Il valore predefinito è null e nessun prefisso è anteposto in C++."
type: docs
weight: 4250
url: /it/cpp/aspose.words.saving/svgsaveoptions/get_idprefix/
---
## SvgSaveOptions::get_IdPrefix method


Specifica un prefisso che viene anteposto a tutti gli ID degli elementi generati nel documento di output. Il valore predefinito è null e nessun prefisso viene anteposto.

```cpp
System::String Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix() const
```


## Esempi



Mostra come aggiungere un prefisso che viene anteposto a tutti gli ID degli elementi generati (svg).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Id prefix.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
saveOptions->set_IdPrefix(u"pfx1_");

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.IdPrefixSvg.html", saveOptions);
```

## Vedi anche

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
