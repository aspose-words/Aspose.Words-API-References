---
title: "Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions metodo"
linktitle: "get_MetafileRenderingOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions metodo. Consente di specificare come i metafile vengono trattati nell'output renderizzato in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.saving/imagesaveoptions/get_metafilerenderingoptions/
---
## ImageSaveOptions::get_MetafileRenderingOptions method


Consente di specificare come i metafile vengono trattati nell'output renderizzato.

```cpp
System::SharedPtr<Aspose::Words::Saving::MetafileRenderingOptions> Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions()
```

## Note


Quando è specificato [Vector](../../metafilerenderingmode/), Aspose.Words renderizza il metafile in grafica vettoriale utilizzando prima il proprio motore di rendering dei metafile e poi renderizza la grafica vettoriale nell'immagine.

Quando è specificato [Bitmap](../../metafilerenderingmode/), Aspose.Words renderizza il metafile direttamente nell'immagine utilizzando il motore di rendering dei metafile GDI+.

Il motore di rendering dei metafile GDI+ è più veloce, supporta quasi tutte le funzionalità dei metafile ma a basse risoluzioni può produrre risultati incoerenti rispetto al resto della grafica vettoriale (soprattutto per il testo) nella pagina. Il motore di rendering dei metafile di Aspose.Words produrrà risultati più coerenti anche a basse risoluzioni, ma è più lento e può renderizzare in modo impreciso metafile complessi.

Il valore predefinito per [MetafileRenderingMode](../../metafilerenderingmode/) è [Bitmap](../../metafilerenderingmode/).

## Esempi



Mostra come impostare la modalità di rendering durante il salvataggio di documenti con immagini Windows Metafile in altri formati immagine.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf");

// Quando salviamo il documento come immagine, possiamo passare un oggetto SaveOptions a
// determina come l'operazione di salvataggio elaborerà i Windows Metafile nel documento.
// Se impostiamo la proprietà "RenderingMode" su "MetafileRenderingMode.Vector",
// oppure "MetafileRenderingMode.VectorWithFallback", renderizzeremo tutti i metafile come grafica vettoriale.
// Se impostiamo la proprietà "RenderingMode" su "MetafileRenderingMode.Bitmap", renderizzeremo tutti i metafile come bitmap.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
options->get_MetafileRenderingOptions()->set_RenderingMode(metafileRenderingMode);
// Aspose.Words utilizza GDI+ per l'emulazione delle operazioni raster, quando il valore è impostato su true.
options->get_MetafileRenderingOptions()->set_UseGdiRasterOperationsEmulation(true);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.WindowsMetaFile.png", options);
```

## Vedi anche

* Class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
