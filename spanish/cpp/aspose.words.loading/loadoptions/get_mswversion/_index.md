---
title: "Aspose::Words::Loading::LoadOptions::get_MswVersion method"
linktitle: "get_MswVersion"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Loading::LoadOptions::get_MswVersion method. Permite especificar que el proceso de carga del documento debe coincidir con una versión específica de MS Word. El valor predeterminado es Word2019 en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words.loading/loadoptions/get_mswversion/
---
## LoadOptions::get_MswVersion method


Permite especificar que el proceso de carga del documento debe coincidir con una versión específica de MS Word. El valor predeterminado es [Word2019](../../../aspose.words.settings/mswordversion/)

```cpp
Aspose::Words::Settings::MsWordVersion Aspose::Words::Loading::LoadOptions::get_MswVersion() const
```


## Ejemplos



Muestra cómo emular el procedimiento de carga de una versión específica de Microsoft Word durante la carga del documento.
```cpp
// Por defecto, Aspose.Words carga documentos según la especificación de Microsoft Word 2019.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();

ASSERT_EQ(Aspose::Words::Settings::MsWordVersion::Word2019, loadOptions->get_MswVersion());

// Este documento carece del estilo de formato de párrafo predeterminado.
// Este estilo predeterminado se regenerará cuando carguemos el documento ya sea con Microsoft Word o Aspose.Words.
loadOptions->set_MswVersion(Aspose::Words::Settings::MsWordVersion::Word2007);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", loadOptions);

// El interlineado del estilo tendrá este valor cuando se cargue según la especificación de Microsoft Word 2007.
ASSERT_NEAR(12.95, doc->get_Styles()->get_DefaultParagraphFormat()->get_LineSpacing(), 0.01);
```

## Ver también

* Enum [MsWordVersion](../../../aspose.words.settings/mswordversion/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
