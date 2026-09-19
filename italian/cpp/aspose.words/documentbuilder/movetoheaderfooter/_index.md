---
title: "Aspose::Words::DocumentBuilder::MoveToHeaderFooter metodo"
linktitle: "MoveToHeaderFooter"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentBuilder::MoveToHeaderFooter metodo. Sposta il cursore all'inizio di un'intestazione o di un piè di pagina nella sezione corrente in C++."
type: docs
weight: 57000
url: /it/cpp/aspose.words/documentbuilder/movetoheaderfooter/
---
## DocumentBuilder::MoveToHeaderFooter method


Sposta il cursore all'inizio di un'intestazione o di un piè di pagina nella sezione corrente.

```cpp
void Aspose::Words::DocumentBuilder::MoveToHeaderFooter(Aspose::Words::HeaderFooterType headerFooterType)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| headerFooterType | Aspose::Words::HeaderFooterType | Specifica l'intestazione o il piè di pagina a cui spostarsi. |
## Note


Dopo aver spostato il cursore in un'intestazione o in un piè di pagina, puoi utilizzare il resto dei metodi di [DocumentBuilder](../) per modificare il contenuto dell'intestazione o del piè di pagina.

Se desideri creare intestazioni e piè di pagina diversi per la prima pagina, devi impostare [DifferentFirstPageHeaderFooter](../../pagesetup/get_differentfirstpageheaderfooter/).

Se desideri creare intestazioni e piè di pagina diversi per le pagine pari e dispari, devi impostare [OddAndEvenPagesHeaderFooter](../../pagesetup/get_oddandevenpagesheaderfooter/).

Usa [MoveToSection()](../movetosection/) per uscire dall'intestazione e passare al testo principale.

## Esempi



Mostra come inserire un'immagine e usarla come filigrana.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci l'immagine nell'intestazione in modo che sia visibile su ogni pagina.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);

// Posiziona l'immagine al centro della pagina.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Left((builder->get_PageSetup()->get_PageWidth() - shape->get_Width()) / 2);
shape->set_Top((builder->get_PageSetup()->get_PageHeight() - shape->get_Height()) / 2);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertWatermark.docx");
```

## Vedi anche

* Enum [HeaderFooterType](../../headerfootertype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
