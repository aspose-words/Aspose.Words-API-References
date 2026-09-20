---
title: "Aspose::Words::Comparing::CompareOptions clase"
linktitle: "CompareOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Comparing::CompareOptions clase. Permite elegir opciones adicionales para la operación de comparación de documentos. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 1000
url: /es/cpp/aspose.words.comparing/compareoptions/
---
## CompareOptions class


Permite elegir opciones adicionales para la operación de comparación de documentos. Para obtener más información, visite el artículo de documentación [Compare Documents](https://docs.aspose.com/words/cpp/compare-documents/).

```cpp
class CompareOptions : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [CompareOptions](./compareoptions/)() |  |
| [get_AdvancedOptions](./get_advancedoptions/)() const | Especifica opciones avanzadas de comparación que pueden ayudar a producir una salida de comparación más precisa. |
| [get_CompareMoves](./get_comparemoves/)() const | Especifica si se deben comparar las diferencias entre los dos documentos. |
| [get_Granularity](./get_granularity/)() const | Especifica si los cambios se rastrean por carácter o por palabra. |
| [get_IgnoreCaseChanges](./get_ignorecasechanges/)() const | True indica que la comparación de documentos no distingue entre mayúsculas y minúsculas. |
| [get_IgnoreComments](./get_ignorecomments/)() const | Especifica si se deben comparar las diferencias en los comentarios. |
| [get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/)() | Especifica si se debe ignorar la diferencia en el Id único de DrawingML. |
| [get_IgnoreFields](./get_ignorefields/)() const | Especifica si se deben comparar las diferencias en los campos. |
| [get_IgnoreFootnotes](./get_ignorefootnotes/)() const | Especifica si se deben comparar las diferencias en notas al pie y notas finales. |
| [get_IgnoreFormatting](./get_ignoreformatting/)() const | True indica que el formato se ignora. |
| [get_IgnoreHeadersAndFooters](./get_ignoreheadersandfooters/)() const | True indica que el contenido de encabezados y pies de página se ignora. |
| [get_IgnoreTables](./get_ignoretables/)() const | Especifica si se deben comparar las diferencias en los datos contenidos en tablas. |
| [get_IgnoreTextboxes](./get_ignoretextboxes/)() const | Especifica si se deben comparar las diferencias en los datos contenidos dentro de los cuadros de texto. |
| [get_Target](./get_target/)() const | Especifica qué documento se debe usar como objetivo durante la comparación. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CompareMoves](./set_comparemoves/)(bool) | Establecedor para [Aspose::Words::Comparing::CompareOptions::get_CompareMoves](./get_comparemoves/). |
| [set_Granularity](./set_granularity/)(Aspose::Words::Comparing::Granularity) | Establecedor para [Aspose::Words::Comparing::CompareOptions::get_Granularity](./get_granularity/). |
| [set_IgnoreCaseChanges](./set_ignorecasechanges/)(bool) | Establecedor para [Aspose::Words::Comparing::CompareOptions::get_IgnoreCaseChanges](./get_ignorecasechanges/). |
| [set_IgnoreComments](./set_ignorecomments/)(bool) | Establecedor para [Aspose::Words::Comparing::CompareOptions::get_IgnoreComments](./get_ignorecomments/). |
| [set_IgnoreDmlUniqueId](./set_ignoredmluniqueid/)(bool) | Establecedor para [Aspose::Words::Comparing::CompareOptions::get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/). |
| [set_IgnoreFields](./set_ignorefields/)(bool) | Establecedor para [Aspose::Words::Comparing::CompareOptions::get_IgnoreFields](./get_ignorefields/). |
| [set_IgnoreFootnotes](./set_ignorefootnotes/)(bool) | Establecedor para [Aspose::Words::Comparing::CompareOptions::get_IgnoreFootnotes](./get_ignorefootnotes/). |
| [set_IgnoreFormatting](./set_ignoreformatting/)(bool) | Establecedor para [Aspose::Words::Comparing::CompareOptions::get_IgnoreFormatting](./get_ignoreformatting/). |
| [set_IgnoreHeadersAndFooters](./set_ignoreheadersandfooters/)(bool) | Método setter para [Aspose::Words::Comparing::CompareOptions::get_IgnoreHeadersAndFooters](./get_ignoreheadersandfooters/). |
| [set_IgnoreTables](./set_ignoretables/)(bool) | Método setter para [Aspose::Words::Comparing::CompareOptions::get_IgnoreTables](./get_ignoretables/). |
| [set_IgnoreTextboxes](./set_ignoretextboxes/)(bool) | Método setter para [Aspose::Words::Comparing::CompareOptions::get_IgnoreTextboxes](./get_ignoretextboxes/). |
| [set_Target](./set_target/)(Aspose::Words::Comparing::ComparisonTargetType) | Método setter para [Aspose::Words::Comparing::CompareOptions::get_Target](./get_target/). |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo filtrar tipos específicos de elementos del documento al realizar una comparación.
```cpp
// Cree el documento original y llénelo con varios tipos de elementos.
auto docOriginal = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docOriginal);

