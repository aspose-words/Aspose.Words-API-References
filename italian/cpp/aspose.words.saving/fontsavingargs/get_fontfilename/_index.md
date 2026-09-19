---
title: "Aspose::Words::Saving::FontSavingArgs::get_FontFileName metodo"
linktitle: "get_FontFileName"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::FontSavingArgs::get_FontFileName metodo. Ottiene o imposta il nome file (senza percorso) dove il carattere verrà salvato in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.saving/fontsavingargs/get_fontfilename/
---
## FontSavingArgs::get_FontFileName method


Ottiene o imposta il nome del file (senza percorso) dove il carattere verrà salvato.

```cpp
System::String Aspose::Words::Saving::FontSavingArgs::get_FontFileName() const
```

## Note


Questa proprietà consente di ridefinire come vengono generati i nomi dei file dei caratteri durante l'esportazione in HTML.

Quando l'evento viene attivato, questa proprietà contiene il nome file generato da Aspose.Words. È possibile modificare il valore di questa proprietà per salvare il carattere in un file diverso. Nota che i nomi dei file devono essere unici.

Aspose.Words genera automaticamente un nome file univoco per ogni carattere incorporato durante l'esportazione in formato HTML. Il modo in cui il nome file del carattere viene generato dipende dal fatto che il documento venga salvato su un file o su uno stream.

Quando si salva un documento su un file, il nome file del carattere generato appare così *%<document base file name>.<original file name><optional suffix>.<extension>*.

Quando si salva un documento su uno stream, il nome file del carattere generato appare così *Aspose.Words.<document guid>.<original file name><optional suffix>.<extension>*.

[FontFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name, the [FontsFolder](../../htmlsaveoptions/get_fontsfolder/) and [FontsFolderAlias](../../htmlsaveoptions/get_fontsfolderalias/) properties.

## Vedi anche

* Class [FontSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
