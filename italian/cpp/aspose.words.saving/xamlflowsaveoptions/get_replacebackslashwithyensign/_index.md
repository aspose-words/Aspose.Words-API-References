---
title: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign metodo"
linktitle: "get_ReplaceBackslashWithYenSign"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign metodo. Specifica se i caratteri backslash devono essere sostituiti con i simboli yen. Il valore predefinito è false in C++."
type: docs
weight: 5500
url: /it/cpp/aspose.words.saving/xamlflowsaveoptions/get_replacebackslashwithyensign/
---
## XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign method


Specifica se i caratteri backslash devono essere sostituiti con i simboli yen. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Saving::XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign() const
```


## Esempi



Mostra come sostituire i caratteri backslash con i simboli yen (Xaml).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Korean backslash symbol.docx");

// Per impostazione predefinita, Aspose.Words imita il comportamento di MS Word e non sostituisce i caratteri backslash con il simbolo yen in
// documenti HTML generati. Tuttavia, le versioni precedenti di Aspose.Words eseguivano tali sostituzioni in determinate
// scenari. Questa opzione consente la retrocompatibilità con le versioni precedenti di Aspose.Words.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::XamlFlowSaveOptions>();
saveOptions->set_ReplaceBackslashWithYenSign(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ReplaceBackslashWithYenSign.xaml", saveOptions);
```

## Vedi anche

* Class [XamlFlowSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
