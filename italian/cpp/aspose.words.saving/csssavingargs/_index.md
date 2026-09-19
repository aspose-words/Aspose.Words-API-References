---
title: "Aspose::Words::Saving::CssSavingArgs classe"
linktitle: "CssSavingArgs"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::CssSavingArgs classe. Fornisce i dati per l'evento CssSaving(). Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.saving/csssavingargs/
---
## CssSavingArgs class


Fornisce i dati per l'evento [CssSaving()](../icsssavingcallback/csssaving/). Per saperne di più, visita l'articolo di documentazione [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class CssSavingArgs : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_CssStream](./get_cssstream/)() const | Consente di specificare lo stream in cui verranno salvate le informazioni CSS. |
| [get_Document](./get_document/)() const | Ottiene l'oggetto documento che è attualmente in fase di salvataggio. |
| [get_IsExportNeeded](./get_isexportneeded/)() const | Consente di specificare se il CSS sarà esportato in un file e incorporato nel documento HTML. Il valore predefinito è **true**. Quando questa proprietà è **false**, le informazioni CSS non verranno salvate in un file CSS e non saranno incorporate nel documento HTML. |
| [get_KeepCssStreamOpen](./get_keepcssstreamopen/)() const | Specifica se Aspose.Words deve mantenere lo stream aperto o chiuderlo dopo aver salvato le informazioni CSS. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CssStream](./set_cssstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Impostatore per [Aspose::Words::Saving::CssSavingArgs::get_CssStream](./get_cssstream/). |
| [set_CssStream](./set_cssstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_IsExportNeeded](./set_isexportneeded/)(bool) | Consente di specificare se il CSS sarà esportato in un file e incorporato nel documento HTML. Il valore predefinito è **true**. Quando questa proprietà è **false**, le informazioni CSS non verranno salvate in un file CSS e non saranno incorporate nel documento HTML. |
| [set_KeepCssStreamOpen](./set_keepcssstreamopen/)(bool) | Impostatore per [Aspose::Words::Saving::CssSavingArgs::get_KeepCssStreamOpen](./get_keepcssstreamopen/). |
| static [Type](./type/)() |  |
## Note


Per impostazione predefinita, quando Aspose.Words salva un documento in HTML, salva le informazioni CSS in linea (come valore dell'attributo **style** su ogni elemento).

[CssSavingArgs](./) allows to save CSS information into file by providing your own stream object.

Per salvare il CSS nello stream, utilizza la proprietà [CssStream](./get_cssstream/).

Per sopprimere il salvataggio del CSS in un file e l'incorporamento nel documento HTML, utilizza la proprietà [IsExportNeeded](./get_isexportneeded/).
## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
