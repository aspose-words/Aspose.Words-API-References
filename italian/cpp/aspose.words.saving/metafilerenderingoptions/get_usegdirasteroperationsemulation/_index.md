---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation metodo"
linktitle: "get_UseGdiRasterOperationsEmulation"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation metodo. Ottiene o imposta un valore che determina se utilizzare o meno GDI+ per l'emulazione delle operazioni raster in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.saving/metafilerenderingoptions/get_usegdirasteroperationsemulation/
---
## MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation method


Ottiene o imposta un valore che determina se utilizzare o meno GDI+ per l'emulazione delle operazioni raster.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation() const
```

## Note


La libreria Windows GDI+ può essere utilizzata per emulare le operazioni raster. Fornisce supporto per tutte le operazioni raster rispetto all'emulazione propria di Aspose.Words, ma le prestazioni potrebbero essere più lente in alcuni casi.

Quando questo valore è impostato su **true**, Aspose.Words utilizza GDI+ per l'emulazione delle operazioni raster.

Quando questo valore è impostato su **false**, Aspose.Words utilizza la propria implementazione dell'emulazione delle operazioni raster.

Questa opzione è usata solo quando il metafile viene renderizzato come grafica vettoriale.

Il valore predefinito è **false**.

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

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
