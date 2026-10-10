---
title: "Clase Aspose::Words::Layout::LayoutOptions"
linktitle: "LayoutOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Layout::LayoutOptions. Contiene las opciones que permiten controlar el proceso de diseño del documento. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.layout/layoutoptions/
---
## LayoutOptions class


Contiene las opciones que permiten controlar el proceso de diseño del documento. Para obtener más información, visite el artículo de documentación [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class LayoutOptions : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Callback](./get_callback/)() const | Obtiene la implementación de [IPageLayoutCallback](../ipagelayoutcallback/) utilizada por el modelo de diseño de página. |
| [get_CommentDisplayMode](./get_commentdisplaymode/)() const | Obtiene o establece la forma en que se renderizan los comentarios. El valor predeterminado es [ShowInBalloons](../commentdisplaymode/). |
| [get_ContinuousSectionPageNumberingRestart](./get_continuoussectionpagenumberingrestart/)() const | Obtiene o establece el modo de comportamiento para calcular los números de página cuando una sección continua reinicia la numeración de páginas. |
| [get_IgnorePrinterMetrics](./get_ignoreprintermetrics/)() const | Obtiene o establece la indicación de si se ignora la opción de compatibilidad "Usar métricas de impresora para diseñar el documento". El valor predeterminado es **true**. |
| [get_KeepOriginalFontMetrics](./get_keeporiginalfontmetrics/)() const | Obtiene o establece una indicación de si se deben usar las métricas de fuente originales después de la sustitución de fuentes. El valor predeterminado es **true**. |
| [get_RevisionOptions](./get_revisionoptions/)() const | Obtiene las opciones de revisión. |
| [get_ShowHiddenText](./get_showhiddentext/)() const | Obtiene o establece la indicación de si se renderiza el texto oculto en el documento. El valor predeterminado es **false**. |
| [get_ShowParagraphMarks](./get_showparagraphmarks/)() const | Obtiene o establece la indicación de si se renderizan los símbolos de párrafo. El valor predeterminado es **false**. |
| [get_TextShaperFactory](./get_textshaperfactory/)() const | Obtiene la implementación de [ITextShaperFactory](../) utilizada para funciones de renderizado de tipografía avanzada. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LayoutOptions](./layoutoptions/)() |  |
| [set_Callback](./set_callback/)(const System::SharedPtr\<Aspose::Words::Layout::IPageLayoutCallback\>\&) | Establece la implementación de [IPageLayoutCallback](../ipagelayoutcallback/) utilizada por el modelo de diseño de página. |
| [set_CommentDisplayMode](./set_commentdisplaymode/)(Aspose::Words::Layout::CommentDisplayMode) | Establecedor de [Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode](./get_commentdisplaymode/). |
| [set_ContinuousSectionPageNumberingRestart](./set_continuoussectionpagenumberingrestart/)(Aspose::Words::Layout::ContinuousSectionRestart) | Establecedor de [Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart](./get_continuoussectionpagenumberingrestart/). |
| [set_IgnorePrinterMetrics](./set_ignoreprintermetrics/)(bool) | Establecedor de [Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics](./get_ignoreprintermetrics/). |
| [set_KeepOriginalFontMetrics](./set_keeporiginalfontmetrics/)(bool) | Establecedor de [Aspose::Words::Layout::LayoutOptions::get_KeepOriginalFontMetrics](./get_keeporiginalfontmetrics/). |
| [set_ShowHiddenText](./set_showhiddentext/)(bool) | Establecedor de [Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText](./get_showhiddentext/). |
| [set_ShowParagraphMarks](./set_showparagraphmarks/)(bool) | Establecedor de [Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks](./get_showparagraphmarks/). |
| [set_TextShaperFactory](./set_textshaperfactory/)(const System::SharedPtr\<Aspose::Words::Shaping::ITextShaperFactory\>\&) | Establece la implementación de [ITextShaperFactory](../) utilizada para funciones de renderizado de tipografía avanzada. |
| static [Type](./type/)() |  |
## Observaciones


No crea instancias de esta clase directamente. Utilice la propiedad [LayoutOptions](../../aspose.words/document/get_layoutoptions/) para acceder a las opciones de diseño de este documento.

Tenga en cuenta que después de cambiar cualquiera de las opciones presentes en esta clase, se debe llamar al método [UpdatePageLayout](../../aspose.words/document/updatepagelayout/) para que las opciones modificadas se apliquen al diseño.

## Ejemplos



Muestra cómo ocultar texto en un documento de salida renderizado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte texto oculto, luego especifique si deseamos omitirlo de un documento renderizado.
builder->Writeln(u"This text is not hidden.");
builder->get_Font()->set_Hidden(true);
builder->Writeln(u"This text is hidden.");

doc->get_LayoutOptions()->set_ShowHiddenText(showHiddenText);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsHiddenText.pdf");
```


Muestra cómo mostrar los símbolos de párrafo en un documento de salida renderizado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Agregue algunos párrafos, luego habilite los símbolos de párrafo para mostrar los finales de los párrafos
// con un símbolo de párrafo (¶) cuando renderizamos el documento.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

doc->get_LayoutOptions()->set_ShowParagraphMarks(showParagraphMarks);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsParagraphMarks.pdf");
```


Muestra cómo alterar la apariencia de las revisiones en un documento de salida renderizado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte una revisión, luego cambie el color de todas las revisiones a verde.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// Elimine la barra que aparece a la izquierda de cada línea revisada.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## Ver también

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
