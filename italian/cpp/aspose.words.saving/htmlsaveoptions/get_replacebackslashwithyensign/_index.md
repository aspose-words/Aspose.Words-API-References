---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ReplaceBackslashWithYenSign method"
linktitle: "get_ReplaceBackslashWithYenSign"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ReplaceBackslashWithYenSign method. Specifica se i caratteri backslash devono essere sostituiti con il simbolo yen. Il valore predefinito è false in C++."
type: docs
weight: 41500
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_replacebackslashwithyensign/
---
## HtmlSaveOptions::get_ReplaceBackslashWithYenSign method


Specifica se i caratteri backslash devono essere sostituiti con i simboli yen. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ReplaceBackslashWithYenSign() const
```


## Esempi



Mostra come sostituire i caratteri backslash con il simbolo yen (Html).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Korean backslash symbol.docx");

// Per impostazione predefinita, Aspose.Words imita il comportamento di MS Word e non sostituisce i caratteri backslash con il simbolo yen in
// documenti HTML generati. Tuttavia, le versioni precedenti di Aspose.Words eseguivano tali sostituzioni in determinate
// scenari. Questa opzione consente la retrocompatibilità con le versioni precedenti di Aspose.Words.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_ReplaceBackslashWithYenSign(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ReplaceBackslashWithYenSign.html", saveOptions);
```

## Vedi anche

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
