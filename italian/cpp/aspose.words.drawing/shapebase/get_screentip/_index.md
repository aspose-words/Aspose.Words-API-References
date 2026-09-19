---
title: "Aspose::Words::Drawing::ShapeBase::get_ScreenTip metodo"
linktitle: "get_ScreenTip"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ShapeBase::get_ScreenTip metodo. Definisce il testo visualizzato quando il puntatore del mouse si sposta sopra la shape in C++."
type: docs
weight: 46000
url: /it/cpp/aspose.words.drawing/shapebase/get_screentip/
---
## ShapeBase::get_ScreenTip method


Definisce il testo visualizzato quando il puntatore del mouse si sposta sopra la forma.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_ScreenTip()
```

## Note


Il valore predefinito è una stringa vuota.

## Esempi



Mostra come inserire una forma che contiene un'immagine ed è anche un collegamento ipertestuale.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_HRef(u"https://forum.aspose.com/");
shape->set_Target(u"New Window");
shape->set_ScreenTip(u"Aspose.Words Support Forums");

// Ctrl + clic sinistro sulla forma in Microsoft Word aprirà una nuova finestra del browser web
// e ci porterà al collegamento ipertestuale nella proprietà "HRef".
doc->Save(get_ArtifactsDir() + u"Image.InsertImageWithHyperlink.docx");
```

## Vedi anche

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
