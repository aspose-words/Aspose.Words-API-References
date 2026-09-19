---
title: "Aspose::Words::Loading::LoadOptions::get_IgnoreOleData method"
linktitle: "get_IgnoreOleData"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Loading::LoadOptions::get_IgnoreOleData method. Specifica se ignorare i dati OLE in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.loading/loadoptions/get_ignoreoledata/
---
## LoadOptions::get_IgnoreOleData method


Specifica se ignorare i dati OLE.

```cpp
bool Aspose::Words::Loading::LoadOptions::get_IgnoreOleData() const
```

## Note


Ignorare i dati OLE può ridurre il consumo di memoria e aumentare le prestazioni senza perdita di dati nel caso in cui il formato di destinazione non supporti oggetti OLE.

Il valore predefinito è **false**.

## Esempi



Mostra come ignorare i dati OLE durante il caricamento.
```cpp
// Ignorare i dati OLE può ridurre il consumo di memoria e aumentare le prestazioni
// senza perdita di dati nel caso in cui il formato di destinazione non supporti oggetti OLE.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_IgnoreOleData(true);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"OLE objects.docx", loadOptions);

doc->Save(get_ArtifactsDir() + u"LoadOptions.IgnoreOleData.docx");
```

## Vedi anche

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
