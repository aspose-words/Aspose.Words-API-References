---
title: "Aspose::Words::Saving::CssSavingArgs::get_CssStream metodo"
linktitle: "get_CssStream"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::CssSavingArgs::get_CssStream metodo. Consente di specificare lo stream dove le informazioni CSS verranno salvate in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.saving/csssavingargs/get_cssstream/
---
## CssSavingArgs::get_CssStream method


Consente di specificare lo stream in cui verranno salvate le informazioni CSS.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::CssSavingArgs::get_CssStream() const
```

## Note


Questa proprietà consente di salvare le informazioni CSS in uno stream.

Il valore predefinito è **null**. Questa proprietà non impedisce il salvataggio delle informazioni CSS in un file o l'incorporamento nel documento HTML. Per sopprimere l'esportazione del CSS utilizzare la proprietà [IsExportNeeded](../get_isexportneeded/).

Utilizzando [ICssSavingCallback](../../icsssavingcallback/) non è possibile sostituire il CSS con un altro. È destinato solo al salvataggio del CSS in uno stream.

## Vedi anche

* Class [CssSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
