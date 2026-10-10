---
title: "Metodo Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins"
linktitle: "get_ExportPageMargins"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins. Specifica se i margini di pagina vengono esportati in HTML, MHTML o EPUB. Il valore predefinito è false in C++."
type: docs
weight: 23000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_exportpagemargins/
---
## HtmlSaveOptions::get_ExportPageMargins method


Specifica se i margini della pagina vengono esportati in HTML, MHTML o EPUB. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins() const
```


## Esempi



Mostra come visualizzare gli oggetti fuori dai limiti nei documenti HTML di output.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Utilizza un builder per inserire una forma senza avvolgimento.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 200, 200);

shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Valori negativi della posizione della forma possono posizionare la forma al di fuori dei limiti della pagina.
// Se esportiamo questo in HTML, la forma apparirà troncata.
shape->set_Left(-150);

// Quando si salva il documento in HTML, possiamo passare un oggetto SaveOptions
// per decidere se regolare la pagina per visualizzare completamente gli oggetti fuori dai limiti.
// Se impostiamo il flag "ExportPageMargins" su "true", la forma sarà completamente visibile nell'HTML di output.
// Se impostiamo il flag "ExportPageMargins" su "false",
// il nostro documento visualizzerà la forma troncata come la vedremmo in Microsoft Word.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportPageMargins(exportPageMargins);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageMargins.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportPageMargins.html");

if (exportPageMargins)
{
    ASSERT_TRUE(outDocContents.Contains(u"<style type=\"text/css\">div.Section_1 { margin:70.85pt }</style>"));
    ASSERT_TRUE(outDocContents.Contains(u"<div class=\"Section_1\"><p style=\"margin-top:0pt; margin-left:150pt; margin-bottom:0pt\">"));
}
else
{
    ASSERT_FALSE(outDocContents.Contains(u"style type=\"text/css\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<div><p style=\"margin-top:0pt; margin-left:220.85pt; margin-bottom:0pt\">"));
}
```

## Vedi anche

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
