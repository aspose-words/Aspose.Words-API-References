---
title: "Metodo Aspose::Words::Drawing::ShapeBase::get_Name"
linktitle: "get_Name"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::ShapeBase::get_Name. Ottiene o imposta il nome opzionale della forma in C++."
type: docs
weight: 40000
url: /it/cpp/aspose.words.drawing/shapebase/get_name/
---
## ShapeBase::get_Name method


Ottiene o imposta il nome opzionale della forma.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_Name()
```

## Note


Il valore predefinito è una stringa vuota.

Non può essere **null**, ma può essere una stringa vuota.

## Esempi



Mostra come usare il testo alternativo di una forma.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 150, 150);
shape->set_Name(u"MyCube");

shape->set_AlternativeText(u"Alt text for MyCube.");

// Possiamo accedere al testo alternativo di una forma facendo clic destro su di essa, e poi tramite "Format AutoShape" -> "Alt Text".
doc->Save(get_ArtifactsDir() + u"Shape.AltText.docx");

// Salva il documento in HTML, quindi elimina l'immagine collegata che appartiene alla nostra forma.
// Il browser che legge il nostro HTML visualizzerà il testo alt al posto dell'immagine mancante.
doc->Save(get_ArtifactsDir() + u"Shape.AltText.html");
System::IO::File::Delete(get_ArtifactsDir() + u"Shape.AltText.001.png");
```

## Vedi anche

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
