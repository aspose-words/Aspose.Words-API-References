---
title: "Metodo Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix"
linktitle: "get_IdPrefix"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix. Specifica un prefisso che viene anteposto a tutti gli ID degli elementi generati nel documento di output. Il valore predefinito è null e nessun prefisso viene anteposto in C++."
type: docs
weight: 10500
url: /it/cpp/aspose.words.saving/htmlfixedsaveoptions/get_idprefix/
---
## HtmlFixedSaveOptions::get_IdPrefix method


Specifica un prefisso che viene anteposto a tutti gli ID degli elementi generati nel documento di output. Il valore predefinito è null e nessun prefisso viene anteposto.

```cpp
System::String Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix() const
```


## Esempi



Mostra come aggiungere un prefisso che viene anteposto a tutti gli ID degli elementi generati.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Id prefix.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
saveOptions->set_IdPrefix(u"pfx1_");

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.IdPrefix.html", saveOptions);
```

## Vedi anche

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