// Texto del párrafo referenciado con una nota al final:
builder->Writeln(u"Hello world! This is the first paragraph.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Original endnote text.");

// Tabla:
builder->StartTable();
builder->InsertCell();
builder->Write(u"Original cell 1 text");
builder->InsertCell();
builder->Write(u"Original cell 2 text");
builder->EndTable();

// Cuadro de texto:
System::SharedPtr<Aspose::Words::Drawing::Shape> textBox = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 20);
builder->MoveTo(textBox->get_FirstParagraph());
builder->Write(u"Original textbox contents");

// Campo DATE:
builder->MoveTo(docOriginal->get_FirstSection()->get_Body()->AppendParagraph(u""));
builder->InsertField(u" DATE ");

// Comentario:
auto newComment = System::MakeObject<Aspose::Words::Comment>(docOriginal, u"John Doe", u"J.D.", System::DateTime::get_Now());
newComment->SetText(u"Original comment.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(newComment);

// Encabezado:
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"Original header contents.");

// Cree una copia de nuestro documento y realice una edición rápida en cada uno de los elementos del documento clonado.
auto docEdited = System::ExplicitCast<Aspose::Words::Document>(System::ExplicitCast<Aspose::Words::Node>(docOriginal)->Clone(true));
System::SharedPtr<Aspose::Words::Paragraph> firstParagraph = docEdited->get_FirstSection()->get_Body()->get_FirstParagraph();

firstParagraph->get_Runs()->idx_get(0)->set_Text(u"hello world! this is the first paragraph, after editing.");
firstParagraph->get_ParagraphFormat()->set_Style(docEdited->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Heading1));
(System::ExplicitCast<Aspose::Words::Notes::Footnote>(docEdited->GetChild(Aspose::Words::NodeType::Footnote, 0, true)))->get_FirstParagraph()->get_Runs()->idx_get(1)->set_Text(u"Edited endnote text.");
(System::ExplicitCast<Aspose::Words::Tables::Table>(docEdited->GetChild(Aspose::Words::NodeType::Table, 0, true)))->get_FirstRow()->get_Cells()->idx_get(1)->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Edited Cell 2 contents");
(System::ExplicitCast<Aspose::Words::Drawing::Shape>(docEdited->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Edited textbox contents");
(System::ExplicitCast<Aspose::Words::Fields::FieldDate>(docEdited->get_Range()->get_Fields()->idx_get(0)))->set_UseLunarCalendar(true);
(System::ExplicitCast<Aspose::Words::Comment>(docEdited->GetChild(Aspose::Words::NodeType::Comment, 0, true)))->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Edited comment.");
docEdited->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Edited header contents.");

// Comparar documentos crea una revisión por cada edición en el documento editado.
// Un objeto CompareOptions tiene una serie de indicadores que pueden suprimir revisiones
// en cada tipo respectivo de elemento, ignorando efectivamente su cambio.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->set_CompareMoves(false);
compareOptions->set_IgnoreFormatting(false);
compareOptions->set_IgnoreCaseChanges(false);
compareOptions->set_IgnoreComments(false);
compareOptions->set_IgnoreTables(false);
compareOptions->set_IgnoreFields(false);
compareOptions->set_IgnoreFootnotes(false);
compareOptions->set_IgnoreTextboxes(false);
compareOptions->set_IgnoreHeadersAndFooters(false);
compareOptions->set_Target(Aspose::Words::Comparing::ComparisonTargetType::New);

docOriginal->Compare(docEdited, u"John Doe", System::DateTime::get_Now(), compareOptions);
docOriginal->Save(get_ArtifactsDir() + u"Revision.CompareOptions.docx");
```

## Ver también

* Namespace [Aspose::Words::Comparing](../)
* Library [Aspose.Words for C++](../../)
