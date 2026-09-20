---
title: "Método Aspose::Words::Layout::RevisionOptions::get_RevisionBarsColor"
linktitle: "get_RevisionBarsColor"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Layout::RevisionOptions::get_RevisionBarsColor. Permite especificar el color que se usará para las barras laterales que identifican las líneas del documento que contienen información revisada. El valor predeterminado es Red en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words.layout/revisionoptions/get_revisionbarscolor/
---
## RevisionOptions::get_RevisionBarsColor method


Permite especificar el color que se usará para las barras laterales que identifican las líneas del documento que contienen información revisada. El valor predeterminado es [Red](../../revisioncolor/).

```cpp
Aspose::Words::Layout::RevisionColor Aspose::Words::Layout::RevisionOptions::get_RevisionBarsColor() const
```


## Ejemplos



Muestra cómo modificar la apariencia de las revisiones.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

// Obtenga el objeto RevisionOptions que controla la apariencia de las revisiones.
System::SharedPtr<Aspose::Words::Layout::RevisionOptions> revisionOptions = doc->get_LayoutOptions()->get_RevisionOptions();

// Renderice las revisiones de inserción en verde y cursiva.
revisionOptions->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::Green);
revisionOptions->set_InsertedTextEffect(Aspose::Words::Layout::RevisionTextEffect::Italic);

// Renderice las revisiones de eliminación en rojo y negrita.
revisionOptions->set_DeletedTextColor(Aspose::Words::Layout::RevisionColor::Red);
revisionOptions->set_DeletedTextEffect(Aspose::Words::Layout::RevisionTextEffect::Bold);

// El mismo texto aparecerá dos veces en una revisión de movimiento:
// una vez en el punto de partida y una vez en el destino de llegada.
// Renderice el texto en la revisión de origen en amarillo con un doble tachado
// y azul doblemente subrayado en la revisión de destino.
revisionOptions->set_MovedFromTextColor(Aspose::Words::Layout::RevisionColor::Yellow);
revisionOptions->set_MovedFromTextEffect(Aspose::Words::Layout::RevisionTextEffect::DoubleStrikeThrough);
revisionOptions->set_MovedToTextColor(Aspose::Words::Layout::RevisionColor::ClassicBlue);
revisionOptions->set_MovedToTextEffect(Aspose::Words::Layout::RevisionTextEffect::DoubleUnderline);

// Renderice las revisiones de formato en rojo oscuro y negrita.
revisionOptions->set_RevisedPropertiesColor(Aspose::Words::Layout::RevisionColor::DarkRed);
revisionOptions->set_RevisedPropertiesEffect(Aspose::Words::Layout::RevisionTextEffect::Bold);

// Coloque una barra gruesa azul oscuro en el lado izquierdo de la página junto a las líneas afectadas por revisiones.
revisionOptions->set_RevisionBarsColor(Aspose::Words::Layout::RevisionColor::DarkBlue);
revisionOptions->set_RevisionBarsWidth(15.0f);

// Muestre marcas de revisión y texto original.
revisionOptions->set_ShowOriginalRevision(true);
revisionOptions->set_ShowRevisionMarks(true);

// Obtenga revisiones de movimiento, eliminación, formato y comentarios para que aparezcan en globos verdes
// en el lado derecho de la página.
revisionOptions->set_ShowInBalloons(Aspose::Words::Layout::ShowInBalloons::Format);
revisionOptions->set_CommentColor(Aspose::Words::Layout::RevisionColor::BrightGreen);

// Estas características solo se aplican a formatos como .pdf o .jpg.
doc->Save(get_ArtifactsDir() + u"Revision.RevisionOptions.pdf");
```

## Ver también

* Enum [RevisionColor](../../revisioncolor/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
