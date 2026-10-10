---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize metodo"
linktitle: "get_ScaleImageToShapeSize"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize metodo. Specifica se le immagini vengono scalate da Aspose.Words alla dimensione della forma contenente durante l'esportazione in HTML, MHTML o EPUB. Il valore predefinito è true in C++."
type: docs
weight: 46000
url: /it/cpp/aspose.words.saving/htmlsaveoptions/get_scaleimagetoshapesize/
---
## HtmlSaveOptions::get_ScaleImageToShapeSize method


Specifica se le immagini vengono ridimensionate da Aspose.Words alle dimensioni della forma di contenimento durante l'esportazione in HTML, MHTML o EPUB. Il valore predefinito è **true**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize() const
```

## Note


Un'immagine in un documento Microsoft Word è una forma. La forma ha una dimensione e l'immagine ha la sua dimensione. Le dimensioni non sono direttamente collegate. Per esempio, l'immagine può essere 1024x786 pixel, ma la forma che visualizza questa immagine può essere 400x300 punti.

Per visualizzare un'immagine nel browser, deve essere scalata alla dimensione della forma. La proprietà [ScaleImageToShapeSize](./) controlla dove avviene il ridimensionamento dell'immagine: in Aspose.Words durante l'esportazione in HTML o nel browser durante la visualizzazione del documento.

Quando [ScaleImageToShapeSize](./) è **true**, l'immagine viene scalata da [Aspose.Words](../../../aspose.words/) utilizzando un ridimensionamento ad alta qualità durante l'esportazione in HTML. Quando [ScaleImageToShapeSize](./) è **false**, l'immagine viene esportata con la sua dimensione originale e il browser deve scalarla.

In generale, i browser effettuano un ridimensionamento rapido e di scarsa qualità. Di conseguenza, otterrai normalmente una migliore qualità di visualizzazione nel browser e un file più piccolo quando [ScaleImageToShapeSize](./) è **true**, ma una migliore qualità di stampa e una conversione più veloce quando [ScaleImageToShapeSize](./) è **false**.

Oltre alle forme contenenti immagini raster individuali, questa opzione influisce anche sulle forme di gruppo composte da immagini raster. Se [ScaleImageToShapeSize](./) è **false** e una forma di gruppo contiene immagini raster la cui risoluzione intrinseca è superiore al valore specificato in [ImageResolution](../get_imageresolution/), Aspose.Words aumenterà la risoluzione di rendering per quel gruppo. Questo consente di preservare meglio la qualità delle immagini ad alta risoluzione raggruppate durante il salvataggio in HTML.

## Vedi anche

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
