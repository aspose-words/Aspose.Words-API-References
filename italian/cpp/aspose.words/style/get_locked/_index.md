---
title: "Metodo Aspose::Words::Style::get_Locked"
linktitle: "get_Locked"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Style::get_Locked. Specifica se questo stile è bloccato in C++."
type: docs
weight: 13500
url: /it/cpp/aspose.words/style/get_locked/
---
## Style::get_Locked method


Specifica se questo stile è bloccato.

```cpp
bool Aspose::Words::Style::get_Locked() const
```


## Esempi



Mostra come bloccare lo stile.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> styleHeading1 = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Heading1);
if (!styleHeading1->get_Locked())
{
    styleHeading1->set_Locked(true);
}

doc->Save(get_ArtifactsDir() + u"Styles.LockStyle.docx");
```

## Vedi anche

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
