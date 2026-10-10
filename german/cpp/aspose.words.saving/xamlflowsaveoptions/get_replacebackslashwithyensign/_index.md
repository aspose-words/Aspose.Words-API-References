---
title: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign Methode"
linktitle: "get_ReplaceBackslashWithYenSign"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign Methode. Gibt an, ob Rückwärtsschrägstrich‑Zeichen durch Yen‑Zeichen ersetzt werden sollen. Der Standardwert ist false in C++."
type: docs
weight: 5500
url: /de/cpp/aspose.words.saving/xamlflowsaveoptions/get_replacebackslashwithyensign/
---
## XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign method


Gibt an, ob Rückwärtsschrägstriche durch Yen‑Zeichen ersetzt werden sollen. Standardwert ist **false**.

```cpp
bool Aspose::Words::Saving::XamlFlowSaveOptions::get_ReplaceBackslashWithYenSign() const
```


## Beispiele



Zeigt, wie Rückwärtsschrägstrich‑Zeichen durch Yen‑Zeichen (Xaml) ersetzt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Korean backslash symbol.docx");

// Standardmäßig ahmt Aspose.Words das Verhalten von MS Word nach und ersetzt Backslash‑Zeichen nicht durch Yen‑Zeichen in
// generierten HTML‑Dokumenten. Frühere Versionen von Aspose.Words führten solche Ersetzungen jedoch in bestimmten
// Szenarien durch. Dieses Flag ermöglicht die Abwärtskompatibilität mit früheren Versionen von Aspose.Words.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::XamlFlowSaveOptions>();
saveOptions->set_ReplaceBackslashWithYenSign(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ReplaceBackslashWithYenSign.xaml", saveOptions);
```

## Siehe auch

* Class [XamlFlowSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
