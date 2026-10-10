---
title: "Metodo Aspose::Words::Font::get_NameAscii"
linktitle: "get_NameAscii"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Font::get_NameAscii. Restituisce o imposta il carattere usato per il testo latino (caratteri con codici da 0 (zero) a 127) in C++."
type: docs
weight: 26000
url: /it/cpp/aspose.words/font/get_nameascii/
---
## Font::get_NameAscii method


Restituisce o imposta il carattere usato per il testo latino (caratteri con codici da 0 (zero) a 127).

```cpp
System::String Aspose::Words::Font::get_NameAscii()
```


## Esempi



Mostra come Microsoft Word può combinare due caratteri diversi in un'unica sequenza.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Supponiamo una sequenza che utilizziamo il builder per inserire usando questa configurazione di carattere
// contiene caratteri all'interno dell'intervallo dei caratteri ASCII. In tal caso,
// visualizzerà quei caratteri usando questo carattere.
builder->get_Font()->set_NameAscii(u"Calibri");

// Se non viene specificato alcun altro carattere, il builder applicherà anche questo carattere a tutti i caratteri che inserisce.
ASSERT_EQ(u"Calibri", builder->get_Font()->get_Name());

// Specifica un carattere da usare per tutti i caratteri al di fuori dell'intervallo ASCII.
// Idealmente, questo carattere dovrebbe avere un glifo per ogni codice di carattere non ASCII richiesto.
builder->get_Font()->set_NameOther(u"Courier New");

// Inserisci una sequenza con una parola composta da caratteri ASCII e una parola con tutti i caratteri al di fuori di quell'intervallo.
// Ogni carattere verrà visualizzato usando uno dei due caratteri, a seconda di.
builder->Writeln(u"Hello, Привет");

doc->Save(get_ArtifactsDir() + u"Font.NameAscii.docx");
```

## Vedi anche

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
