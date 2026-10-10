---
title: "Método Aspose::Words::Style::get_Locked"
linktitle: "get_Locked"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Style::get_Locked. Especifica si este estilo está bloqueado en C++."
type: docs
weight: 13500
url: /es/cpp/aspose.words/style/get_locked/
---
## Style::get_Locked method


Especifica si este estilo está bloqueado.

```cpp
bool Aspose::Words::Style::get_Locked() const
```


## Ejemplos



Muestra cómo bloquear el estilo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> styleHeading1 = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Heading1);
if (!styleHeading1->get_Locked())
{
    styleHeading1->set_Locked(true);
}

doc->Save(get_ArtifactsDir() + u"Styles.LockStyle.docx");
```

## Ver también

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
