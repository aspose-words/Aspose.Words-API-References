---
title: "Metodo Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer"
linktitle: "get_UseGdiEmfRenderer"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer. Ottiene o imposta un valore che determina se utilizzare il renderer di metafile GDI+ o quello di Aspose.Words durante il salvataggio in EMF in C++."
type: docs
weight: 18000
url: /it/cpp/aspose.words.saving/imagesaveoptions/get_usegdiemfrenderer/
---
## ImageSaveOptions::get_UseGdiEmfRenderer method


Ottiene o imposta un valore che determina se utilizzare GDI+ o Aspose.Words metafile renderer durante il salvataggio in EMF.

```cpp
bool Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer() const
```

## Note


Se impostato su **true**, viene utilizzato il renderer di metafile GDI+. Cioè il contenuto è scritto su un oggetto grafico GDI+ e salvato nel metafile.

Se impostato su **false**, viene utilizzato il renderer di metafile Aspose.Words. Cioè il contenuto è scritto direttamente nel formato metafile con Aspose.Words.

Ha effetto solo durante il salvataggio in EMF.

Il salvataggio GDI+ funziona solo su .NET.

Il valore predefinito è **true**.

## Esempi



Mostra come scegliere un renderer quando si converte un documento in .emf.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Quando salviamo il documento come immagine EMF, possiamo passare un oggetto SaveOptions per selezionare un renderer per l'immagine.
// Se impostiamo il flag "UseGdiEmfRenderer" su "true", Aspose.Words utilizzerà il renderer GDI+.
// Se impostiamo il flag "UseGdiEmfRenderer" su "false", Aspose.Words utilizzerà il proprio renderer di metafile.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Emf);
saveOptions->set_UseGdiEmfRenderer(useGdiEmfRenderer);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Renderer.emf", saveOptions);
```

## Vedi anche

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
