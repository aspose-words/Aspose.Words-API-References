---
title: "Metodo Aspose::Words::Drawing::ShapeBase::get_HRef"
linktitle: "get_HRef"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::ShapeBase::get_HRef. Ottiene o imposta l'indirizzo ipertestuale completo per una forma in C++."
type: docs
weight: 24000
url: /it/cpp/aspose.words.drawing/shapebase/get_href/
---
## ShapeBase::get_HRef method


Ottiene o imposta l'indirizzo completo del collegamento ipertestuale per una forma.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_HRef()
```

## Note


Il valore predefinito è una stringa vuota.

Di seguito sono riportati esempi di valori validi per questa proprietà:

URI completo: **https://www.aspose.com/**.

Nome file completo: **C:\\My Documents\\SalesReport.doc**.

URI relativo: **%../../../resource.txt**

Nome file relativo: **%..\\My Documents\\SalesReport.doc**.

[Bookmark](../../../aspose.words/bookmark/) within another document: **https://www.aspose.com/Products/Default.aspx::Suites**

[Bookmark](../../../aspose.words/bookmark/) within this document: **%#BookmakName**.

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
